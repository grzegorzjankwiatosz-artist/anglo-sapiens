# Anglo-Sapiens — Kurs Angielskiego

Interaktywny kurs angielskiego dla Polaków. GitHub Pages + PWA.

## 🚀 Jak uruchomić

1. Utwórz nowe repozytorium GitHub (np. `anglo-sapiens`)
2. Wgraj wszystkie pliki z tego folderu
3. W ustawieniach repo → **Pages** → Branch: `main` / folder: `/ (root)`
4. Kurs będzie dostępny pod: `https://TWOJ-LOGIN.github.io/anglo-sapiens/`

**Ważne:** Jeśli repozytorium NIE nazywa się `anglo-sapiens`, zmień ścieżkę `/anglo-sapiens/` w plikach `sw.js` i `manifest.json` na właściwą.

---

## 📁 Struktura plików

```
anglo-sapiens/
├── index.html          ← Strona główna z listą unitów
├── manifest.json       ← PWA: instalacja na telefonie
├── sw.js               ← Service Worker: tryb offline
├── README.md
└── unit1/
    ├── index.html      ← Unit 1: ABC – The Alphabet
    └── mp3/            ← (opcjonalnie) Twoje nagrania MP3
        ├── letter-a.mp3
        ├── letter-b.mp3
        ├── ...
        ├── dialog1.mp3
        ├── dialog2.mp3
        └── dialog3.mp3
```

---

## 🎵 Jak dodać nagrania MP3

Bez nagrań kurs działa — używa syntezatora mowy przeglądarki (Web Speech API).

Żeby dodać własne nagrania:

### Litery alfabetu
Wgraj pliki do `unit1/mp3/` o nazwie:
- `letter-a.mp3`, `letter-b.mp3`, ..., `letter-z.mp3`

### Dialogi
- `dialog1.mp3` — dialog "Podajesz swoje imię"
- `dialog2.mp3` — dialog "Podajesz adres"
- `dialog3.mp3` — dialog "Podajesz e-mail"

Pliki wczytują się automatycznie. Jeśli plik nie istnieje → fallback na syntezator.

---

## ➕ Jak dodać nowy Unit

1. Utwórz folder `unit2/`
2. Skopiuj `unit1/index.html` jako punkt startowy
3. Zamień dane w sekcji `// DATA` na nowe słownictwo
4. W `index.html` (strona główna) zmień kartę Unit 02 z `locked` na `active` i dodaj link

### Szablon danych do nowego unitu:
```javascript
const WORDS = [
  { word: 'zero',  pl: 'zero',   sound: '[zierołu]' },
  { word: 'one',   pl: 'jeden',  sound: '[łan]'     },
  // ...
];
```

---

## 📱 PWA — Instalacja na telefonie

Kurs działa jak aplikacja:
- Otwórz w Chrome na telefonie
- Pojawi się banner "Zainstaluj"
- Po instalacji działa **offline**

---

## 🗂 Planowane unity

| # | Temat | Status |
|---|-------|--------|
| 01 | ABC — The Alphabet | ✅ Gotowy |
| 02 | Numbers | 🔜 Wkrótce |
| 03 | Greetings | 🔜 Wkrótce |
| 04 | Personal Info | 🔜 Wkrótce |
| 05 | Days & Months | 🔜 Wkrótce |
| 06 | Family | 🔜 Wkrótce |

---

Materiały: Anglo-Sapiens 1 © Violetta Pugh  
Implementacja: GitHub Pages PWA
