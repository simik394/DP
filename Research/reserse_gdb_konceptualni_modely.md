# Rešerše: Konceptuální modely pro grafové databáze

Tento dokument shrnuje poznatky z rešerše na téma využití konceptuálních modelů pro tvorbu grafových databází, se zaměřením na databázi Neo4j.

## 1. Základní pojmy

- **Grafová databáze (GDB):** Databáze, která využívá grafové struktury (uzly, hrany a vlastnosti) k reprezentaci a ukládání dat. Klíčovým konceptem je vztah (hrana), který přímo spojuje datové položky a umožňuje rychlé prohledávání složitých vazeb.
- **Uzly (Nodes):** Reprezentují entity, jako jsou osoby, produkty nebo události. Odpovídají záznamům nebo řádkům v relačních databázích.
- **Hrany (Edges/Relationships):** Reprezentují vztahy mezi uzly. Mohou být orientované (směrové) a mít vlastní vlastnosti.
- **Vlastnosti (Properties):** Klíč-hodnota páry, které ukládají data o uzlech a hranách.

## 2. Modely grafových databází

Existují dva hlavní modely grafových databází:

- **Labeled-Property Graph (LPG):** Tento model, který používá i Neo4j, se skládá z uzlů, vztahů, vlastností a popisků (labels). Uzly mohou mít popisky, které je seskupují do kategorií. Vztahy mají typ, směr, a mohou mít vlastnosti.
- **Resource Description Framework (RDF):** Model založený na trojicích subjekt-predikát-objekt. Každá informace je reprezentována jako samostatný uzel, což může vést ke složitějším strukturám pro reprezentaci jednoduchých dat.

## 3. Postup při modelování grafové databáze

Proces tvorby datového modelu pro grafovou databázi lze shrnout do následujících kroků:

1.  **Pochopení domény a definice případů užití:** Je klíčové porozumět datům a definovat si, jaké otázky chceme databázi pokládat.
2.  **Identifikace entit a vztahů:**
    -   **Entity (Uzly):** Identifikujte klíčové objekty ve vaší doméně. Začněte s centrální entitou a postupně přidávejte další.
    -   **Vztahy (Hrany):** Určete, jak jsou entity mezi sebou propojeny. Vztahy by měly být co nejvíce popisné a specifické.
3.  **Přiřazení vlastností:** Doplňte k uzlům a hranám vlastnosti, které nesou potřebná data.
4.  **Definice schématu:** Ačkoliv jsou grafové databáze často flexibilní, je dobré si definovat základní schéma – jaké typy uzlů a vztahů existují a jaké mají vlastnosti.
5.  **Testování a refaktorizace:** Vytvořte testovací data, vyzkoušejte své případy užití a na základě výsledků a výkonu model upravujte.

## 4. Osvědčené postupy a doporučení

-   **Modelujte vztahy jako "first-class citizens":** Vztahy jsou v GDB stejně důležité jako uzly. Používejte specifické a popisné typy vztahů.
-   **Optimalizujte pro dotazy:** Navrhujte model tak, aby co nejvíce zjednodušoval a urychloval typické dotazy. Nebojte se denormalizace, pokud to zlepší výkon.
-   **Používejte popisky (labels) pro seskupování uzlů:** Popisky umožňují snadné a rychlé vyhledávání skupin uzlů.
-   **Vizualizujte si schéma:** Vizuální reprezentace schématu (např. pomocí ERD nebo nástrojů jako arrows.app) pomáhá lépe pochopit strukturu a komunikovat ji v týmu.

## 5. Převod z konceptuálního modelu na grafové schéma

Zásadní výhodou grafových databází je, že jejich logický model je velmi blízko konceptuálnímu modelu. Na rozdíl od relačních databází, kde se konceptuální model musí často složitě transformovat a normalizovat (což vede ke vzniku spojovacích tabulek a cizích klíčů), je převod do grafového modelu mnohem přímočařejší.

Základní pravidla pro transformaci jsou (Needham, 2014):

-   **Entity → Uzly / Popisky (Nodes / Labels):** Každá entita z konceptuálního modelu (např. Osoba, Kniha) se stane uzlem. Typ entity se reprezentuje popiskem (Label).
-   **Atributy → Vlastnosti (Properties):** Atributy entity (např. jméno osoby, název knihy) se stanou vlastnostmi daného uzlu.
-   **Vztahy → Vztahy (Relationships):** Vztahy mezi entitami (např. `WROTE`, `PURCHASED`) se přímo přenesou jako sémantické, orientované vztahy mezi uzly.
-   **Identifikátory → Unikátní omezení (Unique Constraints):** Unikátní identifikátory entit se v databázi vynucují pomocí unikátních omezení na vlastnosti.

