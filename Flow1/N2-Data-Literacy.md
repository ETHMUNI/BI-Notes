## Data Literacy (Datalæsefærdigheder)
**Definition:** Evnen til at udforske, forstå og kommunikere med data.

**Eksempel:** Du skal analysere salgsdata fra en butik. Data literacy betyder, at du ved, hvordan du fortolker dataene og forklarer, hvad de betyder.

## Typer af Data
**Quantitative Data:** Numeriske værdier (f.eks. alder, temperatur).
  * Diskret: Hele tal (f.eks. 1, 2, 3).
  * Kontinuerlig: Kan have decimaler (f.eks. 1,1; 1,11).

**Qualitative Data:** Kategoriske data (f.eks. farver, madtyper).
  * Ordinal: Kan rangeres (f.eks. god, bedre, bedst).
  * Nominal: Ingen rang (f.eks. mand, kvinde).

**Eksempeler:**
Quantitative: Måling af vægten af produkter (f.eks. 10 kg, 20 kg).
Qualitative: Oplistning af lande (f.eks. USA, Danmark, Japan).

## Datakvalitet
**Betydning:** Dårlige data giver dårlige resultater ("garbage in, garbage out").

**Faktorer:**
  * **Volumen:** Jo flere data, jo større er chancen for at opdage mønstre og træffe præcise beslutninger. Et stort datagrundlag gør det lettere at identificere trends og reducere tilfældige fejl.
    * Eksempel: Hvis du kun har data fra én dags salg i en butik, kan det være svært at se et mønster. Hvis du har data fra hele året, bliver mønstrene tydeligere.
  * **Konsistens:** Data skal være konsistente over tid og på tværs af kilder. Hvis der er store forskelle eller uoverensstemmelser mellem nye og gamle data, kan det skabe forvirring og fejlanalyse.
    * Eksempel: Hvis du registrerer produktpriser i forskellige valutaer, men ikke konsekvent omregner dem til en fælles valuta, vil det føre til inkonsistens i dataene

## Dataindsamling og Forbehandling
**Data Wrangling:** Omformning af rå data til et brugbart format. (JSON, XML, Excel, CSV osv.)

**Eksempel:** indsamlling af salgsdata fra flere forskellige kilder: en CSV-fil fra en leverandør, JSON-data fra en webbutik og Excel-ark fra butikspersonalet. Hver kilde har en anden struktur. Data Wrangling vil være processen, hvor du omformer, renser og kombinerer disse data i et konsistent format, så du kan analysere dem samlet, f.eks. ved at standardisere valutaenheder eller formatere datoer på samme måde.

## Data Cleaning
**Definition:** Fjernelse eller korrektion af forkerte data (f.eks. dubletter, manglende værdier).

**Dubletter (Duplicate Data)**
* Problem: Hvis et datasæt indeholder gentagne poster (f.eks. samme kunde registreret flere gange), kan det skævvride resultaterne.
* Løsning: Find og fjern dubletter. Det kan gøres ved at identificere poster med samme information (f.eks. samme kundens ID, navn eller email), som gentages unødvendigt.

**Manglende værdier (Missing Data)**
* Problem: Data kan mangle i visse felter, hvilket kan gøre det svært at analysere korrekt. F.eks. kan et felt som "alder" eller "indkomst" mangle for nogle kunder.
* Løsninger: Der er flere måder at håndtere manglende data på:
  * Sletning af rækker eller kolonner: Hvis data mangler i mange poster, kan det være nødvendigt at slette dem.
  * Udfyldning: Hvis kun få data mangler, kan man udfylde de manglende værdier med f.eks. gennemsnittet, medianen eller en skønnet værdi.

 NOTE: Der er flere almindelige problemer i rå data. Ovenover er bare de typiske.

## Håndtering af Manglende Data
**Metoder:**
* Udfyld med gennemsnittet eller medianen.
* Erstat med en omtrentlig værdi.

**Eksempel:** Hvis temperaturen for en dag mangler i et vejrdata-sæt, kan du udfylde den manglende værdi med gennemsnitstemperaturen for måneden.

## Outliers (Atypiske Værdier)
**Definition:** Datapunkter, der er langt fra resten. Du skal vuderer om outlieren er en værdi er en reel observation eller en fejl.

**Hvordan håndteres de:** Identificer dem og beslut, om de skal fjernes eller beholdes baseret på deres indvirkning på analysen.

**Eksempel:** Hvis en butik rapporterer 10 millioner kr. i salg på én dag, hvor gennemsnittet er 100.000 kr., kan det være en outlier på grund af en rapporteringsfejl.

## Data Restructuring
**Pivoting:** Omformning af kolonner til rækker for at organisere dataene bedre.

**Eksempel:** Hvis du har salgsdata efter produkt og måned, kan du pivotere dataene, så hver måned bliver en separat kolonne til sammenligning



  
