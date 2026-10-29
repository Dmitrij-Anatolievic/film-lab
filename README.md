# Laboratorio Pellicola · film-lab

**[Italiano](#italiano) · [English](#english) · [Русский](#русский)**

Prova online / Try it online / Попробовать онлайн: **https://dmitrij-anatolievic.github.io/film-lab/**

---

## Italiano

Simulatore spettrale di pellicola fotografica, strato per strato, costruito sulle schede tecniche pubblicate. Serve a progettare una pellicola propria — a basso impatto ambientale e con resa realistica — da proporre in seguito a un produttore.

### Cosa fa

- Ogni "provetta" è uno strato dell'emulsione: si sceglie a quale luce è sensibile, quale colorante forma allo sviluppo, contrasto e densità. Il risultato appare su due scatti di prova.
- Processo negativo (C-41) o invertibile (E-6), densità del supporto, curve colore o B/N, bilanciamento, stampa su carta, esposizione e grana.
- «Ispeziona un punto»: mostra cosa succede in ogni strato per un singolo pixel.
- Esempio interattivo di sintesi sottrattiva con le curve reali dei coloranti Kodak Vision3.
- Ricognizione sulla chimica a basso impatto (Caffenol, sviluppi all'acido ascorbico, CD-4, EDTA, recupero dell'argento), con il livello di affidabilità di ogni voce.

### Dati e fonti

Ogni parametro del modello è etichettato: **2+ fonti** (confermato da almeno due fonti indipendenti), **1 fonte** (una sola fonte o fonte secondaria), **stima** (scelta del modello, da verificare). Tra i dati: curve Kodak Gold 200 estratte dal PDF vettoriale della scheda E-7022, curve B/N Ilford/Harman (HP5 Plus, FP4 Plus, Delta 100/400, XP2 Super), e densità del supporto misurate da me con una Nikon Zfc (Kodak ColorPlus 200, Fomapan 100, LomoChrome Metropolis, Shanghai GP3 100). La tabella completa è nella pagina.

### Scene di prova

Le due scene in `img/` sono dati RGB lineari a 16 bit (primari sRGB, bilanciamento del bianco della fotocamera) convertiti dai NEF della Nikon Zfc; `img/scene.json` ne descrive formato e origine. Le foto caricate dall'utente restano nel browser; essendo JPEG sono un'approssimazione.

### Limiti

Il RAW registra tre canali, non lo spettro completo; l'infrarosso è stimato. I coloranti «fantasia» hanno spettri stimati, la maschera arancio è un colore uniforme, la Duochrome Polaroid è un'approssimazione visiva. Il risultato serve a capire l'idea: un produttore dovrà verificarlo con curve spettrali reali.

### Uso

È una pagina HTML unica, senza installazione. In locale va servita via HTTP (la pagina carica i file di `img/` con `fetch`), per esempio:

```
python3 -m http.server
```

e poi aprire `http://localhost:8000`.

### Feedback

Osservazioni tecniche benvenute: apri una *issue*.

---

## English

A spectral, layer-by-layer photographic film simulator built on published datasheets. Its purpose is to design an original film — low environmental impact, realistic rendering — to be proposed later to a manufacturer.

### What it does

- Each "test tube" is an emulsion layer: choose what light it is sensitive to, which dye it forms on development, its contrast and density. The result is shown on two test shots.
- Negative (C-41) or reversal (E-6) process, base density, colour or B&W curves, balance, paper print, exposure and grain.
- "Inspect a point": shows what happens in every layer for a single pixel.
- Interactive subtractive-mixing example using the real Kodak Vision3 dye curves.
- A survey of low-impact chemistry (Caffenol, ascorbic-acid developers, CD-4, EDTA, silver recovery), with a reliability level for each item.

### Data and sources

Every model parameter is labelled **2+ sources** (confirmed by at least two independent sources), **1 source** (single or secondary source) or **estimate** (model choice, to be verified). Data include Kodak Gold 200 curves extracted from the vector PDF of datasheet E-7022, Ilford/Harman B&W curves (HP5 Plus, FP4 Plus, Delta 100/400, XP2 Super), and base densities I measured with a Nikon Zfc (Kodak ColorPlus 200, Fomapan 100, LomoChrome Metropolis, Shanghai GP3 100). The full table is in the page (Italian interface).

### Test scenes

The two scenes in `img/` are 16-bit linear RGB data (sRGB primaries, camera white balance) converted from Nikon Zfc NEF files; `img/scene.json` describes their format and origin. User-loaded photos stay in the browser; being JPEGs, they are an approximation.

### Limits

A RAW file records three channels, not the full spectrum; infrared is estimated. "Fantasy" dyes have estimated spectra, the orange mask is a uniform colour, and Polaroid Duochrome is a visual approximation. The result illustrates the idea: a manufacturer will need to verify it with real spectral curves.

### Usage

A single HTML page, no installation. Locally it must be served over HTTP (the page loads `img/` with `fetch`), e.g. `python3 -m http.server`, then open `http://localhost:8000`.

### Feedback

Technical feedback is welcome: please open an issue.

---

## Русский

Спектральный симулятор фотоплёнки, слой за слоем, построенный на опубликованных технических паспортах. Цель — разработать собственную плёнку с низким воздействием на окружающую среду и реалистичной передачей, чтобы затем предложить её производителю.

### Что он делает

- Каждая «пробирка» — слой эмульсии: выбирается, к какому свету он чувствителен, какой краситель образует при проявлении, его контраст и плотность. Результат показывается на двух тестовых снимках.
- Негативный (C-41) или обращаемый (E-6) процесс, плотность подложки, цветные или ч/б кривые, баланс, печать на бумаге, экспозиция и зерно.
- «Проверить точку»: показывает, что происходит в каждом слое для одного пикселя.
- Интерактивный пример субтрактивного смешения на реальных кривых красителей Kodak Vision3.
- Обзор химии с низким воздействием (Caffenol, проявители на аскорбиновой кислоте, CD-4, ЭДТА, извлечение серебра) с указанием надёжности каждого пункта.

### Данные и источники

Каждый параметр модели помечен: **2+ источника** (подтверждено как минимум двумя независимыми источниками), **1 источник** (один или вторичный источник), **оценка** (выбор модели, требует проверки). Среди данных: кривые Kodak Gold 200, извлечённые из векторного PDF паспорта E-7022, ч/б кривые Ilford/Harman (HP5 Plus, FP4 Plus, Delta 100/400, XP2 Super) и плотности подложки, измеренные мной камерой Nikon Zfc (Kodak ColorPlus 200, Fomapan 100, LomoChrome Metropolis, Shanghai GP3 100). Полная таблица — на странице (интерфейс на итальянском).

### Тестовые сцены

Две сцены в `img/` — линейные 16-битные RGB-данные (основные цвета sRGB, баланс белого камеры), полученные из NEF-файлов Nikon Zfc; `img/scene.json` описывает их формат и происхождение. Загруженные пользователем фото остаются в браузере; поскольку это JPEG, результат приблизительный.

### Ограничения

RAW записывает три канала, а не полный спектр; инфракрасный канал оценивается. «Фантазийные» красители имеют оценочные спектры, оранжевая маска — однородный цвет, Polaroid Duochrome — визуальное приближение. Результат иллюстрирует идею: производителю нужно будет проверить его по реальным спектральным кривым.

### Использование

Одна HTML-страница, без установки. Локально её нужно открывать через HTTP (страница загружает `img/` через `fetch`), например `python3 -m http.server`, затем открыть `http://localhost:8000`.

### Обратная связь

Технические замечания приветствуются: откройте issue.

---

© 2026 Dmitrij Musella (Дмитрий Муселла) · ORCID [0009-0004-4105-837X](https://orcid.org/0009-0004-4105-837X) · [MIT License](LICENSE)