Tento přístup, často označovaný jako "whiteboard friendly", znamená, že model, který si načrtnete na tabuli, je téměř identický s tím, jak je uložen v databázi. To usnadňuje komunikaci a udržuje model blízko byznys logice.

Složitost a prostor pro různá řešení vzniká až při modelování pokročilejších struktur, jako jsou:
-   Dědičnost (Inheritance)
-   Agregace a kompozice
-   N-ární vztahy (vztahy mezi více než dvěma entitami)
-   Reprezentace času a historie

Právě v těchto oblastech je potřeba aplikovat specifické návrhové vzory a rozhodovací pravidla, která budou předmětem dalšího zkoumání.

### 5.1 Příklad: Modelování dědičnosti (IS-A)

Dědičnost je klíčový koncept v UML, který v grafu nemá jediný správný ekvivalent. Existuje několik validních přístupů, a volba závisí na povaze dat a typických dotazech.

**Přístup 1: Více popisků (Multiple Labels)**

Tento přístup je nejčastější pro modelování **pevné, taxonomické klasifikace**. Potomek v hierarchii dostane jak svůj vlastní popisek, tak i popisek svého předka.

-   **Příklad:** `CREATE (c:Car:Vehicle {name: 'My Car'})`
-   **Výhody:**
    -   Velmi efektivní dotazy (`MATCH (v:Vehicle)` najde všechna vozidla, včetně aut).
    -   Intuitivní a čistý model pro statické hierarchie.
-   **Nevýhody:**
    -   Nevhodné pro dynamické hierarchie, které se často mění (změna labelu je náročná operace).
    -   Nelze přiřadit vlastnosti samotnému vztahu dědičnosti.

**Přístup 2: Explicitní vztah (`IS_A`)**

Tento přístup modeluje dědičnost jako explicitní vztah mezi uzly. Je vhodnější pro **dynamické nebo složitější hierarchie**.

-   **Příklad:** `CREATE (:Car {name: 'My Car'})-[:IS_A]->(:Vehicle)`
-   **Výhody:**
    -   Flexibilní – hierarchii lze snadno měnit přidáváním/mazáním vztahů.
    -   Na vztah `IS_A` lze přidat vlastnosti (např. `since`, `confidence`).
-   **Nevýhody:**
    -   Dotazy na celou hierarchii jsou mírně složitější a pomalejší (vyžadují traversál přes vztahy, např. `MATCH (c:Car)-[:IS_A*]->(v:Vehicle)`).

**Přístup 3: Kategorie a dědičnost atributů**

Jak popisuje blog Neo4j (2010), hierarchii lze modelovat jako strom kategorií. Tento přístup je silný, pokud potřebujeme, aby produkty nebo entity **dědily vlastnosti od svých kategorií**.

-   **Příklad:** `(:Product)-[:IN_CATEGORY]->(:SubCategory)-[:SUBCATEGORY_OF]->(:Category)`
-   **Výhody:**
    -   Umožňuje definovat atributy na úrovni kategorie a aplikovat je na všechny členy.
    -   Elegantně řeší problém správy atributů pro velké množství položek.
-   **Nevýhody:**
    -   Primárně řeší dědičnost atributů, ne nutně sémantický "IS-A" vztah v pravém slova smyslu.

**Rozhodovací bod:**
Klíčovou otázkou při výběru je: *Jedná se o statickou klasifikaci (pes je zvíře), nebo o dynamickou, atributy dědící strukturu (produkt patří do kategorie)?* Odpověď na tuto otázku určí, který z výše uvedených modelů je nejvhodnější.

### 5.2 Pracovní hypotéza

Na základě analýzy lze formulovat následující pracovní hypotézu:

*Přestože základní transformace konceptuálního modelu (UML) na Labeled-Property Graph model je relativně přímočará (entita → uzel, atribut → vlastnost), pro komplexní sémantické konstrukty (jako dědičnost, agregace, n-ární vztahy) existuje více validních transformačních strategií. Volba optimální strategie není libovolná, ale je systematicky odvoditelná z analýzy zamýšlených dotazů a případů užití (query-driven design). Různé strategie vedou k různým grafovým schématům, které se liší flexibilitou, čitelností a především výkonem pro specifické typy dotazů.*

Tato hypotéza bude v další části práce ověřována na příkladech dalších UML konstruktů a následně demonstrována na praktickém modelu skautské domény.

