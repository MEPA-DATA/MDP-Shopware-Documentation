Artikel
=======

Artikel Synchronisieren
-----------------------

Um Artikel mit dem Shopware zu synchronisieren muss der Artikel auf dem UDF
«Shopware Sync» auf «Yes» gesetzt sein. Nur Artikel welche mit «Yes» markiert
sind, werden synchronisiert. Wird ein Artikel auf «No» gesetzt wird dieser nicht
erstellt oder aktualisiert. Dies betrifft auch das entfernen aus dem Shop. Für
das Entfernen aus dem Shop muss der Artikel entweder auf der SAP Business One
Maske auf «Inaktiv» gesetzt werden oder im UDF «Shopware Active» auf «No»
gesetzt sein.

Artikel im Shop anzeigen
------------------------

Um einen Artikel im Shop zu anzuzeigen, muss der Artikel synchronisiert sein. Es
müssen hierfür folgende Kriterien erfüllt sein:

-   Der Artikel muss zum synchronisieren markiert sein. Hierzu wird auf dem UDF
    «Shopware Sync» der Wert auf «Yes» gesetzt.

-   Der Artikel muss aktiv sein. Dies bedeutet, dass der Artikel in SAP Business
    One auf «Aktiv» gesetzt sein muss, plus das UDF Feld «Shopware Active» muss
    auf «Yes» gesetzt sein.

    Ist das erstere Feld auf «Inaktiv» gesetzt übersteuert dies das UDF
    «Shopware Active» und der Artikel wird bei der nächsten Synchronisation auf
    «Inaktiv» im Shop gestellt.

-   Der Artikel muss sichtbaren Shopware Kategorien zugewiesen sein.

-   Der Artikel muss einen Preis in den jeweiligen Shopware Preislisten haben.

-   Falls ein Freigabedatum («Shopware Release Time») gesetzt ist, muss dies
    verstrichen oder erreicht sein.

-   Wenn der Shop definiert hat, dass nur Artikel mit Lagerbestand angezeigt
    werden, muss ein Lagerbestand grösser 0 vorhanden sein. Der Lagerbestand ist
    je nach Konfiguration entweder der Lagerbestand der Shopware aktivierten
    Lager, der Lagerbestand – bestätigt Menge auf den Shopware aktivierten
    Lagern, oder eine individuelle Query Definition.

Artikel aus dem Shop entfernen
------------------------------

Um Artikel aus dem Shop zu entfernen muss dieser entweder auf der SAP Business
One Maske auf «Inaktiv» gesetzt werden oder im UDF «Shopware Active» auf «No»
gesetzt werden. Des Weiteren muss der Artikel mindestens bis nach der nächsten
Synchronisation das UDF «Shopware Sync» auf «Yes» gesetzt haben. Ist letzteres
nicht der Fall, wird der Artikel im Shop nicht aktualisiert.

Artikel Kategorien/Menüs im Shop zuweisen
-----------------------------------------

Um Artikel Kategorien zuzuweisen öffnet der Benutzer auf dem UDF «Shopware
Categories» den Kontextmenupunkt (rechte Maustaste) «Select Shopware
Categories».

Eine Tabelle mit 3 Spalten «Active», «Id», «Path» wird dargestellt. Dies sind
alle im Shopware verfügbaren Kategorien/ Menüs.

Um den Artikel einer bestimmten Kategorie zuzuweisen oder zu entfernen wir in
der Spalte «Active» der Hacken gesetzt oder entfernt. Wenn bereits Kategorien
dem Artikel zugewiesen wurden sind die Hacken für die jeweiligen Kategorien
bereits gesetzt.

Wird eine Änderung an der Selektion gemacht wechselt die Schaltfläche «OK» auf
«Aktualisieren». Um die Änderung zurück in die Artikelmaske zu schreiben,
klicken Sie auf «Aktualisieren» und dann auf «OK» auf derselben Maske. Mit OK
sollte die Maske geschlossen werden.

Des Weiteren muss danach der Artikel aktualisiert werden. Die Kategorien, werden
dann im UDF «Shopware Categories» mit deren «Id» und getrennt durch ein «;»
dargestellt.

Tipp: Für das vereinfachte suchen in den Kategorien, kann über das Textfeld
oberhalb der Tabelle innerhalb der Tabelle gesucht werden.

Lagerbestand mit Shop synchronisieren.
--------------------------------------

Falls gewünscht wird, dass der Lagerbestand mit dem Shop synchronisiert wird,
muss das UDF «Shopware Sync Stock» auf «Yes» gesetzt werden.

Der Lagerbestand ist je nach Konfiguration entweder der Lagerbestand der
Shopware aktivierten Lager, der Lagerbestand – bestätigt Menge auf den Shopware
aktivierten Lagern, oder eine individuelle Query Definition.

Artikel Freigabedatum im Shop setzten
-------------------------------------

