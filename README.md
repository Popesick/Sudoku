# Sudoku – PWA

Enthält 4 Dateien, die zusammen im selben Ordner bleiben müssen:

- `index.html` – die App
- `manifest.json` – macht die App installierbar
- `sw.js` – Service Worker für Offline-Nutzung
- `icon.svg` – App-Icon

## Wichtig: Hosting nötig für "Installieren"

Damit dein Handy-Browser den Button "Zum Startbildschirm hinzufügen" /
die Installations-Möglichkeit anbietet, muss die App über **https** von
einem echten Server ausgeliefert werden (Service Worker funktionieren
nicht, wenn man die Datei nur lokal doppelklickt).

Am einfachsten – kostenlos, in 2 Minuten:

1. Lege ein neues Repository auf GitHub an und lade alle 4 Dateien hoch
   (oder nutze Netlify Drop: https://app.netlify.com/drop – dort den
   ganzen Ordner per Drag & Drop reinziehen, fertig ist die URL).
2. Bei GitHub: Einstellungen → Pages → Branch auswählen → Speichern.
   Du bekommst eine URL wie `https://dein-name.github.io/sudoku/`.
3. Diese URL auf dem Handy im Browser öffnen.
   - **Android/Chrome:** Menü (⋮) → "App installieren" bzw.
     "Zum Startbildschirm hinzufügen".
   - **iOS/Safari:** Teilen-Symbol → "Zum Home-Bildschirm".
4. Danach startet die App wie eine normale App, auch offline
   (der Service Worker hat sie beim ersten Laden zwischengespeichert).

## Lokal zum Ausprobieren (ohne Installation)

Reicht ein einfacher lokaler Webserver, z. B. im Ordner:

```
python3 -m http.server 8080
```

und dann `http://localhost:8080` öffnen. Für den echten Install-Banner
auf dem Handy braucht es aber https – siehe oben.
