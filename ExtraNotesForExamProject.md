## Our Clustering
Hvad er "boldene" i dit projekt?
I dit tilfælde er "boldene" de forskellige lande i datasættet. Hver bold (eller land) har flere karakteristika, som f.eks.:

CO2-udslip (Total emissions)
Befolkningstal (Population)
BNP (GDP)
Gennemsnitstemperatur (Average annual temperature)
Disse karakteristika fungerer som egenskaber, der bruges til at afgøre, hvor tæt en "bold" (land) er på andre bolde, baseret på de værdier de har for disse egenskaber.

Hvordan ved vi, hvilke "bolde" der skal i hvilke kasser?
Du bruger KMeans clustering, som hjælper med at placere bolde (lande) i kasser (klynger) baseret på deres egenskaber. KMeans forsøger at finde den bedste måde at dele dine lande op i forskellige klynger, så de bolde, der ligner hinanden mest (f.eks. har lignende udslip, befolkning osv.), ender i samme klynge. KMeans gør dette ved at:

Tildele et centrum til hver klynge (en slags "midtpunkt" for en klynge).
Sammenligne hvert land (bold) med centrene og tildele det til den klynge, hvis centrum det er tættest på.
Flytte centrene rundt, indtil bolde er så tæt som muligt på deres klyngecentrum.
Hvordan bruges silhuet-scoren?
Silhuet-scoren hjælper os med at måle, hvor godt vores bolde (lande) passer i deres klynger. En høj silhuet-score (tæt på 1) betyder, at boldene passer godt ind i deres klynge og ikke ligner bolde i andre klynger. En negativ eller lav score betyder, at nogle bolde er tættere på en anden klynge, hvilket betyder, at de måske er placeret forkert.

I dit plot for silhuet-scoren kan vi se, at 2 og 3 klynger har de højeste scores, hvilket betyder, at 2 eller 3 klynger er det bedste antal, fordi boldene (lande) passer bedst i deres respektive kasser.

Hvad kan vi konkludere fra gennemsnittet?
Når vi ser på gennemsnittet af silhuet-scoren, kan vi konkludere, at det bedste antal klynger er der, hvor gennemsnittet er højest. I dit projekt ser det ud til, at 3 klynger er det bedste valg, fordi gennemsnittet for silhuet-scoren er højt, og det betyder, at dine bolde (lande) passer bedst i 3 kasser (klynger).

Hvis vi havde valgt et højere antal klynger, kunne flere bolde være blevet placeret forkert, hvilket ville have givet lavere scores og dårligere klynger.

Forudsigelsen med et nyt land
Når du prøvede at tilføje et nyt land og forudsige, hvilken klynge det tilhører, brugte du de samme egenskaber (CO2-udslip, befolkning osv.). KMeans sammenlignede dette lands egenskaber med dine eksisterende klynger og placerede det i den klynge, hvor det passede bedst (klynge 1, i dette tilfælde).

