# Vermittlungsservice — Formulare

Öffentlich gehostete Telegram-WebApp-Formulare für den Hackethal
Vermittlungsservice-Bot. Enthält **keine Kundendaten** — nur die leere
Formular-Seite (HTML/CSS/JS). Bot-Token, Chat-ID und alle echten
Geschäftsdaten bleiben ausschließlich im privaten Haupt-Repo
`hackethalvermittlung/anzeigen-vermittlung`.

Muss public sein, damit GitHub Pages es auf dem kostenlosen Plan
öffentlich servieren kann (private Repos brauchen dafür GitHub Pro).
Schreibzugriff bleibt trotzdem nur beim Owner/den Collaboratorn.

- `index.html` — Menü mit allen Bot-Funktionen (seit 01.10.2026): Leads
  holen (Anzahl + Nische), Neuer Kunde, Neue Nische, Nische ausschalten,
  Provision eintragen / bezahlt / anzeigen. Der Bot hängt die aktuellen
  Nischen-Namen als `?nischen=Name1|Name2` an.
- `index.html?typ=kunde` — direkt das Formular "Neuer Kunde"
- `index.html?typ=<aktion>` — direkt eine andere Aktion (leads, nische,
  nische_aus, provision, provision_bezahlt, provisionen)

Sendet die ausgefüllten Werte per `Telegram.WebApp.sendData()` zurück an
den Bot, der sie in `scripts/telegram_commands.py` (im Haupt-Repo)
auswertet.
