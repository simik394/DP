# Detailní log rešerše

Tento soubor dokumentuje proces rešerše pro diplomovou práci "Realizace báze zna
lostí skautských programů".

## Strategie klíčových slov

1.  **Základní přehled:** `graph data modeling`, `graph database schema design p
atterns`, `conceptual to graph model transformation`.
    *   **Odůvodnění:** Cílem je zopakovat základy a najít zdroje, které byly v
první, povrchní rešerši přehlédnuty.
2.  **Akademické zdroje:** `graph database modeling survey`, `property graph vs
RDF comparison`, `graph database schema evolution`, `"graph data modeling" filet
ype:pdf`.
    *   **Odůvodnění:** Cílem je najít odborné články a "research papers" pro za
jištění akademické hloubky práce.
3.  **Pokročilé techniky:** `modeling hyperedges in property graphs`, `temporal
graph data modeling`, `graph model refactoring`, `"node vs relationship" graph m
odeling`.
    *   **Odůvodnění:** Cílem je najít specifická řešení pro pokročilé problémy
a designové vzory.
4.  **Praktické příklady:** `Neo4j data modeling anti-patterns`, `graph modeling
 for social networks`, `knowledge graph schema design`.
    *   **Odůvodnění:** Cílem je najít reálné příklady, osvědčené postupy a pou
čení z chyb z praxe.

---

## Záznam vyhledávání

### Dotaz 1: `graph database schema design patterns` (Google)

1.  **URL:** https://hypermode.com/blog/database-architecture
    *   **Název:** What is Graph Database Architecture? Exploring Schema and Mod
els - Hypermode
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
    *   **Název:** What is Graph Data Modeling? Techniques and Best Practices -
Hypermode
    *   **Relevance:** Vysoká. Podrobný článek s best practices.
    *   **Použití:** Použito pro sekci o osvědčených postupech.

### Dotaz 3: `"graph data modeling" filetype:pdf site:arxiv.org` (ArXiv)

*   **Výsledek:** Žádné relevantní výsledky. Zkusím obecnější dotazy na jiných p
latformách.

### Dotaz 4: `node vs relationship graph modeling` (Google)

6.  **URL:** https://bigbear.ai/blog/property-graphs-is-it-a-node-a-relationship
-or-a-property/
    *   **Název:** Property Graphs: Is it a Node, a Relationship, or a Property?
 - BigBear.ai
    *   **Relevance:** Velmi vysoká. Přesně se zabývá klíčovou otázkou modelován
í.
    *   **Použití:** Bude tvořit jádro kapitoly o pokročilém modelování.
7.  **URL:** https://aws.amazon.com/compare/the-difference-between-graph-and-rel
ational-database/
    *   **Název:** Graph vs Relational Databases - Difference Between Databases
- AWS
    *   **Relevance:** Střední. Spíše srovnání GDB a RDB, ale dotýká se i modelo
vání.
    *   **Použití:** Doplňující materiál.

### Dotaz 5: `Neo4j data modeling anti-patterns` (Google)

8.  **URL:** https://neo4j.com/blog/cypher-and-gql/dark-side-neo4j-worst-practic
es/
    *   **Název:** Welcome to the Dark Side: Neo4j Worst Practices (& How to Avo
id Them)
    *   **Relevance:** Velmi vysoká. Konkrétní příklady, čemu se vyhnout.
    *   **Použití:** Bude tvořit základ pro kapitolu o anti-patternech a osvědče
ných postupech.

### Dotaz 6: `temporal graph data modeling` (Google Scholar)

*   **Výsledek:** Žádné relevantní výsledky. Budu muset zkusit jiné dotazy a pla
tformy.

### Dotaz 7: `graph database modeling survey` (Google)

9.  **URL:** https://arxiv.org/abs/2505.24758
    *   **Název:** [2505.24758] Survey: Graph Databases - arXiv
    *   **Relevance:** Velmi vysoká. Aktuální přehledový článek.
    *   **Použití:** Klíčový zdroj pro teoretickou část.
10. **URL:** https://repositorio.uchile.cl/bitstream/handle/2250/125044/ANGLES_R
ENZO.pdf?sequence=1
    *   **Název:** Survey of Graph Database Models - Repositorio UCHILE
    *   **Relevance:** Vysoká. Starší, ale velmi citovaný a foundational článek.
    *   **Použití:** Zdroj pro historický kontext a základní definice.
11. **URL:** https://www.dcc.uchile.cl/TR/2005/TR_DCC-2005-010.pdf
    *   **Název:** Survey of Graph Database Models - DCC UChile
    *   **Relevance:** Vysoká. Podobné jako předchozí, ale jiná verze.
    *   **Použití:** Zkontrolovat rozdíly a případně doplnit informace.
12. **URL:** https://www.semanticscholar.org/paper/Survey-of-graph-database-mode
ls-Angles-Guti%C3%A9rrez/d57ca29d73272e139c04f118d5c3107dfb964596
    *   **Název:** [PDF] Survey of graph database models - Semantic Scholar
    *   **Relevance:** Vysoká. Opět odkaz na stejný článek, ale s metadaty o cit
acích.
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