### 5.3 Příklad: Modelování agregace a kompozice (HAS-A)

Agregace a kompozice reprezentují "whole-part" (celek-část) vztahy. Klíčový rozdíl mezi nimi v UML je závislost životního cyklu:
- **Agregace (Aggregation):** Slabý vztah. Části mohou existovat i po zániku celku. (Např. Tým a Členové).
- **Kompozice (Composition):** Silný vztah. Části jsou zničeny spolu s celkem. (Např. Auto a Motor).

V Labeled-Property Graph modelu, jako je Neo4j, neexistuje vestavěný mechanismus, který by tyto dva typy vztahů na úrovni schématu rozlišoval. Rozdíl se tedy musí implementovat v logice datového modelu a operací.

**Přístup k modelování:**

Oba vztahy se modelují jako standardní sémantické vztahy. Volba názvu vztahu by měla jasně odrážet povahu vazby.
- **Agregace:** `(:Team)-[:HAS_MEMBER]->(:Person)`
- **Kompozice:** `(:Car)-[:CONSISTS_OF]->(:Engine)`

**Rozhodovací bod a implementace:**

Rozdíl se projeví až při operaci mazání. To představuje klíčový rozhodovací bod při návrhu aplikace.
- **Pro agregaci:** Při smazání uzlu `Team` se jednoduše smaže jen tento uzel. Vztahy `HAS_MEMBER` zaniknou, ale uzly `Person` zůstanou nedotčeny.
  - `MATCH (t:Team {name: 'MyTeam'}) DELETE t;` (POZOR: `DETACH DELETE` by smazalo i vztahy, ale ne členy)
- **Pro kompozici:** Při smazání uzlu `Car` je **nutné** v rámci stejné transakce explicitně smazat i všechny jeho části. Toto je zodpovědnost aplikace nebo specifického Cypher dotazu.
  - `MATCH (c:Car {vin: '123'})-[r:CONSISTS_OF]->(part) DETACH DELETE c, part;`

Zatímco sémantický význam je v UML jasně daný, v grafovém modelu je přenesen z deklarativní úrovně (schéma) na imperativní úroveň (operace). To dává větší flexibilitu, ale zároveň klade větší nároky na disciplínu při vývoji.

## 6. Použité zdroje

-   [Graph database - Wikipedia](https://en.wikipedia.org/wiki/Graph_database)
-   [7 Best Graph Database Modeling Tools In 2025 - PuppyGraph](https://www.puppygraph.com/blog/graph-database-modeling-tools)
-   [What is graph data modeling? - Getting Started - Neo4j](https://neo4j.com/docs/getting-started/data-modeling/)
-   [Graph database concepts - Getting Started - Neo4j](https://neo4j.com/docs/getting-started/appendix/graphdb-concepts/)
-   [The ultimate guide to creating graph data models - Cambridge Intelligence](https://cambridge-intelligence.com/graph-data-modeling-101/)
-   [Neo4j Data Modeling Best Practices and Tips](https://neo4j.guide/article/Neo4j_Data_Modeling_Best_Practices_and_Tips.html)
-   [Conceptual Model vs Graph Model - Mark Needham, Neo4j Blog (2014)](https://neo4j.com/blog/graph-database/conceptual-model-vs-graph-model/)
-   [Modeling Categories in a Graph Database - Neo4j Blog (2010)](https://neo4j.com/blog/developer/modeling-categories-in-a-graph-database/)

---
### Dodatek: Zdroje k Agregaci a Kompozici

Následující zdroje byly použity k formulaci závěrů o modelování agregace a kompozice. Ačkoliv se primárně nevěnují Neo4j, definují klíčový princip závislosti životního cyklu, který je nutné implementovat na aplikační úrovni.

-   **Stack Overflow:** [What is the difference between association, aggregation and composition?](https://stackoverflow.com/questions/885937/what-is-the-difference-between-association-aggregation-and-composition) - Zdůrazňuje silnou závislost životního cyklu u kompozice.
-   **Visual Paradigm:** [UML Association vs Aggregation vs Composition](https://www.visual-paradigm.com/guide/uml-unified-modeling-language/uml-aggregation-vs-composition/) - Definuje a srovnává koncepty v kontextu UML.
-   **GeeksforGeeks:** [Association, Composition and Aggregation in Java](https://www.geeksforgeeks.org/java/association-composition-aggregation-java/) - Poskytuje příklady implementace v OOP, jejichž principy jsou přenositelné do databázových transakcí.
