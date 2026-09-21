# HerdenPro – Projekt-Links

Alle wichtigen URLs für Entwicklung, Deployment und Administration der App.

Stand: Juni 2026 · Projekt-ID Firebase: **herdenmanagement-33ff5** (Region: europe-west1)

---

## 🐄 Live-App

- **HerdenPro Web-App**: https://sepplkbg.github.io/herdenpro/

---

## 📦 Code & Quellcode (GitHub)

- **Repository (Übersicht)**: https://github.com/sepplkbg/herdenpro
- **Dateien hochladen** (Upload neuer/aktualisierter Dateien): https://github.com/sepplkbg/herdenpro/upload/main
- **Einzelne Datei bearbeiten** (z.B. `index.html`): https://github.com/sepplkbg/herdenpro/edit/main/index.html
- **Commits-Verlauf** (was wann geändert): https://github.com/sepplkbg/herdenpro/commits/main
- **GitHub Pages Settings** (Deploy-Status, Custom Domain): https://github.com/sepplkbg/herdenpro/settings/pages

---

## 🔥 Firebase-Konsole (Datenbank, Auth, Regeln)

- **Projekt-Übersicht**: https://console.firebase.google.com/project/herdenmanagement-33ff5
- **Realtime Database – Daten ansehen**: https://console.firebase.google.com/project/herdenmanagement-33ff5/database/herdenmanagement-33ff5-default-rtdb/data
- **Database Rules** (Permissions, z.B. für `schalmtest`, `spielScores`, neue Pfade): https://console.firebase.google.com/project/herdenmanagement-33ff5/database/herdenmanagement-33ff5-default-rtdb/rules
- **Authentication – User-Verwaltung**: https://console.firebase.google.com/project/herdenmanagement-33ff5/authentication/users
- **Usage / Analytics**: https://console.firebase.google.com/project/herdenmanagement-33ff5/usage

---

## 📋 Vorlagen & Downloads

- **Saisonstart-Excel-Vorlage** (lädt direkt aus dem Repo): https://sepplkbg.github.io/herdenpro/Saisonstart_Vorlage.xlsx

---

## 🛠 Status-Checks & Tools

- **GitHub Pages Status**: https://www.githubstatus.com/
- **Firebase Status**: https://status.firebase.google.com/
- **PWA-Lighthouse-Test** (App-Qualität, Installierbarkeit): https://pagespeed.web.dev/?url=https%3A%2F%2Fsepplkbg.github.io%2Fherdenpro%2F

---

## 🚀 Standard-Deployment-Workflow

1. Code lokal ändern in `C:\Users\lonig\Downloads\Herdenmanagement\`
2. Auf GitHub hochladen: https://github.com/sepplkbg/herdenpro/upload/main
3. Commit-Message eintragen → **„Commit changes"**
4. ~1–2 Minuten warten bis GitHub Pages den Deploy abschließt
5. Auf jedem Endgerät: Aa-Icon im Topbar → **„↺ App aktualisieren"**
   (alternativ: Mehr → 📐 Darstellung → „Cache leeren & neu laden")

---

## 🔐 Firebase-Rules ergänzen (Vorlage)

Wenn ein neues Modul einen neuen Firebase-Pfad braucht (z.B. ein neues Feature
mit eigenen Daten), in den Database Rules ergänzen:

```json
"neuerPfad": { ".read": "auth != null", ".write": "auth != null" }
```

Komma zur vorherigen Zeile nicht vergessen. Die letzte Regel im Block darf
**kein** Komma am Ende haben, sonst meckert der JSON-Parser.

Bereits angelegte Pfade (Stand v152):
`benutzer`, `kuehe`, `behandlungen`, `besamungen`, `zaehlung`, `zaehlVerlauf`,
`milch`, `milchEintraege`, `weideTage`, `weiden`, `bauern`, `saison`,
`saisonArchiv`, `journal`, `kontakte`, `gruppen`, `fotos`, `herde_session`,
`chat`, `kraftfutter`, `kfLieferungen`, `kaese_produktion`, `kalenderTermine`,
`traenkeLog`, `stallplan`, `stallplanV2`, `wartung`, `lager`, `aufgaben`,
`almKarteWeiden`, `klauenpflege`, `schalmtest`, `spielScores`

---

## 📞 Schnellzugriff für häufige Probleme

| Problem | Lösung-URL |
|---|---|
| Hirte sieht neue Module nicht | Aa-Icon → App aktualisieren |
| PERMISSION_DENIED beim Speichern | https://console.firebase.google.com/project/herdenmanagement-33ff5/database/herdenmanagement-33ff5-default-rtdb/rules |
| App zeigt veraltete Version | Aa-Icon → App aktualisieren (auf jedem Gerät) |
| Neue Datei deployen | https://github.com/sepplkbg/herdenpro/upload/main |
| Benutzer freischalten | https://console.firebase.google.com/project/herdenmanagement-33ff5/authentication/users |

---

*HerdenPro · Engineering by LN Machinery*
