# Detailní log rešerše

Tento soubor dokumentuje proces rešerše pro diplomovou práci "Realizace báze znalostí skautských programů".

## Strategie klíčových slov

1.  **Základní přehled:** `graph data modeling`, `graph database schema design patterns`, `conceptual to graph model transformation`.
    *   **Odůvodnění:** Cílem je zopakovat základy a najít zdroje, které byly v první, povrchní rešerši přehlédnuty.
2.  **Akademické zdroje:** `graph database modeling survey`, `property graph vs RDF comparison`, `graph database schema evolution`, `"graph data modeling" filetype:pdf`.
    *   **Odůvodnění:** Cílem je najít odborné články a "research papers" pro zajištění akademické hloubky práce.
3.  **Pokročilé techniky:** `modeling hyperedges in property graphs`, `temporal graph data modeling`, `graph model refactoring`, `"node vs relationship" graph modeling`.
    *   **Odůvodnění:** Cílem je najít specifická řešení pro pokročilé problémy a designové vzory.
4.  **Praktické příklady:** `Neo4j data modeling anti-patterns`, `graph modeling for social networks`, `knowledge graph schema design`.
    *   **Odůvodnění:** Cílem je najít reálné příklady, osvědčené postupy a poučení z chyb z praxe.

---

## Záznam vyhledávání

### Dotaz 1: `graph database schema design patterns` (Google)

1.  **URL:** https://hypermode.com/blog/database-architecture
    *   **Název:** What is Graph Database Architecture? Exploring Schema and Models - Hypermode
    *   **Relevance:** Vysoká. Popisuje základní principy návrhu schématu.
    *   **Použití:** Použito pro úvodní kapitoly rešerše.

### Dotaz 2: `"graph data modeling"` (Google)

2.  **URL:** https://neo4j.com/docs/getting-started/data-modeling/
    *   **Název:** What is graph data modeling? - Getting Started - Neo4j
    *   **Relevance:** Vysoká. Oficiální dokumentace.
    *   **Použití:** Použito.
3.  **URL:** https://linkurious.com/graph-data-modeling/
    *   **Název:** Graph data modeling: A quick guide - Linkurious
    *   **Relevance:** Vysoká. Dobrý přehled pro začátečníky.
    *   **Použití:** Použito pro ujasnění základních pojmů.
4.  **URL:** https://memgraph.com/docs/data-modeling
    *   **Název:** Data modeling - Memgraph
    *   **Relevance:** Střední. Zaměřeno na Memgraph, ale principy jsou obecné.
    *   **Použití:** Použito pro srovnání přístupů.
5.  **URL:** https://hypermode.com/blog/graph-models
    *   **Název:** What is Graph Data Modeling? Techniques and Best Practices - Hypermode
    *   **Relevance:** Vysoká. Podrobný článek s best practices.
    *   **Použití:** Použito pro sekci o osvědčených postupech.

### Dotaz 3: `"graph data modeling" filetype:pdf site:arxiv.org` (ArXiv)

*   **Výsledek:** Žádné relevantní výsledky. Zkusím obecnější dotazy na jiných platformách.

### Dotaz 4: `node vs relationship graph modeling` (Google)

6.  **URL:** https://bigbear.ai/blog/property-graphs-is-it-a-node-a-relationship-or-a-property/
    *   **Název:** Property Graphs: Is it a Node, a Relationship, or a Property? - BigBear.ai
    *   **Relevance:** Velmi vysoká. Přesně se zabývá klíčovou otázkou modelování.
    *   **Použití:** Bude tvořit jádro kapitoly o pokročilém modelování.
7.  **URL:** https://aws.amazon.com/compare/the-difference-between-graph-and-relational-database/
    *   **Název:** Graph vs Relational Databases - Difference Between Databases - AWS
    *   **Relevance:** Střední. Spíše srovnání GDB a RDB, ale dotýká se i modelování.
    *   **Použití:** Doplňující materiál.

### Dotaz 5: `Neo4j data modeling anti-patterns` (Google)

8.  **URL:** https://neo4j.com/blog/cypher-and-gql/dark-side-neo4j-worst-practices/
    *   **Název:** Welcome to the Dark Side: Neo4j Worst Practices (& How to Avoid Them)
    *   **Relevance:** Velmi vysoká. Konkrétní příklady, čemu se vyhnout.
    *   **Použití:** Bude tvořit základ pro kapitolu o anti-patternech a osvědčených postupech.

### Dotaz 6: `temporal graph data modeling` (Google Scholar)

*   **Výsledek:** Žádné relevantní výsledky. Budu muset zkusit jiné dotazy a platformy.

### Dotaz 7: `graph database modeling survey` (Google)

9.  **URL:** https://arxiv.org/abs/2505.24758
    *   **Název:** [2505.24758] Survey: Graph Databases - arXiv
    *   **Relevance:** Velmi vysoká. Aktuální přehledový článek.
    *   **Použití:** Klíčový zdroj pro teoretickou část.
10. **URL:** https://repositorio.uchile.cl/bitstream/handle/2250/125044/ANGLES_RENZO.pdf?sequence=1
    *   **Název:** Survey of Graph Database Models - Repositorio UCHILE
    *   **Relevance:** Vysoká. Starší, ale velmi citovaný a foundational článek.
    *   **Použití:** Zdroj pro historický kontext a základní definice.
