# straz-vps

Strażnik VPS spoza Hetznera. VPS co 30 min zapisuje `bicie.txt` (epoch + czas UTC). Cron Actions co 30 min sprawdza
wiek bicia: ≥ 60 min = bieg oblany → GitHub wysyła właścicielowi konta e-mail („Run failed: straz-vps”).

- Nadawca bicia: `~/architekt-vps/straz/bicie.sh` (wołany z `check_i_alarm.sh`, `architekt-check.timer`).
- Brak sekretów w tym repo. Treść: tylko znacznik czasu.
- Repo publiczne, bo minuty Actions dla repo prywatnych dzieli konto z CI KGNB.
