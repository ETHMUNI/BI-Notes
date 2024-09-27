Link https://cphbusiness.mrooms.net/pluginfile.php/1147613/mod_book/chapter/38541/N7-Classification.pdf

## Classification vs Regression

**Classification:** En maskinlæringsopgave, hvor data opdeles i foruddefinerede klasser. Bruges til at forudsige, hvilken klasse ny data tilhører.

**Regression:** Skaber en model, der bedst passer til dataene, ofte til at forudsige kontinuerlige værdier.

**Eksempler på classification:**
* Forudsigelse af kundens valg
* Billedgenkendelse
* Medicinske diagnoser

## Decision Tree Algorithm

**Decision Tree:** En hierarkisk struktur med beslutningskriterier, bestående af:
* **Nodes:** Indeholder regler, der driver beslutninger.
* **Branches:** Forbinder noderne.
* **Leaves:** Ender i anbefalede resultater.
* **Root node:** Øverst, hvor hele datasættet starter. Hvert niveau splitter datasættet i mindre undergrupper.
* **Entropy:** Måling af usikkerhed eller uorden i et system.
* **Information Gain:** Mængden af information opnået ved at observere en variabel.

## ID3 Decision Tree Algorithm

* Algoritmen bygger et træ ved at vælge attributter med maksimal information gain.
* Trinnene involverer at beregne entropi, opdele datasættet og vælge de mest nyttige attributter til at skabe grene i træet.
  * Entropi i en klassifikation: du har et datasæt, hvor du skal klassificere elementer i forskellige kategorier. Hvis alle     elementer tilhører én kategori, er entropien lav, da der er meget lidt usikkerhed. Men hvis elementerne er ligeligt fordelt på tværs af      mange kategorier, er entropien høj, fordi der er stor usikkerhed om, hvilken kategori et nyt element vil tilhøre
* Træet bruges derefter til at forudsige resultater baseret på nye data.

## Naïve Bayes Algorithm

**Bayes Theorem:** Beregner sandsynligheden for en begivenhed baseret på tidligere viden om forholdet mellem hændelser.
* Anvendes i klassifikation, hvor vi beregner sandsynlighederne for forskellige klasser og vælger den mest sandsynlige klasse.
  * Fordele: Hurtig og effektiv, særligt velegnet til flerklasse-forudsigelser.
  * Ulemper: Forudsætter uafhængige prædiktorer, hvilket kan være urealistisk i virkelige data.
    * Eksempel på ulempe: Hvis man klassificerer emails som spam eller ikke-spam, kan visse ord ofte forekomme sammen (f.eks. "gratis" og          "tilbud"). Hvis Naïve Bayes-algoritmen antager, at disse ord er uafhængige, kan det føre til fejl i klassificeringen, fordi algoritmen       ikke tager højde for deres korrelation
 
## Validation of Predictions

**Confusion Matrix:** Bruges til at måle modelkvalitet ved at sammenligne forudsigelser og faktiske observationer.

**Precision, Recall, og F1-score er målinger af modelnøjagtighed:**
* Precision: Hvor mange af de forudsagte positive eksempler er korrekte?
* Recall: Hvor mange af de faktiske positive eksempler blev korrekt identificeret?
* F1-score: Den harmoniske gennemsnit af precision og recall.
