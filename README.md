# Schnellanfrage
Einbinden eines Schnellanfrage-Formulares zum Übergeben einer Anfrage an den AnfrageAssistent4you.

### Daten

| Name | Beschreibung | `<input name="aa4y_*" >` |
|:-----|:-------------|:--------|
|Anreise| Datum der Anreise | anreise |
|Abreise| Datum der Ebreise |  abreise |
|Zimmer| Anzahl der Zimmer |  zimmer |
|Erwachsene| Anzahl der mitreisenden Erwachsenen |  erwachsene |
|E-Mail| E-Mail Adresse des Gastes | email|

### Weitere Felder

| Name | Beschreibung | `<input name="aa4y_*" >` |
|:-----|:-------------|:--------|
|URL| Url zur Weiterleitung bei Eingabe-Fehlern | url |
|Betrieb| ID des Betriebes |  betrieb |
|Sprache| Sprache des Gastes, Sprache der Fehlermeldungen |  sprache |
|Format| Formatierung der Datumseingaben |  form_datum |

Die Daten werden per POST oder GET an https://live.anfrageassistent4you.com/api/request.php versendet. 
Ist eine Angabe nicht korrekt, wird z.B. über `aa4y_fehler_anreise` der Fehler ausgegeben und über `aa4y_anreise` der Inhalt (value) übertragen.

Die CSS-Stile sind frei anpassbar.

### Optionale Felder

| Name | Beschreibung | `<input name="aa4y_*" >` |
|:-----|:-------------|:--------|
|Geschlecht| Geschlecht (m/f) | geschelcht |
|Name| Nachname des Gastes |  name |
|Vorname| Vorname des Gastes |  vorname |
|Adresse| Straße und Hausnummer des Gastes |  adresse |
|PLZ| PLZ des Gastes |  plz |
|Ort| Wohnort des Gastes |  ort |
|Land| Land des Gastes |  land |
|Telefon| Telefonnummer des Gastes |  telefon |
|Fax| Faxnummer des Gastes |  fax |

Wenn Sie komplexere Belegungsvaranten übergeben möchten, können sie die Belegung für bis zu drei Zimmer und je bis zu vier Kinder wie folgt übergeben:

Anzahl der Erwachsenen im ersten Zimmer:`<input name="aa4y_1_erwachsene" >`

Alter des ersten Kindes im ersten Zimmer: `<input name="aa4y_1_1_alter" >`
Alter des zweiten Kindes im ersten Zimmer: `<input name="aa4y_1_2_alter" >`

Sie können das Alter des Kindes sowohl als Alter in Jahren als auch als Geburtsjahr übergeben.

#### Sprache

Sie können `de`für Deutsch, oder `en`für Englisch übergeben.

#### Format

Das Datum wird im Format d.m.Y übertragen. Andere Formate können über das Feld form_datum übergeben werden. Richten Sie sich bitte bei der Angabe des Datumsformat nach der Parameter-Liste unter http://php.net/manual/de/function.date.php.

## Impressum

**LSL OG**<br>
Schmiedau 1<br>
6272 Kaltenbach / Zillertal<br>

Tel.: +43 720 880563<br>

Firmenbuchnummer: FN 420310 d<br>
UID-Nr. ATU69074039<br>
Gerichtsstand: Bezirksgericht Zell am Ziller<br>

Schuster Hannes, Geschäftsführung<br>
office@anfrageassistent4you.com<br>
+43 676 3314900<br>

Andreas Lechner, Vertrieb<br>
vertrieb@anfrageassistent4you.com <br>
+49 172 176 5348<br>

Jascha Lemburg, Support<br>
technik@anfrageassistent4you.com<br>
+43 720 880563
