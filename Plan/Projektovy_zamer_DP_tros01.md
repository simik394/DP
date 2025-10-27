# Projektový záměr diplomové práce „Realizace báze znalostí skautských programů“

**Diplomant:** Šimon Trousil
**Vedoucí DP:** Václav Řepa
**Datum vypracování:** 11.5.2025

---

## 1 Vymezení projektu

### 1.1 Cíle projektu

| ID | Cíl projektu                                                                                                | Metrika                                                                | Indikátor dosažení cíle (cílová hodnota metriky)                                       |
|----|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| 1  | Analyzovat a popsat využití konceptuálních modelů (specificky UML) pro návrh schémat grafových databází.       | Počet a hloubka popsaných transformačních pravidel a doporučení.       | Vytvoření sady minimálně 5 doporučení a 3 anti-patternů pro převod UML na Labeled-Property Graph. |
| 2  | Implementovat prototyp báze znalostí obsahující nejužitečnější funkcionality identifikované z bakalářské práce a dotazníkového šetření. | Procento implementovaných a uživateli ověřených funkcionalit.         | Minimálně 50 % navržených klíčových entit a vztahů implementováno a pozitivně ověřeno v uživatelském testování. |
| 3  | Vytvořit ucelenou uživatelskou dokumentaci a sadu příkladů pro efektivní práci s vytvořenou bází znalostí.      | Počet a komplexnost zdokumentovaných dotazů a případů užití.           | Dokumentace obsahuje minimálně 10 praktických Cypher dotazů pokrývajících běžné uživatelské scénáře. |

### 1.2 Předmětem projektu není

- Implementace kompletního rozsahu báze znalostí navržené v bakalářské práci.
- Vytvoření plnohodnotného grafického uživatelského rozhraní (GUI). Interakce s bází bude probíhat přes Neo4j Browser.
- Formální testování kódu (unit testy, integrační testy). Důraz je kladen na funkční prototyp.

### 1.3 Očekávané přínosy projektu

- **Pro skautský oddíl:** Prakticky využitelný nástroj pro plánování a vyhledávání ve skautských programech, který zefektivní přípravu akcí.
- **Pro akademickou obec:** Souhrn doporučení a osvědčených postupů pro transformaci konceptuálních modelů (UML) na grafová schémata, což přispěje k metodice návrhu GDB.

### 1.4 Předpoklady realizace projektu

- **Doménové znalosti:** Diplomant má dostatečné znalosti skautského prostředí a programů (splněno).
- **Technologická dostupnost:** Volně dostupný přístup k databázi Neo4j (Community Edition) pro vývoj a testování.
- **Uživatelská zpětná vazba:** Ochota členů skautských oddílů zapojit se do dotazníkového šetření a uživatelského testování.

### 1.5 Omezení projektu

| Omezení                                       | Zdůvodnění                                                                          | Dopad na projekt a řešení                                                                                                                                                             |
|-----------------------------------------------|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Minimální provozní náklady**                | Řešení je určeno pro neziskovou organizaci (skautský oddíl) s omezeným rozpočtem.   | Využití open-source technologií (Neo4j Community Edition) a zvážení nasazení na hardware s nízkými náklady. Omezení se projeví i ve výběru rozsahu implementace.                  |
| **Důraz na teoretický přínos**                | Práce je realizována v rámci studijního oboru Aplikovaná informatika, kde je kladen důraz na obecnější, metodický přínos. | Kromě implementace bude velká část práce věnována teoretické analýze a tvorbě doporučení pro modelování GDB, což tvoří významnou část hodnocení.                                    |
| **Vyvážení implementace a teoretické části** | Potřeba doručit funkční prototyp a zároveň splnit akademické požadavky na teoretický přínos. | Projekt je rozdělen na dvě hlavní části: teoretickou (rešerše, analýza, doporučení) a praktickou (implementace, testování). Časový plán je navržen tak, aby obě části byly vyvážené. |

### 1.6 Vazby na ostatní projekty diplomových prací

- Nejsou známy žádné přímé vazby na jiné diplomové práce. Projekt je primárně pokračováním vlastní bakalářské práce diplomanta.

### 1.7 Vazby na případné jiné projekty

- Do budoucna existuje potenciál pro napojení báze znalostí na další skautské systémy, jako je interní informační systém (skautIS), pro sdílení dat.

### 1.8 Východiska uvažovaná při zpracování projektového záměru

- Bakalářská práce "Návrh báze znalostí skautských programů" (Trousil, 2023).
- Praktická potřeba efektivnějšího plánování a vyhledávání v programech skautských oddílů.
- Rostoucí relevance grafových databází pro správu a analýzu propojených dat.