11. **URL:** https://www.dcc.uchile.cl/TR/2005/TR_DCC-2005-010.pdf
    *   **Název:** Survey of Graph Database Models - DCC UChile
    *   **Relevance:** Vysoká. Podobné jako předchozí, ale jiná verze.
    *   **Použití:** Zkontrolovat rozdíly a případně doplnit informace.
12. **URL:** https://www.semanticscholar.org/paper/Survey-of-graph-database-models-Angles-Guti%C3%A9rrez/d57ca29d73272e139c04f118d5c3107dfb964596
    *   **Název:** [PDF] Survey of graph database models - Semantic Scholar
    *   **Relevance:** Vysoká. Opět odkaz na stejný článek, ale s metadaty o citacích.
    *   **Použití:** Pomůže najít navazující práce.

---
*Prohledáno 13 zdrojů. Pokračuji v hledání...*

---

## 2025-10-27 (Pokračování)

### Dotazy:
13. `UML to graph schema transformation`
14. `"conceptual model to neo4j" "best practices"`
15. `object-oriented model to property graph`
16. `neo4j data modeling guide from conceptual model`
17. `modeling inheritance UML in Neo4j`
18. `type hierarchies in neo4j`

### Zjištění:
-   Přímé "best practices" pro transformaci UML->Neo4j nejsou snadno dohledatelné, což potvrzuje relevanci tématu DP.
-   Klíčový je článek od Marka Needhama (Neo4j Blog), který stanovuje základní pravidla 1:1 mapování (Entita->Uzel, Atribut->Vlastnost, Vztah->Vztah).
-   Jádro problému leží v řešení pokročilých sémantických konstruktů (dědičnost, agregace, n-ární vztahy), kde existuje více validních řešení.
-   Pro modelování dědičnosti/hierarchie v Neo4j byly identifikovány tři hlavní přístupy:
    1.  **Více popisků (Multiple Labels):** Pro statické, taxonomické hierarchie.
    2.  **Explicitní `IS_A` vztahy:** Pro dynamické hierarchie, kde se může struktura měnit.
    3.  **Strom kategorií:** Pro modelování dědičnosti atributů.
-   Volba mezi těmito přístupy je klíčový **rozhodovací bod**, který závisí na povaze dat a především na zamýšlených dotazech (query-driven design).

### Nápady na další dotazy/klíčová slova:
-   `graph database normalization vs denormalization`
-   `representing n-ary relationships in property graphs patterns`
-   `UML aggregation vs composition in Neo4j modeling`
-   `time representation in graph databases patterns`
-   `object to graph mapping academic paper survey`
-   `conceptual model to logical graph model transformation rules`
-   `Neo4j composite key implementation`
-   `resolving many-to-many relationships graph best practices`

---

## 2025-11-01 (Pokračování)

### Dotazy:
19. `UML aggregation vs composition in Neo4j modeling`
20. `neo4j cascade delete relationship`
21. `enforcing lifecycle dependency neo4j`
22. `graph modeling composition vs aggregation`

### Zjištění:
-   Jak **agregace**, tak **kompozice** se v Neo4j typicky modelují pomocí standardního vztahu `(parent)-[:HAS_A]->(child)` nebo podobně sémanticky pojmenovaného vztahu. Z pohledu čisté struktury grafu jsou nerozlišitelné.
-   Klíčový rozdíl je v **sémantice životního cyklu**: u kompozice platí, že "dítě" (child) nemůže existovat bez "rodiče" (parent). Smazání rodiče musí nutně vést ke smazání dítěte.
-   Tato sémantika se **nevynucuje na úrovni schématu** v Neo4j, ale na **aplikační/operační úrovni**.
-   Standardním řešením je použití **transakčního smazání s kaskádou (cascade delete)**. Při operaci mazání uzlu, který je součástí kompozice, je nutné explicitně smazat i všechny jeho související "dětské" uzly v rámci jedné transakce.
-   Některé knihovny a OGM (Object-Graph Mapper) nástroje mohou toto chování automatizovat, ale v čistém Cypheru je za to zodpovědný vývojář.
-   **Závěr:** Rozdíl mezi agregací a kompozicí není ve způsobu, jak jsou *uloženy* v grafu, ale ve způsobu, jak jsou *spravovány* operacemi (především mazáním). Toto zjištění musí být v DP jasně uvedeno.

---
## 2025-11-01 (Dodatek - Zdroje k Agregaci/Kompozici)

Tato sekce explicitně doplňuje zdroje použité pro zjištění z předchozího záznamu, aby se napravila chyba v dokumentaci.

### Použité zdroje:
-   **URL:** https://stackoverflow.com/questions/885937/what-is-the-difference-between-association-aggregation-and-composition
    -   **Název:** What is the difference between association, aggregation and composition? - Stack Overflow
    -   **Relevance:** Vysoká. Jasně vysvětluje sémantiku životního cyklu.
-   **URL:** https://www.visual-paradigm.com/guide/uml-unified-modeling-language/uml-aggregation-vs-composition/
    -   **Název:** UML Association vs Aggregation vs Composition - Visual Paradigm
    -   **Relevance:** Vysoká. Definuje koncepty z pohledu UML.
-   **URL:** https://www.geeksforgeeks.org/java/association-composition-aggregation-java/
    -   **Název:** Association, Composition and Aggregation in Java - GeeksforGeeks
    -   **Relevance:** Střední. Ukazuje, jak se princip řeší v OOP.
-   **URL:** https://www.gleek.io/blog/aggregation-vs-composition
    -   **Název:** UML Essentials: Aggregation vs Composition Explained - Gleek.io
    -   **Relevance:** Střední. Dobré shrnutí a příklady.
