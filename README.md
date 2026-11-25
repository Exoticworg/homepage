# exoticworg.de

Homepage von ExoticWorg – läuft über GitHub Pages.

## Streamplan ändern (jeden Sonntag)

1. Datei **`streamplan.json`** öffnen → oben rechts auf den **Stift** klicken.
2. `woche_ab` auf den Montag der neuen Woche setzen (Format `JJJJ-MM-TT`).
3. Bei jedem Tag `zeit` und `spiel` eintragen. Leer lassen (`""`) = Pause.
4. Optional `hinweis`, z. B. `"Mittwoch Überraschungsspiel"`.
   Streampause für die ganze Woche: `"pause": true` (dazu gern ein `hinweis`).
5. Unten **Commit changes** – nach ca. 1 Minute ist der Plan online.

Die Seite zeigt nur Termine aus genau dieser Woche. Ist die Woche vorbei und noch kein neuer Plan drin, steht dort „Der neue Streamplan kommt am Sonntag“ – kein falscher Termin. Ein Datum in der Zukunft wird als „Kommende Woche“ angezeigt.

Wichtig: Anführungszeichen und Kommas stehen lassen, sonst kann die Seite den Plan nicht lesen.

## Partner ändern

Datei **`partner.json`** – pro Partner ein Block:

- `name` – Anzeigename
- `art` – `"partner"` (Freund/Empfehlung) oder `"werbung"` (Affiliate-/Werbelink, wird als „Werbung“ markiert – das ist Pflicht)
- `text` – ein, zwei Sätze
- `url` – Link (muss mit `https://` anfangen; leer = Karte ohne Link)
- `code` – optional ein Rabattcode

## Freunde ändern

Datei **`freunde.json`** – pro Freund:

- `name` – Anzeigename
- `twitch` – Twitch-Name wie in der Adresse (twitch.tv/**name**)
- `text` – optional ein kurzer Satz, sonst wird der Twitch-Link angezeigt

Die Twitch-Profilbilder holt die Action **„Freunde-Bilder holen“** automatisch, sobald `freunde.json` geändert wird (und jeden Montag). Sie liegen dann in `assets/freunde/`. Ohne Bild zeigt die Seite den Anfangsbuchstaben.

Zusätzliche Felder bei Partnern (optional): `titel` (fette Überschrift), `link_text` (Text des Links), `breit: true` (Karte doppelt so breit). Zeilenumbrüche im `text` mit `\n`.
