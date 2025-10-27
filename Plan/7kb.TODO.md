---
id: TODO
aliases:
  - 7kb.todo
tags: []
---
# PRIORITY
- [x] Dovyplnit Projektový záměr markdown verzi ve složce Plan.
- [ ] Pokračovat ve tvorbě tohoto projektu podle tasků v tomto souboru

## Další kroky
- [ ] **Etapa A: Rešerše (do 30.6.2025)**
  - [ ] **[A1] Teoretický základ**
    - [x] [A1.1] Vyhledat a prostudovat úvodní literaturu o konceptuálních modelech pro GDB.
    - [x] [A1.2] Zpracovat základní teoretický přehled a definice (GDB, LPG, UML).
    - [x] [A1.3] Vytvořit seznam relevantních zdrojů.
  - [ ] **[A2] Jádro rešerše: Transformace UML na grafové schéma**
    - [ ] [A2.1] Prozkoumat a zdokumentovat existující systematické přístupy a metodiky pro převod UML (zejména class diagrams) na Labeled-Property Graph model.
    - [ ] [A2.2] Analyzovat, jak různé interpretace UML konstruktů (asociace, agregace, kompozice, dědičnost) vedou k odlišným, ale validním grafovým schématům.
    - [ ] [A2.3] Identifikovat klíčové rozhodovací body v procesu transformace, které ovlivňují výslednou strukturu grafu (např. reprezentace vztahů jako uzlů vs. hran).
    - [ ] [A2.4] Formulovat hypotézu o tom, jak systematicky odvodit více možných grafových schémat z jednoho UML modelu a jak hodnotit jejich vhodnost pro různé typy dotazů.
  - [ ] **[A3] Návrhové vzory pro grafové databáze**
    - [ ] [A3.1] Provést explorativní rešerši návrhových vzorů v grafových databázích (bez omezení na "běžné" vzory). Hledat inspiraci v různých doménách.
    - [ ] [A3.2] Analyzovat, jak vybrané vzory řeší specifické problémy modelování (např. hierarchie, časové údaje, stavy, n-ární vztahy).
  - [ ] **[A4] Porovnání s relačním modelováním**
    - [ ] [A4.1] Analyzovat klíčové entity a vztahy ze skautské domény (dle BP).
    - [ ] [A4.2] Vytvořit konceptuální model (UML class diagram) pro vybranou část domény.
    - [ ] [A4.3] Z tohoto modelu odvodit relační schéma (v 3NF).
    - [ ] [A4.4] Z téhož modelu odvodit alespoň dvě varianty grafového schématu.
    - [ ] [A4.5] Porovnat modely z hlediska čitelnosti, flexibility a předpokládaného výkonu pro typické dotazy.
  - [ ] **[A5] Syntéza a dokumentace**
    - [ ] [A5.1] Průběžně doplňovat a strukturovat poznatky v `Research/reserse_gdb_konceptualni_modely.md`.
    - [ ] [A5.2] Vytvořit přehledovou tabulku/diagram srovnávající různé přístupy a transformační pravidla.

- [ ] **Etapa B: Dotazník – žádanosti údajů a funkcí (do 31.7.2025)**
  - [ ] [B1] Vytvořit formulář dotazníku.
  - [ ] [B2] Distribuovat dotazník a sesbírat data.
  - [ ] [B3] Vyhodnotit data a prioritizovat funkcionality.

- [ ] **Etapa C: Implementace – nejžádanějších funkcionalit (do 30.9.2025)**
  - [ ] [C1] Navrhnout finální schéma GDB v Neo4j.
  - [ ] [C2] Vytvořit skript pro synchronizaci dat.
  - [ ] [C3] Naplnit databázi a implementovat základní dotazy.

- [ ] **Etapa D: Vyhodnocení (do 31.10.2025)**
  - [ ] [D1] Připravit scénáře a uspořádat uživatelské testování.
  - [ ] [D2] Zpracovat zpětnou vazbu.

- [ ] **Etapa E: Tvorba dokumentace a doporučení (do 30.11.2025)**
  - [ ] [E1] Napsat uživatelskou dokumentaci.
  - [ ] [E2] Zkompletovat metodiku transformace (výstup A2.4).
  - [ ] [E3] Zkompletovat text diplomové práce.

# Nedůležité
- [ ] nastavit clasp na OCI inatanci
- [ ] zprovoznit vývoj apps scripts na OCI instanci
