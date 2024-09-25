Link: https://cphbusiness.mrooms.net/pluginfile.php/1147608/mod_book/chapter/37651/N5-Regression.pdf

## Regression

* Regression er en statistisk metode, der bruges til at bestemme styrken og karakteren af forholdet mellem en afhængig variabel (Y) og en eller flere uafhængige variabler (X).
* Anvendes til at forudsige output baseret på kendte input.

Historisk oprindelse: Regressionsbegrebet stammer fra Sir Francis Galtons observation i 1885 om, at børns højder tendensmæssigt var tættere på gennemsnittet end deres forældre, et fænomen, han kaldte "regression mod middelværdien".

## Typer af Analyse

**Exploratory Analysis:** Forklarer, hvad der er sket baseret på eksisterende data, f.eks. ved at finde korrelationer.

**Predictive Analysis:** Skaber modeller til at forudsige fremtidig adfærd, f.eks. ved at bruge korrelationer til at forudsige fremtidige observationer.

## Lineær Regression

* Modellen bruger en best-fitting line til at forudsige, hvordan X påvirker Y.
* Y = b*X + a (hvor b er hældningen, og a er skæringspunktet).
* Målet er at minimere fejl (forskellen mellem forudsagte og observerede værdier).

## Best Fitting Line

**Fejlminimering:** Find den linje, der minimerer summen af fejlene mellem de faktiske datapunkter og den forudsagte værdi.
  * Almindelige metoder inkluderer at minimere summen af absolutte fejl eller kvadrerede fejl.

## Model Validation

**Gradient Descent:** En optimeringsalgoritme, der iterativt justerer parametre (a og b) for at finde den bedste fitting linje.

**R-squared:** En måling af, hvor tæt data er på regressionlinjen (1 = perfekt model).
  * Højere R-squared værdi indikerer bedre modelpræcision.

## Flere Typer af Regression

**Multiple Linear Regression:** Modeller med flere uafhængige variabler.
  * Y = a0 + a1X1 + a2X2 + ... + an*Xn.

**Non-linear Regression:** Bruges, når forholdet mellem X og Y ikke er lineært (f.eks. kvadratisk, eksponentiel, logaritmisk).

**Polynomial Regression:** Modeller, hvor forholdet mellem variabler er et polynomium af højere grad.

## Overfitting vs. Underfitting

**Overfitting:** Modellen passer for godt til træningsdata og har svært ved at generalisere til nye data.

**Underfitting:** Modellen er for simpel og kan ikke forklare dataene tilstrækkeligt.

## Fordele ved Regression

* Simpelt og let at forstå.
* Kræver relativt få ressourcer og er hurtig at træne.
* Velegnet til kvantitative variabler og situationer uden mange outliers.

## 
