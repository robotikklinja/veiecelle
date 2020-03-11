# Veiecelle

Veiecellen er en **Mettler Toledo IND9D56**.

Den drives av en tre faset 230V asynkronmotor og vekten på båndet blir regnet ut av fire mindre vekter på hvert av føttene til båndet. Det er også en liten modul under som regner ut hastigheten på båndet.

Veiecella og transportbåndet fungerer, men det gjenstår kalibrering av vektene for mer nøyaktige målinger og andre ting som kan finnes på roadmappen under "Projects".

Motorskiltet har følgende informasjon:
![](https://github.com/robotikklinja/veiecelle/blob/master/bilder/Motorskilt.png)

# Transportbåndet

Selve transportbåndet er en **Mettler Toledo model 9477**. Informasjon om den kan finnes i databrief dokumentene på [denne siden](https://kennedyscales.com/product/9477ind9d57/). Her er et bilde av skiltet på transportbåndet.

![](https://github.com/robotikklinja/veiecelle/blob/master/bilder/transportbaand_skilt.jpg)

## Intro

Da vi åpnet kontrollboksen var ingen av jordlederene i styrestrømmen til kontrolleren koblet til.

Begge skinnene kontrollboksen satt på har blitt skrudd av slik at det er lettere å jobbe med boksen.

## Veiecella

Det kommer inn 4 kabelenr til kontrollboksen.

- Datakabel Hvit (10 ledere + GND)
- Strømkabel (2-fas 230V + GND)
- Datakabel Sort (7 ledere, 6 tynnne, 1 tykk)
- Ukjent kabel (dato: 28/11/19)

## Kübler incremental encoder

Se mer informasjon om encoderen i dens datablad i pubs mappa. Her skal det forklares egenskapene av enkoderen i mer detalj. Enkoderen er av type 8.5000.D34W.2500.P0004.

Ifølge databladet gjelder følgende påstander:

- D: square flange, med IP65; tverrsnitt 63.5 mm
- 3: shaft med dimensjoner (ø x L): 10 x 20 mm
- 4: output circuit / power supply (RS422 (with inverted signal) / 5 V DC)
- W: koblings- og kabeltype (radial MIL connector, 7-pin)
- 2500: pulse rate

## Den andre enkoderen

Vi har ikke sett på enkoderen i mer detalj enn at vi fant ut hva den er for noe. Dens datablad står i pubs mappa.

## Ukjent Kabel

Denne kabelen har 10 ledere og en jord leder. Ingen av de andre kabelene i systemet har så mange ledere. Vi antar at denne kabelen tilhører noen sensorer som mangler på venstre siden av motoren. 

## Laser

Vi mangler reflekser til laserne, og dette er mer beskrevet i en issue laget av Jakob. Laserne er ennå ikke testet for å se om de i det hele tatt fungerer.  

## Kontrollboksen

Denne kontrollboksen inneholder motorkretsen og et kretskort. Kretskortet er en analog junction box og brukes til å samle inn signalene fra vektene og videre føre dem til selve veiecella.

## Motoren

Motoren er koblet opp, men vi tenker å se om den kan kontrolleres via veiecella. Hvis ikke, tenkte vi å koble opp en krets med en frekvensomformer, siden båndet går for fort med denne farten.
For å implementere frekevensomformeren og derav kontroll av hastighet må kabelen på motor byttes ut med en skjermet en. Her må også nippelen byttes ut med en EMC nippel, se issues.

## Kabeloversikt

Kabel som ble tatt ut som gikk til hver av rekkeklemmene i kontrollboksen (10 + GND)

| Kabel   | Rekkeklemme |
|---------|-------------|
| Rød     | 24V-1       |
| Hvit    | 0V-1        |
| Brun    | X1:1        |
| Lilla   | X1:2        |
| Rosa    | X1:3        |
| Orange  | X1:4        |
| Lys Blå | X1:5        |
| Grå     | X1:6        |
| Blå     | X2:1        |
| Grønn   | X2:2        |
| Gul     | X2:3        |
| Svart   | X2:4        |

## Frekvensomformer
![](https://github.com/robotikklinja/veiecelle/blob/master/bilder/Formel%20motoreffekt.jpg)

Ut ifra den generelle formelen for å beregne motoreffekt får vi en verdi på på 717W. Våre frekvensomformere har ikke stor nok effekt (375W). Det ble funnet en annen frekvensomformer med effekt på 750W fra Emerson. Denne kan benyttes, eventuelt kan vi bestille denne frekvensomformeren [her](https://www.beijerelectronics.com/en/Products/frequency-inverters/General___purpose___-___BFI___E3/BFI___E3___IP20/BFI-E3-12-0043-1F12)
