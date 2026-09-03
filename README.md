<div align="center">

# ⛏ Gildoria — Strona + Sklep serwera Minecraft

[![Next.js](https://img.shields.io/badge/Next.js-15-000000?style=for-the-badge&logo=next.js&logoColor=white)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-4-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![Drizzle ORM](https://img.shields.io/badge/Drizzle-ORM-C5F74F?style=for-the-badge&logo=drizzle&logoColor=black)](https://orm.drizzle.team/)
[![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)](https://www.sqlite.org/)

[![Status](https://img.shields.io/badge/Status-Aktywne-brightgreen?style=for-the-badge)](#)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](#-licencja)

<br>

### 🌐 Kompletna strona serwera Minecraft: sklep, czat na żywo, statystyki, eventy, pomoc i automatyczne dostarczanie zakupów

Strona z prawdziwym procesem płatności i danymi z serwera w czasie rzeczywistym.
**Klimat klasycznej strony serwera MC** — bez „AI landing page": kanciaste panele, pikselowe fonty, zero gradientów.

<br>

[📸 Screenshots](#-screenshots) •
[🛠️ Technologie](#️-technologie) •
[🔌 Integracje](#-integracje) •
[📞 Kontakt](#-kontakt)

<br>

---

</div>

<br>

## 🌐 Co potrafi

### 🏠 Strona główna

Wszystko, co gracz musi zobaczyć w 3 sekundy: adres serwera, licznik graczy i droga do sklepu.

- ✅ **Karta serwera jak z listy w grze** — ikona bloku, MOTD, gracze online, pasek „siły sygnału"; kliknięcie kopiuje IP
- ✅ **Licznik graczy na żywo** — aktualizowany bez przeładowania strony
- ✅ **Czat z serwera na żywo** — sam się przewija, rozróżnia wejścia/wyjścia/zgony/osiągnięcia, maskuje wulgaryzmy
- ✅ **Feed „ostatnie zakupy"** — nicki **zamaskowane serwerowo** (`KacperGracz` → `Ka********z`)
- ✅ **Top graczy, eventy i ogłoszenia** od razu na pierwszej stronie
- ✅ **Jak dołączyć** — trzy kroki z wersją gry i adresem

### 🛒 Sklep

- ✅ **Kategorie i paczki** — rangi, monety, klucze, itemy, usługi; kafelki jak sloty w ekwipunku
- ✅ **Koszyk** — zapisywany w przeglądarce, zmiana ilości, podsumowanie
- ✅ **Kasa** — walidacja nicku Minecrafta (3–16 znaków), zgoda na regulamin, podsumowanie
- ✅ **Płatności** — karty, BLIK, przelewy, PayPal, Paysafecard przez zewnętrzną bramkę
- ✅ **Status zamówienia** — kroki *oczekuje → opłacone → dostarczone*, same się odświeżają
- ✅ **Dostawa automatyczna** — po zaksięgowaniu płatności ranga lub item lecą na serwer bez udziału administracji

### 📊 Statystyki i eventy

- ✅ **Ranking graczy** — czas gry, zabójstwa, poziom, bogactwo; sortowanie i podium top 3
- ✅ **Wyszukiwarka gracza** — pełne statystyki po nicku (K/D, monety, zbite bloki)
- ✅ **Eventy z odliczaniem** — turnieje, dropy, konkursy; status *trwa / zaplanowany / zakończony*

### 🎥 Streamy z serwera

- ✅ **Baner „TRWA STREAM"** — pojawia się sam, gdy ktoś streamuje serwer
- ✅ **Osadzony player** — tytuł, liczba widzów, link do kanału
- ✅ **Wykrywanie na dwa sposoby** — po zlinkowanych nickach (gracz ↔ kanał) albo po tytule transmisji zawierającym IP serwera

### 🎧 Pomoc i panel

- ✅ **LiveHelp** — widget w rogu ekranu, zgłoszenie bez logowania
- ✅ **Panel administracyjny** — odpowiedzi na zgłoszenia, zamówienia, kolejka komend, przychód
- ✅ **Dostęp chroniony hasłem** i podpisanym ciasteczkiem

---

## 🔌 Integracje

### 🧩 Serwer Minecraft (Paper / Spigot)

- ✅ **Serwer → strona** — czat, wejścia/wyjścia, zgony, osiągnięcia, gracze online, TPS, wersja, eventy
- ✅ **Strona → serwer** — komendy do wykonania (np. nadanie rangi za zakup) i wiadomości ze strony na czat w grze
- ✅ **Potwierdzenie wykonania** — zamówienie samo przechodzi na status *zrealizowane*
- ✅ **Komunikacja po HTTP z tokenem** — żadnych zewnętrznych zależności po stronie Javy

### 💳 Płatności

- ✅ Koszyk tworzony w bramce płatności → gracz dostaje bezpieczny link
- ✅ **Webhook z weryfikacją podpisu HMAC-SHA256**
- ✅ Zdarzenia: opłacone / odrzucone / zwrócone
- ✅ Komendy z paczki lecą na serwer z podstawionym nickiem (`{nick}`, `{quantity}`, `{package}`)

### 🤖 Discord

- ⏳ **Bot w przygotowaniu** — status serwera, statystyki gracza, powiadomienia o zakupach i streamach

---

## 🎨 Wygląd

Celowo **nie** jest to „AI landing page". Zasady zapisane w `apps/web/src/app/globals.css`:

- 🟩 **Wszystko kwadratowe** — `border-radius: 0` wymuszone globalnie
- 🔤 **Fonty pikselowe serwowane lokalnie** — bez pytań do Google Fonts, szybciej i bez problemów z RODO
- 🧱 **Panele jak okno inventory** — ostra ramka, światło od góry, cień od dołu
- 🔘 **Wciskane przyciski** — efekt 3D jak w menu gry, animacje klatkowe zamiast miękkich przejść
- ⛏ **Własne ikony SVG** zamiast emoji — identyczne na każdym systemie
- 🖼️ **Social preview generowane automatycznie** — po wklejeniu linku na Discordzie czy X wyświetla się grafika z nazwą i IP serwera

---

## 📸 Screenshots

Zdjęcia leżą w folderze `screenshots/`.

### 🏠 Strona główna

Karta serwera jak z listy w grze, czat na żywo, feed zakupów z zamaskowanymi nickami, top graczy i nadchodzące eventy.

<img src="screenshots/strona-glowna.png" alt="Strona główna" width="800">

*Wszystkie dane „na żywo" — czat, gracze i zakupy aktualizują się bez przeładowania strony*

<br><br>

### 🛒 Sklep

Kafelki paczek jak sloty w ekwipunku, kategorie, odznaki (Bestseller / Promocja / Polecane).

<img src="screenshots/sklep.png" alt="Sklep" width="800">

*Sklep — ceny liczone po stronie serwera, koszyk zapisywany w przeglądarce*

<br><br>

### 🧾 Koszyk i płatność

Podsumowanie, nick gracza, zgoda na regulamin i przejście do bramki płatności.

<img src="screenshots/koszyk.png" alt="Koszyk" width="800">

*Kasa — walidacja nicku Minecrafta i podsumowanie zamówienia*

<br><br>

### 📦 Status zamówienia

Kroki *oczekuje → opłacone → dostarczone* z automatycznym odświeżaniem.

<img src="screenshots/zamowienie.png" alt="Status zamówienia" width="800">

*Zamówienie — po wykonaniu komend na serwerze status zmienia się na „zrealizowane"*

<br><br>

### 📊 Statystyki

Ranking z sortowaniem, podium i wyszukiwarką gracza.

<img src="screenshots/statystyki.png" alt="Statystyki" width="800">

*Statystyki graczy — czas gry, K/D, poziom, bogactwo*

<br><br>

### 🛠️ Panel administracyjny

Zgłoszenia pomocy z odpowiedziami, zamówienia i kolejka komend do wykonania na serwerze.

<img src="screenshots/panel.png" alt="Panel administracyjny" width="800">

*Panel — obsługa pomocy i sprzedaży w jednym miejscu*

<br><br>

### 🎥 Stream z serwera

Baner „TRWA STREAM" z osadzonym playerem — pojawia się sam po wykryciu transmisji.

<img src="screenshots/stream.png" alt="Stream z serwera" width="800">

*Wykrywanie streamów — po zlinkowanych kanałach albo po tytule z IP serwera*

<br>

---

## 🛠️ Technologie

| Warstwa | Technologia |
|---|---|
| Frontend | **Next.js 15** (App Router), **React 19**, **TypeScript** |
| Style | **Tailwind CSS v4** + własny design system (`mc-panel`, `mc-btn`, `mc-slot`) |
| Baza | **Drizzle ORM** + **SQLite** (pod produkcję: **Postgres** — zmiana 3 linii) |
| Dane na żywo | **SSE** (`/api/realtime`) + event bus |
| Płatności | bramka zewnętrzna + webhook HMAC |
| Streamy | **Twitch Helix API** |
| Hosting | **Fly.io** (Docker + wolumen pod bazę) |

---

## 🔒 Bezpieczeństwo

- 🔐 Płatności idą przez **zewnętrzną bramkę** — strona nie ma dostępu do danych karty
- 🔐 Ceny wyliczane **wyłącznie po stronie serwera**
- 🔐 Nicki w publicznym feedzie zakupów **maskowane** (tryby: częściowy / pełny / wyłączony)
- 🔐 Ochrona przed spamem na czacie, w koszyku, pomocy i logowaniu
- 🔐 Panel i webhooki chronione hasłem oraz podpisem kryptograficznym

---

<div align="center">

## 📄 Licencja

**MIT** — możesz używać, modyfikować i sprzedawać.

Copyright (c) 2026 WilkorPLYT (𝓓𝓻𝓦𝓲𝓵𝓴𝓸𝓻)

Pełny tekst: [LICENSE](LICENSE)

<br>

---

## 👨‍💻 Autor

| Developer | Discord | GitHub |
|-----------|---------|--------|
| **𝓓𝓻𝓦𝓲𝓵𝓴𝓸𝓻** | [DrWilkor](https://discord.com/users/446740090757316608) | [@WilkorPLYT](https://github.com/WilkorPLYT) |

<br>

Stworzony z ❤️ przez **𝓓𝓻𝓦𝓲𝓵𝓴𝓸𝓻**

<br>

[![Discord](https://img.shields.io/badge/Discord-DrWilkor-5865F2?style=flat-square&logo=discord&logoColor=white)](https://discord.com/users/446740090757316608)
[![GitHub](https://img.shields.io/badge/GitHub-WilkorPLYT-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/WilkorPLYT)

<br>

---

**⭐ Jeśli podoba Ci się ten projekt, zostaw gwiazdkę! ⭐**

<br>

<sub>Dokumentacja techniczna (uruchomienie, wdrożenie, architektura, kontrakty API): katalog `docs/`</sub>

</div>
