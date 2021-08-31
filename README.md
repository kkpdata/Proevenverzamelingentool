# Inleiding

Door Hoogheemraadschap Hollands Noorderkwartier, Hoogheemraadschap Delfland en Waterschap Rivierenland is een proevenverzamelingentool (ook wel STOWA database genoemd) geïnitieerd en verder ontwikkeld.
De proevenverzamelingentool bestaat uit een tool in Excel om proevenverzamelingen samen te stellen. De onderliggende data om een proevenverzameling samen te stellen is beschreven in een vaste structuur. Deze structuur is vastgelegd in een uitwisselformat.

Deze proevenverzamelingentool en uitwisselformat versie 4.2k is nu beschikbaar. De geotechnische laboratoria kennen deze database en kunnen deze database vullen met resultaten van grond- en laboratoriumonderzoek. Op deze wijze ontstaat er een eerste uniformering op het gebied van data-uitwisseling en –opslag van proefresultaten.

Met de gevulde proevenverzamelingentool is het mogelijk om proevenverzamelingen op te zetten en te analyseren. Op basis van een set proeven leidt het Excel sheet zowel gedraineerde als ongedraineerde schuifsterkte parameters af. Van deze parameters worden verwachtingswaarde, karakteristieke waarde en rekenwaarde bepaald. De bestanden worden "as is" beschikbaar gesteld. De verantwoordelijkheid voor het gebruik van deze tools ligt bij de gebruiker.

De proevenverzamelingentool stond voorheen op de helpdesk water.

# Omvang

De proevenverzamelingentool bestaat uit een verzameling bestanden. Naast deze toelichting bestaat de complete set uit de volgende bestanden:

* Proevenverzamelingen_tool_v4.2l.xlsm
* Beschrijving van deze proevenverzamelingentool
* Het uitwisselformat-database-proevenverzameling_versie_4_2l.xlsx
* Toelichting bij Uitwisselformat-database-proevenverzameling_versie_4_2l_202105.pdf

# Wijzigingen uitwisselformat ten opzichte van voorgaande versie

De huidige versie 4.2 is inmiddels aangekomen bij subversie l. 

Ten opzichte van versie 4.2k zijn de volgende wijzigingen in versie 4.2l doorgevoerd:

* De naamgeving van een aantal velden in de databasestructuur zijn aangepast om het uitwisselformat geschikt te maken voor gebruik met NEN-EN-ISO 14688-1:2019+NEN 8990:2020 nl, naast de NEN5104:1989 nl.De aanpassing betreft de kolommen die een verwijzing bevatten naar de NEN5104. "_NEN5104" is vervangen door "_GRONDSOORT". "_NEN5104_BIJMENGING" is vervangen door "_OVERIGE_BESTANDDELEN". Dit is toegepast op de classificatie (groepcode CLAS), korrelverdelingen (groepcode KV), de CRS-proeven (groepcode CRS), de samendrukkingsproeven (groepcode SD) en de DSS en triaxiaalproeven (groepcodes DSS resp. TXT). Zie "Aanwijzingen voor het beschrijven van de grond bij verschillende normen".


Ten opzichte van versie 4.2h zijn de volgende wijzigingen in versie 4.2k doorgevoerd:

* Helpdeskvraag #18 04 2230: er is geen match tussen velden uitwisselformat en proevenverzamelingentool. De proevenverzamelingentool geeft de juiste velden weer.
   oplossing: velden zijn aangepast in uitwisselformat zodat ze overeenkomen met proevenverzamelingentool.
* Helpdeskvraag #18 04 2230 Match tussen uitwisselformat en velden proevenverzamelingentool. Het uitwisselformat is aangepast zodat de volgorde en naamgeving van de velden overeenkomen. Dit geldt ook voor de omschrijving van de velden.
* Kolomnummers 368 t/m 370 hebben geen betekenis en zijn per abuis opgenomen in de database. De omschrijving bij deze namen is aangepast en de velden hoeven niet ingevuld te worden. Om de impact te verkleinen is alleen de omschrijving aangepast, velden blijven onderdeel uitmaken van het uitwisselformat.
* De omschrijving van het monsterniveau per proef is aangepast. Met het monsterniveau wordt het niveau bedoeld van het hart/midden van het proefstuk bedoeld. Dit niveau ligt ten opzichte van m NAP en tussen de bovenkant en onderkant van de monsterbuis.
* De eenheid van de kolom 70, CLAS_AT_PI Plasticiteitsindex is aangepast naar procenten [%] omdat dit in lijn is met de gebruikelijke eenheid van deze parameter
* In kolom 50 (CLAS_NEN5104_BIJMENGING) wordt gevraagd om de beschrijving van de bijmengingen behorend bij de classificatie conform de NEN5104. Met bijmenging wordt normaliter een toevoeging bedoeld, zoals bijvoorbeeld 'zwak siltig'. Omdat de bijmenging ook al wordt gevraagd in kolom 49 (CLAS_NEN5104), was het onduidelijk wat met kolom 50 ‘bijmengingen’ bedoeld wordt. Bedoeld wordt bijzondere bestanddelen (zoals puin, plantenresten etc.). De beschrijving en de naamgeving van de kolom is aangepast.

