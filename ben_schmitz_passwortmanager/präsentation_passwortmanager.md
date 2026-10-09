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
    --blau:      #000000;   /* Titel, Balken, Linien */
    --blau-hell: #000000;   /* Akzente, Rand der Karten */
    --flaeche:   #c8ccd1;   /* Hintergründe von Kästen */
    --flaeche-2: #edf5fb;   /* zweiter Hintergrundton */
    --flaeche-3: #e8f1f8;   /* dritter Hintergrundton */
    --flaeche-4: #a9c1cf;   /* Karten */
    --gelb:      #f7f7f7;   /* Hervorhebung */
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

- Was möchte ich erreichen? - Nutzen von sicheren Passwortmanagern für weniger Ausgaben von Geld
- Leitfrage und Ziel: Was möchte ich zeigen oder klären?
- Ben-Luca Schmitz
- Klasse 9A I Diff.-Kurs Informatik
- Stand: 02.10.2026

</div>

<div class="fusszeile">
  
</div>

---

<div class="titel">

# Welche wichtigen Funktionen kann ich kostenlos bei einem Passwortmanager nutzen?

</div>

<div class="liste">

- Sichere Speicherung von Passwörtern
- Bearbeitung und Verwaltung von Paswörtern
- Nutzung auf mehreren Geräten
- Verschlüsselung der Passwörter
- Sichere Notizen und Überprüfungen

</div>

<div class="fusszeile">
  Passwortmanager · Ben Schmitz , 9A
</div>

---

<div class="titel">

# Vor-& Nachteile von kostenlosen Passwortmanagern

</div>

<div class="grid-2">
  <div class="spalte">

  **Vorteile**

  - keine Gebühren
  - ebenfalls sicheres Speichern und Verschlüsseln
  - gut zum ausprobieren von dingen
  

  </div>
  <div class="spalte">

  **Nachteile**

  - weniger Geräte nutzbar
  - Weniger Komfortfunktionen
  - Oft viel (Eigen-)Werbung
  - weniger Zusatzfunktionen
  - Weniger Sicherheitsfunktionen
  - Eingeschränkte Synchroniesierung 


  </div>
</div>

<div class="fusszeile">
  Passwortmanager · Ben Schmitz , 9A
</div>

---

<div class="titel">

# Drei kostenlose qualititave Passwortmanager
</div>

<div class="karten">
  <div class="karte">

  **Bitwarden**

  - Unbegrenzt Passwörter Speichern
  - Open Source
  - Synchroniesierung über Onlinedienst nach Abspeicherung in der Cloud

  </div>
  <div class="karte">

  **KeePassXC**

  - komplett kostenlos und Open Source
  - Zugriff jederzeit auf eigene Passwortdatenbank
  - Eigene Kümmerung um Backups

  </div>
  <div class="karte">

  **Protonpass**

  - Ende zu Ende Verschlüsselung
  - Nutzung von Onlinedienst von Proton nach Synchroniesierung

  </div>
</div>

<div class="fusszeile">
  Passwortmanager · Ben Schmitz , 9A
</div>

---

<div class="titel">

# Wichtige Funktionen von kostenpflichtigen Versionen  bei Passwortmanagern

</div>

<div class="liste">

- Synchronisierung auf beliebig vielen Geräten
- Detaillierte Analysen und doppeltes Absichern von Daten
- Direkter Kontakt und Support beim Managerdienst
- Größerer Verschlüsselter Daten- & Speicherplatz
- Erweiterte Authentifizierungsfunktionen

</div>

<div class="fusszeile">
  Passwortmanager · Ben Schmitz, 9A
</div>

---

<div class="titel">

# Darum bieten Kostenpflichtige Premiumfunktionen mehr als kostenlose Nutzungen

</div>

<div class="liste">

- Mehr Geld
- Höhere Server und Speicherkosten
- Profesioneller Kundensupport jederzeit

</div>

<div class="fusszeile">
  Passwortmanager · Ben Schmitz , 9A
</div>

---