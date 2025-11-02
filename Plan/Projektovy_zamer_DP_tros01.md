# Projektový záměr diplomové práce „Realizace báze znalostí skautských programů
“

**Diplomant:** Šimon Trousil
**Vedoucí DP:** Václav Řepa
**Datum vypracování:** 11.5.2025

---

## 1 Vymezení projektu

### 1.1 Cíle projektu

| ID | Cíl projektu
                                   | Metrika
                            | Indikátor dosažení cíle (cílová hodnota metriky)
                                     |
|----|--------------------------------------------------------------------------
-----------------------------------|--------------------------------------------
----------------------------|---------------------------------------------------
-------------------------------------|
| 1  | Analyzovat a popsat využití konceptuálních modelů (specificky UML) pro n
ávrh schémat grafových databází.       | Počet a hloubka popsaných transformačn
ích pravidel a doporučení.       | Vytvoření sady minimálně 5 doporučení a 3 ant
i-patternů pro převod UML na Labeled-Property Graph. |
| 2  | Implementovat prototyp báze znalostí obsahující nejužitečnější funkcional
ity identifikované z bakalářské práce a dotazníkového šetření. | Procento implem
entovaných a uživateli ověřených funkcionalit.         | Minimálně 50 % navržen
ých klíčových entit a vztahů implementováno a pozitivně ověřeno v uživatelském t
estování. |
| 3  | Vytvořit ucelenou uživatelskou dokumentaci a sadu příkladů pro efektivní
práci s vytvořenou bází znalostí.      | Počet a komplexnost zdokumentovaných do
tazů a případů užití.           | Dokumentace obsahuje minimálně 10 praktických
Cypher dotazů pokrývajících běžné uživatelské scénáře. |

### 1.2 Předmětem projektu není

- Implementace kompletního rozsahu báze znalostí navržené v bakalářské práci.
- Vytvoření plnohodnotného grafického uživatelského rozhraní (GUI). Interakce s
bází bude probíhat přes Neo4j Browser.
- Formální testování kódu (unit testy, integrační testy). Důraz je kladen na fun
kční prototyp.

### 1.3 Očekávané přínosy projektu

- **Pro skautský oddíl:** Prakticky využitelný nástroj pro plánování a vyhledáv
ání ve skautských programech, který zefektivní přípravu akcí.
- **Pro akademickou obec:** Souhrn doporučení a osvědčených postupů pro transfor
maci konceptuálních modelů (UML) na grafová schémata, což přispěje k metodice n
ávrhu GDB.

### 1.4 Předpoklady realizace projektu

- **Doménové znalosti:** Diplomant má dostatečné znalosti skautského prostředí a
 programů (splněno).
- **Technologická dostupnost:** Volně dostupný přístup k databázi Neo4j (Communi
ty Edition) pro vývoj a testování.
- **Uživatelská zpětná vazba:** Ochota členů skautských oddílů zapojit se do dot
azníkového šetření a uživatelského testování.

### 1.5 Omezení projektu

| Omezení                                       | Zdůvodnění
                                                      | Dopad na projekt a řešen
í
                                                                              |
|-----------------------------------------------|-------------------------------
------------------------------------------------------|-------------------------
--------------------------------------------------------------------------------
------------------------------------------------------------------------------|
| **Minimální provozní náklady**                | Řešení je určeno pro neziskovo
u organizaci (skautský oddíl) s omezeným rozpočtem.   | Využití open-source tech
nologií (Neo4j Community Edition) a zvážení nasazení na hardware s nízkými nákla
dy. Omezení se projeví i ve výběru rozsahu implementace.                  |
| **Důraz na teoretický přínos**                | Práce je realizována v rámci s
tudijního oboru Aplikovaná informatika, kde je kladen důraz na obecnější, metodi
cký přínos. | Kromě implementace bude velká část práce věnována teoretické anal
ýze a tvorbě doporučení pro modelování GDB, což tvoří významnou část hodnocení.
                                   |
| **Vyvážení implementace a teoretické části** | Potřeba doručit funkční prototy
p a zároveň splnit akademické požadavky na teoretický přínos. | Projekt je rozd
ělen na dvě hlavní části: teoretickou (rešerše, analýza, doporučení) a prakticko
u (implementace, testování). Časový plán je navržen tak, aby obě části byly vyv
ážené. |

### 1.6 Vazby na ostatní projekty diplomových prací

- Nejsou známy žádné přímé vazby na jiné diplomové práce. Projekt je primárně po
kračováním vlastní bakalářské práce diplomanta.

### 1.7 Vazby na případné jiné projekty

- Do budoucna existuje potenciál pro napojení báze znalostí na další skautské sy
stémy, jako je interní informační systém (skautIS), pro sdílení dat.

### 1.8 Východiska uvažovaná při zpracování projektového záměru

- Bakalářská práce "Návrh báze znalostí skautských programů" (Trousil, 2023).
- Praktická potřeba efektivnějšího plánování a vyhledávání v programech skautsk
ých oddílů.
- Rostoucí relevance grafových databází pro správu a analýzu propojených dat.

---