# Wijzigingen proevenverzamelingentool

De huidige versie van de proevenverzamelingentool is versie 4.2l. 

Ten opzichte van de vorige versie (4.2k) zijn de volgende wijzigingen doorgevoerd in versie 4.2l:

* De naamgeving van een aantal velden in de databasestructuur zijn aangepast om het uitwisselformat geschikt te maken voor gebruik met NEN-EN-ISO 14688-1:2019+NEN 8990:2020 nl. Zie de toelichting bij de wijzigingen in het uitwisselformat.


Ten opzichte van versie 4.2h zijn de volgende wijzigingen doorgevoerd:

* In een aantal gevallen bleek het mogelijk dat niet-unieke monsterid werden aangemaakt. Een unieke ID is nodig voor de functionaliteit. Dit is opgelost door het regelnummer toe te voegen aan het monsterid.
* Bug verholpen indien de proevenverzamelingentool wordt gebruikt in Office365. De tool werkt nu voor de nederlandse en engelse versies van de formules.
* De berekening van het veld ANA_TXT_CONSOLIDATIE_TYPE en ANA_DSS_CONSOLIDATIE_TYPE is aangepast zodat een kleine afwijking van normaal geconsolideerde proeven ook als NC proef worden bestempeld.
* De berekening van de karakteristieke waarde van de gedraineerde parameters is aangepast aan de methode in de schematiseringshandleiding macrostabiliteit.
* De naamgeving van de database velden en beschrijving is consistent gemaakt met het uitwisselformat.
* In versie 4.2k2 is een probleem opgelost waarbij de tool vastliep bij herberekening indien een punt als decimaalteken was ingesteld in Excel.

# Aanwijzingen voor het beschrijven van de grond bij verschillende normen

Het uitwisselformat is geschikt om zowel grondbeschrijvingen conform NEN5104:1989 nl als NEN-EN-ISO 14688-1:2019+NEN 8990:2020 nl te bevatten. Overeengekomen is dat kolom 47 (CLAS_NORMEN) een hoofdrol vervult in het uitwisselen van informatie. 
Hiermee kan de hele STOWA sheet voorts onveranderd blijven t.o.v. versie 4.2K, zonder nieuwe kolommen of andere volgordes of wijzigingen, behalve dat enkele kolomtitels (louter tekstueel) aangepast zijn door verwijzingen naar NEN5104 te vervangen door een generieke naamgeving.

De waardelijst voor kolom 47 (CLAS_NORMEN) is:

- ‘NEN5104:1989 nl’
- ‘NEN-EN-ISO 14688-1:2019+NEN 8990:2020 nl’

Voor kolommen met "_GRONDSOORT" gelden de volgende aanwijzingen:

1. Bij gebruik NEN5104:1989 nl voor de beschrijving van de grond de codering gebruiken, niet geheel uitschrijven. Bijvoorbeeld: Ks2 of Vm of Ks3h1
2. Bij gebruik conform NEN-EN-ISO 14688-1:2019+NEN 8990:2020 nl de waardelijst 7.41 gebruiken van https://docs.geostandaarden.nl/bro/def-im-BHR-GT-20200325/

Voor kolommen met "_OVERIGE_BESTANDDELEN" gelden de aanwijzingen:

3. Bij gebruik NEN5104:1989 nl de uitgeschreven tekst gebruiken.
4. Bij gebruik conform NEN-EN-ISO 14688-1:2019+NEN 8990:2020 nl de waardelijst 7.76 gebruiken van https://docs.geostandaarden.nl/bro/def-im-BHR-GT-20200325/


# Issues en vragen

Vragen of issues over de werking van de proevenverzamelingentool en het uitwisselformat kunnen gesteld worden door een issue aan te maken in Github. Overige vragen met betrekking tot overige analysetools en/of statistiek binnen het domein van waterkeringen kunnen gesteld worden via de Helpdesk Water.