Wenn gewünscht wird, dass ein Artikel erst von einem bestimmten Datum angezeigt
werden sollt, dann im Feld «Shopware Release Time» ein Freigabedatum gesetzt
werden. Um dieses wieder zu entfernen muss das Feld gelehrt werden.

Artikel Lieferzeit im Shop übersteuern.
---------------------------------------

Wir gewünscht, dass eine artikelspezifische Lieferzeit auf dem Shop dargestellt
werden soll, kann im UDF «Shopware Shipping Time» ein frei definierter Text
eingegeben werden z.B. «10 Tage». Dies übersteuert dann den im Shop definierten
Standard.

Artikelbeschreibung im Shop darstellen
--------------------------------------

Standardmässig wird die SAP Business One Artikel Beschreibung in den Shop
synchronisiert.

Artikelbeschreibung zweite Zeile im Shop darstellen.
----------------------------------------------------

Standardmässig wird als zweite Zeile die fremdsprachige Bezeichnung in den Shop
synchronisiert.

Artikeltext im Shop darstellen
------------------------------

Die Artikelbeschreibung wird standardmässig aus dem UDF «Shopware Item Text» in
den Shop synchronisiert. Dieses Feld kann einfachen Text oder HTML Code
enthalten.

Für das vereinfachte editieren von HTML Code kann auf dem UDF «Shopware Item
Text» im Kontext Menu (rechte Maustaste) der «MDP HTML Editor» aufgerufen
werden.

Dieser ermöglicht verschiedenste HTML Formatierungen auf den eingegebenen Text
anzuwenden.

**Achtung: Das kopieren und einfügen von bereits formatieren Text aus dritter
Quelle ist möglich, wird jedoch nicht empfohlen.**

Hersteller mit Shop synchronisieren
-----------------------------------

Innerhalb von Shopware kann der Hersteller als Filterkriterium oder als
Gruppierungseigenschaft genutzt werden.

Standardmässig wird das SAP Business One Feld «Hersteller» synchronisiert.

Artikelbilder und zusätzliche Dateien mit dem Shop synchronisieren
------------------------------------------------------------------

Das synchronisieren von Dateien mit Shopware wird über die Lasche «Anhänge»
gemacht.

Für das synchronisieren von Dateien wird auf die jeweilige Zeile der Anhänge
geklickt und das Feld «Shopware Sync» auf «Yes» gesetzt werden.

Bei Bilder kann auf einem Bild pro Artikel das Bild als Standardbild, mit dem
setzen des Hacken auf dem Feld «Shopware Default» unterhalb des Feldes «Shopware
Sync» in der Anhang Lasche, gesetzt werden. Dieses ist nur verfügbar wenn die
selektierte Zeile im Feld «Shopware Sync» auf der Anhang Lasche das Feld
«Shopware Sync» auf «Yes» gesetzt hat.

Externe Links mit dem Shop synchronisieren
------------------------------------------

Shopware ermöglicht das auflisten von externen Links. Hierzu wird im UDF
«Shopware Links» die jeweilige URL eingetragen. Wenn ein spezifischer Text,
anstatt der URL, für den Link gewünscht wird kann muss das Format
folgendermassen sein «TEXT\|URL». Wobei die Trennung ein «\|», Pipe ist. Dies
ist auf der «ch-de» Tastatur mittels der Tastenkombination «ALTGR» + «7»
verfügbar.

Bei der Eingabe von mehreren Links müssen diese jeweils auf einer eigenen Zeile
sein.

Minimale- / Maximale- / Schrittmenge für Bestellungen mit Shop Synchronisieren
------------------------------------------------------------------------------

Für das definieren einer minimalen Bestellmenge wird im UDF «Shopware Minimal
Order Quantity» die minimale Menge gesetzt, dies ist standardmässig «1».

Für das definieren einer maximalen Bestellmenge wird im UDF «Shopware Maximal
Order Quantity» die maximale Menge gesetzt, dies ist standardmässig «99»

Wenn zum Beispiel nur in zweier Schritten bestellt werden soll (2, 4, 6,…) kann
im UDF «Shopware Graduation Order Quantity» die Schrittmenge eingeben werden.
Z.B. mit der minimalen Menge auf «5» und er Schrittmenge auf 5, ist die im
Shopware verfügbare Mengenauswahl 5, 10, 15, …

Artikel von Versandkosten im Shop ausnehmen
-------------------------------------------

Wenn in Shopware Versandkosten definiert sind können einzelne Artikel generell
von den Versandkosten ausgenommen werden. Hierzu wird im UDF «Shopware Free
Shipping» das Feld auf «Yes» gesetzt. Der Artikel wird nun in der
Versandkostenberechnung nicht mehr in die Kalkulation einbezogen.

Artikel im Shop als hervorheben «Highlight»
-------------------------------------------

UDF «Shopware Highlight» auf «Yes» setzen.

Artikel im Shop als «On Sale» markieren
---------------------------------------

UDF «Shopware OnSale» auf «Yes» setzten.