---

## 2 SWOT faktory projektu

|                                                  | Faktor                                                                                                                            | Opatření (k eliminaci/využití)                                                                                                                            |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Příležitosti (Opportunities)**                 | **Nízká konkurence:** Existující nástroje pro správu skautských programů jsou funkčně omezené nebo zastaralé.                     | Prototyp bude navržen tak, aby pokrýval klíčové funkcionality a demonstroval výhody grafového přístupu, čímž se jasně odliší od stávajících řešení.          |
| **Nebezpečí (Threats)**                          | **Omezené uživatelské rozhraní:** Interakce přes Neo4j Browser může být pro běžné uživatele bez znalosti jazyka Cypher překážkou. | Bude vytvořena podrobná uživatelská dokumentace s knihovnou předpřipravených, parametrizovatelných Cypher dotazů pro nejčastější případy užití. Uživatelé tak nebudou muset psát dotazy od nuly. |
| **Silné stránky (Strengths)**                    | **Hluboké doménové znalosti:** Diplomant je aktivním členem skautského oddílu a rozumí potřebám cílové skupiny.                      | Doménové znalosti budou využity pro návrh relevantního a prakticky použitelného datového modelu a funkcionalit. Umožní také efektivnější komunikaci s uživateli při sběru zpětné vazby. |
| **Slabé stránky (Weaknesses)**                   | **Časová náročnost implementace:** Manuální naplnění databáze a implementace všech funkcí by byla příliš časově náročná.         | Implementace se zaměří na nejužitečnější části definované dotazníkem. Bude vytvořen skript pro automatizovaný import dat z existujících zdrojů (Google Docs), což minimalizuje manuální práci. |

---

## 3 Hlavní výstupy projektu

| ID | Hlavní výstup projektu                                     | Metriky výstupu                                   | Indikátory dosažení výstupu                                    | Detailní popis výstupu                                                                                                                                             | Výstupem naplňovaný cíl |
|----|------------------------------------------------------------|---------------------------------------------------|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| 01 | **Nástroj pro synchronizaci dat**                          | Počet podporovaných typů dokumentů, frekvence synchronizace. | Podpora synchronizace pro minimálně 2 typy dokumentů (programy, aktivity). | Skript (pravděpodobně v Pythonu nebo jako Google Apps Script), který automaticky extrahuje, transformuje a nahrává data ze strukturovaných Google Docs do Neo4j databáze. | 2                       |
| 02 | **Analýza žádanosti funkcionalit**                         | Počet respondentů dotazníku, počet identifikovaných priorit. | Získání odpovědí od minimálně 10 respondentů a sestavení prioritizovaného seznamu funkcionalit. | Zpracované a vyhodnocené výsledky dotazníkového šetření, které slouží jako podklad pro rozhodnutí, které části báze implementovat.                                    | 2                       |
| 03 | **Uživatelská dokumentace**                                | Počet kapitol, počet a složitost příkladů.         | Kompletní dokumentace s minimálně 10 praktickými příklady Cypher dotazů. | Příručka pro koncové uživatele, která popisuje datový model, způsob pokládání dotazů a obsahuje "receptář" na řešení běžných úloh.                                    | 3                       |
| 04 | **Metodika pro návrh GDB schémat**                       | Počet a relevance doporučení a anti-patternů.      | Formulace minimálně 5 konkrétních doporučení a 3 anti-patternů. | Soubor osvědčených postupů pro převod konceptuálního modelu (UML) na fyzické schéma v grafové databázi, včetně ukázek, jak se vyvarovat častých chyb v modelování.    | 1                       |

---

## 4 Plánované etapy projektu

| ID etapy | Název etapy                                         | Výstupy etapy                                                              | Termín ukončení |
|----------|-----------------------------------------------------|----------------------------------------------------------------------------|-----------------|
| A        | Rešerše - konceptuální model GDB                    | Seznam relevantních zdrojů, teoretický základ, draft metodiky pro návrh GDB | 30.6.2025       |
| B        | Dotazník – žádanost údajů a funkcí                  | Formulář dotazníku, sesbíraná a vyhodnocená data                           | 31.7.2025       |
| C        | Implementace – prototyp a synchronizace             | Funkční prototyp báze, synchronizační skript, testovací data               | 30.9.2025       |
| D        | Vyhodnocení a uživatelské testování                 | Zpráva z vyhodnocení, seznam nejvyužívanějších funkcí, zpětná vazba        | 31.10.2025      |
| E        | Kompletace – dokumentace, doporučení a text práce   | Finální uživatelská dokumentace, metodika pro návrh GDB, text DP           | 30.11.2025      |
