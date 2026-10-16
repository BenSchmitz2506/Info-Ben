---
marp: true
paginate: true
style: |
  /* ==============================================================
     Vorlage für Marp
     Diese Datei ist dein Gerüst. Ändere Werte, niemals die Namen
     der Klassen – die müssen zum Text passen, sonst passiert nichts.

     Wichtig: Diese Vorlage nutzt HTML (<div class="...">). Marp
     blockiert das standardmäßig. Aktiviere HTML:
       - VS Code: Einstellung "markdown.marp.enableHtml"
       - Marp CLI: Option --html
     ============================================================== */

  /* --- Die Farben ------------------------------------------------
     Jede Farbe steht genau einmal hier. Alle Klassen weiter unten
     benutzen nur noch den Namen. Willst du das Aussehen ändern,
     änderst du nur diese sieben Zeilen – nicht die Klassen. */

  :root {
    --blau:      #17324d;   /* Titel, Balken, Linien */
    --blau-hell: #24527a;   /* Akzente, Rand der Karten */
    --flaeche:   #f7f9fc;   /* Hintergründe von Kästen */
    --flaeche-2: #edf5fb;   /* zweiter Hintergrundton */
    --flaeche-3: #e8f1f8;   /* dritter Hintergrundton */
    --flaeche-4: #eef5f9;   /* Karten */
    --gelb:      #f4d35e;   /* Hervorhebung */
  }

  /* --- Die Folie selbst ------------------------------------------
     Jede Folie wird zu einem <section>. Alles hier gilt für alle. */
  section {
    display: flex;
    flex-direction: column;
    align-items: center;
    min-height: 100%;
    padding: 40px;
    font-family: Arial, Helvetica, sans-serif;
  }

  /* --- Der Folientitel ------------------------------------------- */
  .titel {
    width: 100%;
    text-align: center;
    color: var(--blau);
    margin-bottom: 24px;
  }

  /* --- Eine einfache Liste --------------------------------------- */
  .liste {
    width: 80%;
    padding: 18px 24px;
    background: var(--flaeche);
    border-left: 6px solid var(--blau);
    text-align: left;
  }

  /* --- Ein hervorgehobener Satz ---------------------------------- */
  .merksatz {
    width: 80%;
    margin-bottom: 20px;
    padding: 20px;
    background: var(--gelb);
    font-weight: bold;
    border-radius: 20px;
    text-align: left;
  }

  /* --- Ein einzelner Kasten -------------------------------------- */
  .box {
    width: 80%;
    padding: 18px 24px;
    background: var(--flaeche-2);
    border-left: 6px solid var(--blau);
    text-align: left;
  }

  /* --- Zwei Spalten: legt die Aufteilung fest -------------------- */
  .grid-2 {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 24px;
    width: 100%;
  }

  /* Spaltenverhältnisse zum Ausprobieren:
       1fr 1fr  -> zwei gleich breite Spalten
       2fr 1fr  -> links doppelt so breit wie rechts
       1fr 2fr  -> rechts doppelt so breit wie links               */

  /* Eine breite und eine schmale Spalte:
     .grid-2 { grid-template-columns: 2fr 1fr; align-items: center; } */

  /* --- Die Spalte: nur das Aussehen ------------------------------ */
  .spalte {
    padding: 18px;
    background: var(--flaeche-3);
    border-radius: 14px;
    text-align: left;
  }

  /* --- Karten: drei Dinge nebeneinander -------------------------- */
  .karten {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 18px;
    width: 100%;
  }

  .karte {
    min-height: 150px;
    padding: 16px;
    background: var(--flaeche-4);
    border-top: 5px solid var(--blau-hell);
    text-align: left;
  }

  /* --- Bilder ---------------------------------------------------- */
  .bild {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
  }

  .bild img {
    width: 320px;
    height: auto;
  }

  /* --- Die Fußzeile ---------------------------------------------- */
  .fusszeile {
    width: 100%;
    margin-top: auto;
    padding-top: 12px;
    border-top: 1px solid var(--blau);
    text-align: center;
    font-size: 0.6em;
  }
---

<div class="titel">

# Passwortmanager

</div>

<div class="liste">

- Heutige Bedeutung: Warum sind sichere Passwortmanager gerade jetzt wichtig?
- Leitfrage und Ziel: Mein Ziel ist es zu erklären, wie Passwortmanager unsere Konten schützen und warum sie nützlich sind.
- Name: Ben Jansweidt
- Klasse: 9a
- Datum: 

</div>
<!--
Warum Passwortmanagergerade jetzt wichtig sind?
Mein Ziel ist es zu erklären, wie Passwortmanager unsere Konten schützen und warum sie nützlich sind.
-->

<div class="fusszeile">
  
</div>

---

<div class="titel">

# Welche wichtigen Funktionen kann ich kostenlos nutzen?

</div>

<div class="liste">

-  Unbegrenzt viele Passwörter speichern 
-  Auf mehreren Geräten synchronisieren
-  Automatisches Ausfüllen
-  Sichere Passwörter generieren 
-  Passkeys speichern und verwenden 
-  Schwache oder wiederverwendete Passwörter erkennen 

</div>
<!--
-  Unbegrenzt viele Passwörter speichern 
-  Auf mehreren Geräten synchronisieren
-  Automatisches Ausfüllen
-  Sichere Passwörter generieren 
-  Passkeys speichern und verwenden 
-  Schwache oder wiederverwendete Passwörter erkennen 
-->
<div class="fusszeile">
  
</div>

---

<div class="titel">

# Vor-& Nachteile eines Passwortmanagers

</div>

