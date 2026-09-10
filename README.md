# Sudoku – PWA

Enthält mehrere Dateien, die zusammen im selben Ordner bleiben müssen:

- `index.html` – die App
- `manifest.json` – macht die App installierbar
- `sw.js` – Service Worker für Offline-Nutzung
- `icon.svg`, `icon-192.png`, `icon-512.png`, `icon-512-maskable.png` – App-Icons (PNG-Varianten sind nötig, damit z. B. Samsung Internet die Installation zuverlässig anbietet)
- `hirsch.png` – Sponsor-Grafik auf dem Startbildschirm

## Wichtig: Hosting nötig für "Installieren"

Damit dein Handy-Browser den Button "Zum Startbildschirm hinzufügen" /
die Installations-Möglichkeit anbietet, muss die App über **https** von
einem echten Server ausgeliefert werden (Service Worker funktionieren
nicht, wenn man die Datei nur lokal doppelklickt).

Am einfachsten – kostenlos, in 2 Minuten:

1. Lege ein neues Repository auf GitHub an und lade alle Dateien hoch
   (oder nutze Netlify Drop: https://app.netlify.com/drop – dort den
   ganzen Ordner per Drag & Drop reinziehen, fertig ist die URL).
2. Bei GitHub: Einstellungen → Pages → Branch auswählen → Speichern.
   Du bekommst eine URL wie `https://dein-name.github.io/sudoku/`.
3. Diese URL auf dem Handy im Browser öffnen.
   - **Android/Chrome & Samsung Internet:** Menü → "App installieren" bzw.
     "Zum Startbildschirm hinzufügen".
   - **Android/Firefox:** kein automatischer Install-Banner mehr –
     nur "Zum Startbildschirm hinzufügen" (Menü), das legt eine
     Verknüpfung an statt einer echten Installation.
   - **iOS (nur Safari):** Teilen-Symbol → "Zum Home-Bildschirm".
     Andere iOS-Browser (Chrome, Firefox, …) laufen dort technisch auf
     Safaris Engine und bieten diese Option meist gar nicht an – auf
     iOS also immer über Safari installieren.
4. Danach startet die App wie eine normale App, auch offline
   (der Service Worker hat sie beim ersten Laden zwischengespeichert).

## Lokal zum Ausprobieren (ohne Installation)

Reicht ein einfacher lokaler Webserver, z. B. im Ordner:

```
python3 -m http.server 8080
```

und dann `http://localhost:8080` öffnen. Für den echten Install-Banner
auf dem Handy braucht es aber https – siehe oben.