Zubehör zu Artikel mit Shop synchronisieren
-------------------------------------------

Shopware ermöglicht das darstellen von Zubehörartikel. Um Artikel als Zubehör im
Shop darzustellen kann im UDF «Shopware Accessory» eine Liste von Artikelnummern
getrennt mit einem «;» (Semikolon) eingeben werden. Die Artikelliste kann auch
mittles der Artikelauswahl verfügbar über das Kontextmenu «Select Shopware
Accessory» gepflegt werden

Bei der Synchronisation wird werden die Zubehörartikel automatisch auf «Shopware
Sync» gesetzt und ebenfalls mit dem Shop synchronisiert.

**Achtung: Für die Darstellung im Shop müssen die selben Anforderungen wie für
reguläre Artikel erfüllt sein.**

Alternative Artikel mit Shop Synchronisieren
--------------------------------------------

Shopware ermöglicht das darstellen von ähnlichen Artikeln im Shop. Um Artikel
als ähnliche Artikel im Shop darzustellen müssen die alternativen Artikel in SAP
Business One innerhalb der Maske «Alternativartikel» gepflegt werden. Dies ist
über das Kontextmenu auf dem Artikel verfügbar.

Des Weiteren muss das UDF «Shopware Sync Alternative Items» auf «Yes» gesetzt
sein.

**Achtung: Für die Darstellung im Shop müssen die selben Anforderungen wie für
reguläre Artikel erfüllt sein.**

SEO Informationen mit Shop Synchronisieren
------------------------------------------

Für die bessere SEO Indexierung können in den UDF Feldern «Shopware META Title»,
«Shopware META Keywords», «Shopware Description» benutzt werden.

Das Feld «Shopware META Keywords» kann eine Liste von Suchbegriffen, getrennt
mit einem «,» (Komma) sein.

Verfügbar Menge im Shop übersteuern
-----------------------------------

Falls kein Lagerbestand synchronisiert wird oder Lagerbestand 0 ist kann im UDF
«Shopware Pseudo Quantity» die verfügbar Menge künstlich übersteuert werden.
Somit stellt der Shop trotz nicht vorhanden seins eines Lagerbestands einen
Bestand dar.

Um dies zu ignorieren wird der Wert auf «-99999» gesetzt. Hiermit wird die
Übersteuerung deaktiviert.

Spezialpreis im Shop darstellen
-------------------------------

Um einen Sonderpreis im Shop darzustellen (z.B. Sommerverkaufspreis) wird im UDF
«Shopware Pseudo Price» der gewünschte Preis eingegeben. Dieser wird dann im
Shop anstatt des regulären Preislistenpreis dargestellt. Des Weiteren wird im
falls der Shop ein Standardlayout die Ersparnis prozentual dargestellt.

Preise mit Shop synchronisieren
-------------------------------

Für die Synchronisation von Preisen müssen die jeweiligen Preislisten, welche
mit dem Shop synchronisiert werden sollen, in der Basiskonfiguration mit den
Preislisten von Shopware verknüpft sein.

Danach müssen nur noch die Preise in der jeweiligen Preisliste gepflegt werden.

Achtung: Artikel mit Preis 0 werden nicht dargestellt.

Artikel manuell mit Shopware synchronisieren
--------------------------------------------

Um Artikel nach Änderungen manuell zu synchronisieren kann der Benutzer entweder
über den manuellen Massenupload Hauptmenu: «MDP Shopware \> Items \> Upload
Items» zum Shop hochgeladen werden. Oder über das einzeln über den Artikelstamm.

Im Kontextmenu des Artikelstamms sind unter «Shopware Upload» die diversen
Upload Modelle verfügbar. Standardmässig sind 4 Modelle vorhanden. Diese können
kundenindividuell über die Konfiguration erweitert werden. Die Modelle
unterscheiden sich, welche Daten synchronisiert werden sollen.

Artikelübersetzungen mit Shopware synchronisieren
-------------------------------------------------

Übersetzungen werden über die Standard SAP Business One Funktion auf den
jeweiligen Feldern konfiguriert. Die verfügbaren Shop -Sprachen, -Shops müssen
in der MDP Shopware Basisinitialisierung den verfügbaren SAP Business One
Sprachen zugewiesen sein.

Übersetzungen sind für die Artikel Beschreibung, zweit Zeilen Text und den
Artikeltext (UDF «Shopware Item Text») verfügbar.

Nach dem Öffnen des Übersetzungsfensters, entweder über dem Kontextmenü auf dem
jeweiligen Feld, oder durch das anklicken des Übersetzungssymbols auf dem
jeweiligen Feld, wird in der Tabelle zuerst eine die gewünschte Sprache
ausgewählt und dann in der Spalte «Übersetzung» der gewünschte Text eingegeben.
Es ist möglich einfachen Text oder HTML Code einzufügen.

Für das vereinfachte eingeben von HTML formatierten Codes, kann über das
Kontextmenü der MDP HTML Editor aufgerufen werden.