## 2 SWOT faktory projektu

|                                                  | Faktor

                       | Opatření (k eliminaci/využití)

                   |
|--------------------------------------------------|----------------------------
--------------------------------------------------------------------------------
-----------------------|--------------------------------------------------------
--------------------------------------------------------------------------------
-------------------|
| **Příležitosti (Opportunities)**                 | **Nízká konkurence:** Exist
ující nástroje pro správu skautských programů jsou funkčně omezené nebo zastaral
é.                     | Prototyp bude navržen tak, aby pokrýval klíčové funkcio
nality a demonstroval výhody grafového přístupu, čímž se jasně odliší od stávaj
ících řešení.          |
| **Nebezpečí (Threats)**                          | **Omezené uživatelské rozhr
aní:** Interakce přes Neo4j Browser může být pro běžné uživatele bez znalosti ja
zyka Cypher překážkou. | Bude vytvořena podrobná uživatelská dokumentace s kniho
vnou předpřipravených, parametrizovatelných Cypher dotazů pro nejčastější případ
y užití. Uživatelé tak nebudou muset psát dotazy od nuly. |
| **Silné stránky (Strengths)**                    | **Hluboké doménové znalosti
:** Diplomant je aktivním členem skautského oddílu a rozumí potřebám cílové skup
iny.                      | Doménové znalosti budou využity pro návrh relevantn
ího a prakticky použitelného datového modelu a funkcionalit. Umožní také efektiv
nější komunikaci s uživateli při sběru zpětné vazby. |
| **Slabé stránky (Weaknesses)**                   | **Časová náročnost implemen
tace:** Manuální naplnění databáze a implementace všech funkcí by byla příliš ča
sově náročná.         | Implementace se zaměří na nejužitečnější části definovan
é dotazníkem. Bude vytvořen skript pro automatizovaný import dat z existujících
zdrojů (Google Docs), což minimalizuje manuální práci. |

---

## 3 Hlavní výstupy projektu

| ID | Hlavní výstup projektu                                     | Metriky výst
upu                                   | Indikátory dosažení výstupu
                       | Detailní popis výstupu

                            | Výstupem naplňovaný cíl |
|----|------------------------------------------------------------|-------------
--------------------------------------|-----------------------------------------
-----------------------|--------------------------------------------------------
--------------------------------------------------------------------------------
----------------------------|-------------------------|
| 01 | **Nástroj pro synchronizaci dat**                          | Počet podpor
ovaných typů dokumentů, frekvence synchronizace. | Podpora synchronizace pro min
imálně 2 typy dokumentů (programy, aktivity). | Skript (pravděpodobně v Pythonu
nebo jako Google Apps Script), který automaticky extrahuje, transformuje a nahr
ává data ze strukturovaných Google Docs do Neo4j databáze. | 2
     |
| 02 | **Analýza žádanosti funkcionalit**                         | Počet respon
dentů dotazníku, počet identifikovaných priorit. | Získání odpovědí od minimáln
ě 10 respondentů a sestavení prioritizovaného seznamu funkcionalit. | Zpracovan
é a vyhodnocené výsledky dotazníkového šetření, které slouží jako podklad pro ro
zhodnutí, které části báze implementovat.                                    | 2
                       |
| 03 | **Uživatelská dokumentace**                                | Počet kapito
l, počet a složitost příkladů.         | Kompletní dokumentace s minimálně 10 pr
aktickými příklady Cypher dotazů. | Příručka pro koncové uživatele, která popisu
je datový model, způsob pokládání dotazů a obsahuje "receptář" na řešení běžných
 úloh.                                    | 3                       |
| 04 | **Metodika pro návrh GDB schémat**                       | Počet a releva
nce doporučení a anti-patternů.      | Formulace minimálně 5 konkrétních doporu
čení a 3 anti-patternů. | Soubor osvědčených postupů pro převod konceptuálního m
odelu (UML) na fyzické schéma v grafové databázi, včetně ukázek, jak se vyvarova
t častých chyb v modelování.    | 1                       |

---

## 4 Plánované etapy projektu

| ID etapy | Název etapy                                         | Výstupy etapy
                                                              | Termín ukončení
|
|----------|-----------------------------------------------------|--------------
--------------------------------------------------------------|-----------------
|
| A        | Rešerše - konceptuální model GDB                    | Seznam releva
ntních zdrojů, teoretický základ, draft metodiky pro návrh GDB | 30.6.2025
 |
| B        | Dotazník – žádanost údajů a funkcí                  | Formulář dota
zníku, sesbíraná a vyhodnocená data                           | 31.7.2025
|
| C        | Implementace – prototyp a synchronizace             | Funkční proto
typ báze, synchronizační skript, testovací data               | 30.9.2025
|
| D        | Vyhodnocení a uživatelské testování                 | Zpráva z vyho
dnocení, seznam nejvyužívanějších funkcí, zpětná vazba        | 31.10.2025
|
| E        | Kompletace – dokumentace, doporučení a text práce   | Finální uživa
telská dokumentace, metodika pro návrh GDB, text DP           | 30.11.2025
|
