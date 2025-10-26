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

## 5. Použité zdroje

-   [Graph database - Wikipedia](https://en.wikipedia.org/wiki/Graph_database)
-   [7 Best Graph Database Modeling Tools In 2025 - PuppyGraph](https://www.puppygraph.com/blog/graph-database-modeling-tools)
-   [What is graph data modeling? - Getting Started - Neo4j](https://neo4j.com/docs/getting-started/data-modeling/)
-   [Graph database concepts - Getting Started - Neo4j](https://neo4j.com/docs/getting-started/appendix/graphdb-concepts/)
-   [The ultimate guide to creating graph data models - Cambridge Intelligence](https://cambridge-intelligence.com/graph-data-modeling-101/)
-   [Neo4j Data Modeling Best Practices and Tips](https://neo4j.guide/article/Neo4j_Data_Modeling_Best_Practices_and_Tips.html)
