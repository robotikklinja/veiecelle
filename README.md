# Veiecelle

Veiecellen er en **Mettler Toledo IND9D56**.

Den drives av en tre faset 230V asynkronmotor og vekten på båndet blir regnet ut av fire mindre vekter på hvert av føttene til båndet. Det er også en liten modul under som regner ut hastigheten på båndet.

## Intro

Når vi åpnet kontrollboksen var ingen av jordlederene i styrestrømmen til kontrolleren koblet til.

Begge skinnene kontrollboksen satt på har blitt skrudd av slik at det er lettere å jobbe med boksen.

## Kontrollboksen

Det kommer inn 4 kabelenr til kontrollboksen.

- Datakabel Hvit (10 ledere + GND)
- Strømkabel (2-fas 230V + GND)
- Datakabel Sort (7 ledere, 6 tynnne, 1 tykk)
- Ukjent kabel (dato: 28/11/19)

### Datakabel Hvit (10-ledere + GND)

Denne kabelen har blitt tatt ut (se #kabeloversikt). Disse lederene gikk inn i settene med rekkeklemmer og jordlederen var skrudd ned i boksen.

Denne kabelen kommer fra noe ukjent som sitter under selve båndet.

### Strømkaben (2-fas 230V + GND)

Denne kabelen kommer i fra et støpsel og er strømforsyningen til kontrollboksen.

Disse lederene går inn i en rekkeklemme som videre går til et [230VAC -> 28VDC] PSU. Ut i fra rekkeklemmene går to ledere og en jordleder som skal skal til et ukjent koblingspunkt. Denne jordlederen er koblet til selve kontrollboksen, men fasene henger fritt.

### Datakabel Sort (7 ledere, 6 tynne, 1 tykk)

Denne kabelen kommer i fra de fire (vektene? ikke sikker) som står på hver fot på veiecellen.

Disse 7 lederene passer inn i `+EXC - -EXC` rekken på kontrollboksen.

## Ukjent Kabel

Denne kabelen har 10 ledere og en jord leder. Ingen av de andre kabelene i systemet har så mange ledere. Vi antar at denne kabelen tilhører noen sensorer som mangler på venstre siden av motoren. 

De to sensorene som står på høyre side av veiecellen skal ha to lasere som skal antageligvis lyse mot en sensor på andre siden.

Dette er nok for å unngå at objekter kjører av veiecellen.

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
