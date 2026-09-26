# Vermittlungsservice — Formulare

Öffentlich gehostete Telegram-WebApp-Formulare für den Hackethal
Vermittlungsservice-Bot. Enthält **keine Kundendaten** — nur die leere
Formular-Seite (HTML/CSS/JS). Bot-Token, Chat-ID und alle echten
Geschäftsdaten bleiben ausschließlich im privaten Haupt-Repo
`hackethalvermittlung/anzeigen-vermittlung`.

Muss public sein, damit GitHub Pages es auf dem kostenlosen Plan
öffentlich servieren kann (private Repos brauchen dafür GitHub Pro).
Schreibzugriff bleibt trotzdem nur beim Owner/den Collaboratorn.

- `index.html?typ=kunde` — Formular "Neuer Kunde"
- `index.html?typ=nische` — Formular "Neue Nische"

Sendet die ausgefüllten Werte per `Telegram.WebApp.sendData()` zurück an
den Bot, der sie in `scripts/telegram_commands.py` (im Haupt-Repo)
auswertet.