<div class="grid-2">
  <div class="spalte">

  **Vorteil**

  -  Mehr Sicherheit
  -  Keine Passwörter merken
  -  Schutz vor Passwort-Wiederverwendung

  </div>
  <div class="spalte">

  **Nachteil**

  -  Ein zentraler Angriffspunkt
  -  Teilweise kostenpflichtig
  -  Abhängigkeit von der Software

<!--

**Vorteil**

  -  Mehr Sicherheit
  -  Keine Passwörter merken
  -  Schutz vor Passwort-Wiederverwendung
  **Nachteil**

  -  Ein zentraler Angriffspunkt
  -  Teilweise kostenpflichtig
  -  Abhängigkeit von der Software
-->
  </div>
</div>

<div class="fusszeile">
  
</div>

---

<div class="titel">

# Unterschiede Kostenpflichtige und Kostenlose Version

</div>

<div class="grid-2" style="grid-template-columns: 2fr 1fr; align-items: center;">
  <div class="spalte">

  **Unterschiede**

  -  Kosten
  -  Sicherheitsfunktionen
  -  Zusatzfunktionen
  

  </div>
  <div class="spalte">

  **Gleichheiten**

  - Passwörter sicher speichern
  - Passwörter automatisch ausfüllen
  - Sichere Passwörter erstellen

<!--
**Unterschiede**

  -  Kosten
  -  Sicherheitsfunktionen
  -  Zusatzfunktionen
   **Gleichheiten**

  - Passwörter sicher speichern
  - Passwörter automatisch ausfüllen
  - Sichere Passwörter erstellen
-->
  </div>
</div>
<!--

<div class="fusszeile">
  
</div>

---

<div class="titel">

# Drei Passwortmanager im Überblick

</div>

<div class="karten">
  <div class="karte">

  **Bitwarden**

  - Kostenmodell: Kostenlos und kostenpflichtig
  - Quellcode: Open Source
  - Unterschiede: Günstig und mit einfacher Synchronisierung.

  </div>
  <div class="karte">

  **1Passwort**

  - Kostenmodell: Kostenpflichtiges Abonnement
  - Quellcode: Proprietär
  - Unterschiede: Besonders komfortabel, aber ohne dauerhaft kostenlose Vollversion.

  </div>
  <div class="karte">

  **Keepass**

  - Kostenmodell: Kostenlos
  - Quellcode: Open Source
  - Unterschiede: Lokale Speicherung, Synchronisierung muss selbst eingerichtet werden.

<!--
**Bitwarden**

  - Kostenmodell: Kostenlos und kostenpflichtig
  - Quellcode: Open Source
  - Unterschiede: Günstig und mit einfacher Synchronisierung.
  **1Passwort**

  - Kostenmodell: Kostenpflichtiges Abonnement
  - Quellcode: Proprietär
  - Unterschiede: Besonders komfortabel, aber ohne dauerhaft kostenlose Vollversion.
  **Keepass**

  - Kostenmodell: Kostenlos
  - Quellcode: Open Source
  - Unterschiede: Lokale Speicherung, Synchronisierung muss selbst eingerichtet werden.
-->
  </div>
</div>

<div class="fusszeile">
  
</div>

---

<div class="titel">

# Merksatz 

</div>

<div class="merksatz">
  Ein Passwortmanager schützt deine Passwörter, damit du deine Online-Konten sicherer und einfacher nutzen kannst – du musst dir nur noch ein starkes Master-Passwort merken.
</div>

<div class="box">

- wegen der vielen Hackerangriffen in der letzten Zeit
- und es auch so doof wäre wenn andere auf deine persönlichen sachen zugreifen können 

</div>
<!--
Ein Passwortmanager schützt deine Passwörter, damit du deine Online-Konten sicherer und einfacher nutzen kannst – du musst dir nur noch ein starkes Master-Passwort merken.
- wegen der vielen Hackerangriffen in der letzten Zeit
- und es auch so blöd wäre wenn andere auf deine persönlichen sachen zugreifen können 
-->
<div class="fusszeile">
  
</div>

---

<div class="titel">

# Warum sind Passwortmanager heute insgesamt so wichtig?

</div>

<div class="liste">

- Schutz vor Hackern und Diebstahl 
- Verhindern mehrfach verwendeter Passwörter
- Schutz persönlicher Daten und Konten
- Erstellen starker Passwörter

<!--
Warum sind Passwortmanager heute wichtig?
- Schutz vor Hackern und Datendiebstahl: Starke Passwörter sind schwerer zu knacken und schützen unsere Konten besser.
- Verhindern mehrfach verwendeter Passwörter: Wenn ein Passwort gestohlen wird, bleiben andere Konten mit eigenen Passwörtern besser geschützt.
- Schutz persönlicher Daten und Konten: Passwortmanager helfen dabei, private Informationen vor fremdem Zugriff zu schützen.
- Erstellen starker Passwörter: Sie erzeugen lange und zufällige Passwörter, die schwer zu erraten sind.
-->

<div class="fusszeile">
  
</div>

---

<div class="titel">

# Wie sicher ist ein Passwortmanager?

</div>

<div class="liste">

- Verschlüsselung schützt gespeicherte Passwörter
- Starkes Master-Passwort ist wichtig
- Zwei-Faktor-Authentifizierung bietet zusätzlichen Schutz 

<!--
Wie sicher ist ein Passwortmanager?
- Verschlüsselung schützt gespeicherte Passwörter: Dadurch können Unbefugte die Passwörter ohne den passenden Schlüssel nicht einfach lesen.
- Starkes Master-Passwort ist wichtig: Es erschwert es Hackern, Zugriff auf alle gespeicherten Passwörter zu bekommen.
- Zwei-Faktor-Authentifizierung bietet zusätzlichen Schutz: Selbst wenn jemand das Passwort kennt, braucht er noch einen zweiten Nachweis, um sich anzumelden.
-->

<div class="fusszeile">
  
</div>
