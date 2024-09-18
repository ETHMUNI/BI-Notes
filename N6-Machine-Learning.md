## Machine Lerning Overblik
Link: https://cphbusiness.mrooms.net/pluginfile.php/1147613/mod_book/chapter/38467/N6-Machine%20Learning%20Intro.pdf

**Definition:**
* Machine Learning er en AI-teknologi, der bruges til at forudsige fremtidige resultater baseret på historiske data.

**Nogle eksempler:**
* Forudsigelse af vejret på en specifik lokation ud fra historiske data.
* Forudsigelse af, hvor meget en person vil kunne lide en film, baseret på deres vurderinger af tidligere set film.
* Forudsigelse af fremtidige salg og priser for et produkt.

**Grund ide:**
* Et program lærer fra observerede data og bruger denne læring til at lave forudsigelser i nye, uobserverede situationer.

## Machine Learning Fundament

**Matematisk repræsentation:**
* ML søger at afdække en ukendt funktion F() ved at forbinde input (features) til output (labels):
  * Output = F(Input)

**Formål:**
* Målet er at opdage denne funktion og bruge den til at lave præcise forudsigelser i fremtiden.

**ML-algoritmer:**
* Algoritmer bruges til at udtrække mønstre fra data, så computeren kan foretage forudsigelser og drage informative gæt på baggrund af disse.

## Typer af Machine Learning
**Supervised Learning (overvåget læring):**

* Systemet trænes med data, hvor labels (output) allerede er kendt.
* To hovedopgaver inden for supervised learning:
  * **Classification (klassifikation):**
    * Her tildeles data en foruddefineret kategori eller klasse (kvalitativ værdi). Fx om en email er spam eller ej.
  * **Regression:**
    * Bruges til at forudsige en ny, ukendt kvantitativ værdi. Fx forudsigelse af boligpriser.
   
  
**Unsupervised Learning (uovervåget læring):**

* Data bruges uden kendte labels, og algoritmen opdager selv strukturer i data.
* En typisk opgave er:
  * Clustering: Her grupperes data i nye, udefinerede grupper. Det bruges fx til kunde-segmentering.
 
## Machine Learning-processen

**Dataindsamling:**
* Saml de relevante data fra forskellige kilder.

**Data Pre-processing (forbehandling):**
Rens og forbered dataene, så de er klar til modellering. Det kan inkludere behandling af manglende data, fjernelse af outliers osv.

**Training (træning):**
* Træn modellen på en del af dataene (train-sættet) for at identificere mønstre og lære af dem.

**Testing (testning):**
* Test modellen på en anden del af dataene (test-sættet) for at vurdere dens præstation.

**Evaluation (evaluering):**
* Vurder modellens nøjagtighed og juster den efter behov.

**Deployment (implementering):**
* Efter modellen er blevet valideret, kan den implementeres og bruges til at forudsige nye, ukendte data.

## Bygning af en Machine Learning Model
**Dataindsamling:**
* Start med at indsamle data, der skal bruges i modellen.

**Visualisering af data:**
* Lav forskellige visualiseringer for at få indsigt i dataenes fordeling og mønstre.

**Dataforberedelse:**
* Forbered dataene ved at splitte dem op i et train-sæt og et test-sæt.

**Træning af modellen:**
* Brug train-sættet til at lære modellen at forudsige resultater.

**Testning af forudsigelser:**
* Brug test-sættet til at se, hvor godt modellen præsterer på ukendte data.

**Validering:**
* Valider modellen ved at bruge nye, ukendte data og vurder, hvor godt modellen generaliserer.
<img width="1098" alt="Skærmbillede 2024-09-18 kl  10 57 09" src="https://github.com/user-attachments/assets/cf08997e-1fa6-472e-9dbf-ccee325d2db3">
