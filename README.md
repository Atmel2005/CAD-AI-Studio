# 🚀 CAD AI Studio

**English below / Deutsch / Українська / Русский**

Windows CAD-application with a built-in LLM: describe a part in plain text (or attach a photo) — the AI builds a real, validated, 3D-printable model. Three interchangeable CAD backends: **Autonomous** (built-in parametric engine on OpenCascade), **FreeCAD** and **Solid Edge 2026** (via MCP bridge). Plus organic-model pipelines: SDF sculpting by description and photo-to-3D via Stable Fast 3D.

---

## Deutsch

### Was ist das?
CAD AI Studio ist eine Desktop-Anwendung für Windows (PySide6), die eine lokale oder externe LLM mit einem parametrischen CAD-Engine verbindet. Die KI beschreibt kein Modell als Text — sie ruft echte CAD-Werkzeuge auf (Primitives, Booleans, Gewinde, Zahnräder, Loft, SDF-Felder, Bild-zu-3D) und das Ergebnis wird automatisch auf Druckbarkeit geprüft und als STL/STEP/3MF exportiert.

### CAD-Backends (wählbar in den Einstellungen)
- **Autonomous AI CAD** — eigener paramischer Engine (build123d/OpenCascade): Primitive, Boolean-Operationen, Gewinde, Zahnräder, Patterns, Loft/Sweep, SDF-Modelle (März-Februar: organische Formen wie Tiere/Figuren), Bild-zu-3D (Stable Fast 3D).
- **FreeCAD** — über FreeCAD MCP Server (Port 39280).
- **Solid Edge 2026** — über Solid Edge MCP Bridge (Port 39281), ~68 Werkzeuge.

### LLM-Anbindung
Die App arbeitet mit einem OpenAI-kompatiblen Endpoint — z. B. llama.cpp (`llama-server`), LM Studio oder einem Remote-Server. Modellverwaltung (Modelle durchsuchen, herunterladen, pro Modell Einstellungen) ist im Einstellungsdialog integriert.

### Installation
1. `CAD_AI_Studio.exe` herunterladen.
2. Die Programmarchive (`*.7z.part*.rar`/Teile) aus den **Releases** herunterladen — sie sind passwortgeschützt; das Passwort ist im Programm eingebettet, die Selbst-Extraktion erfolgt automatisch beim ersten Start.
3. Fehlende oder beschädigte Dateien werden beim nächsten Start automatisch nachgeladen.
4. **Optional:** Solid Edge 2026 oder FreeCAD separat installieren — sie werden nicht mitgeliefert (Lizenzbedingungen).

### Systemanforderungen
- Windows 10/11 (64-bit)
- RAM: 16 GB empfohlen (mehr für große LLMs)
- GPU: NVIDIA mit CUDA-Treiber empfohlen (bild-zu-3D und LLM-Beschleunigung)
- ~15 GB freier Speicherplatz

### Funktionen
- Parametrischer CAD-Tree mit inkrementeller Neuberechnung
- Automatische Druckbarkeitsprüfung (Watertight, Überhänge, Stabilität)
- Export: STL, STEP, 3MF, OBJ + Statistik
- Visuelle Kontrolle: OpenGL-Viewer + optionaler VTK-Viewer
- Autonome Korrekturschleife (LLM sieht Fehlschläge und repariert das Modell)
- SDF-Modus für organische Formen (Elefant, Figuren) nach Beschreibung
- Bild-zu-3D-Modus (Stable Fast 3D, lokal über HuggingFace-Gewichte)

---

## Українська

### Що це?
CAD AI Studio — Windows-застосунок (PySide6), що поєднує локальну або зовнішню LLM з параметричним CAD-рушієм. ШІ не описує модель текстом — він викликає реальні CAD-інструменти (примітиви, булеві операції, різьби, шестерні, loft, SDF-поля, image-to-3D), а результат автоматично перевіряється на придатність до друку та експортується у STL/STEP/3MF.

### CAD-бекенди (вибираються в налаштуваннях)
- **Autonomous AI CAD** — власний параметричний рушій (build123d/OpenCascade): примітиви, булеві, різьби, шестерні, патерни, loft/sweep, SDF-моделі для органічних форм, image-to-3D через Stable Fast 3D.
- **FreeCAD** — через FreeCAD MCP Server (порт 39280).
- **Solid Edge 2026** — через Solid Edge MCP Bridge (порт 39281), ~68 інструментів.

### Підключення LLM
Працює з OpenAI-сумісним endpoint — llama.cpp (`llama-server`), LM Studio або віддалений сервер. Управління моделями (пошук, завантаження, налаштування для кожної моделі) вбудовано в діалог налаштувань.

### Встановлення
1. Завантажте `CAD_AI_Studio.exe`.
2. Завантажте архіви програми (частини) з **Releases** — вони захищені паролем; пароль вбудований у програму, саморозпакування відбувається автоматично при першому запуску.
3. Відсутні або пошкоджені файли автоматично довантажуються при наступному запуску.
4. **Опційно:** Solid Edge 2026 або FreeCAD встановлюються окремо — не постачаються (ліцензійні умови).

### Системні вимоги
- Windows 10/11 (64-bit)
- RAM: рекомендовано 16 ГБ (більше для великих LLM)
- GPU: NVIDIA з CUDA-драйвером рекомендовано
- ~15 ГБ вільного місця

### Можливості
- Параметричне CAD-дерево з інкрементним перерахунком
- Автоматична перевірка на друк (watertight, нависання, стійкість)
- Експорт: STL, STEP, 3MF, OBJ + статистика
- Візуальний контроль: OpenGL-в'ювер + опційний VTK
- Автономний цикл виправлень (ШІ бачить помилки і ремонтує модель)
- SDF-режим для органічних форм за описом
- Image-to-3D (Stable Fast 3D, локально через ваги HuggingFace)

---

## English

### What is it?
CAD AI Studio is a Windows desktop app (PySide6) that connects a local or remote LLM to a parametric CAD engine. The AI does not "describe" a model — it calls real CAD tools (primitives, booleans, threads, gears, loft, SDF fields, image-to-3D), and the result is automatically checked for printability and exported as STL/STEP/3MF.

### CAD backends (selectable in Settings)
- **Autonomous AI CAD** — built-in parametric engine (build123d/OpenCascade): primitives, booleans, threads, gears, patterns, loft/sweep, SDF models for organic shapes, image-to-3D via Stable Fast 3D.
- **FreeCAD** — via FreeCAD MCP Server (port 39280).
- **Solid Edge 2026** — via Solid Edge MCP Bridge (port 39281), ~68 tools.

### LLM connection
Works with any OpenAI-compatible endpoint — llama.cpp (`llama-server`), LM Studio, or a remote server. Model management (browse, download, per-model settings) is built into the settings dialog.

### Installation
1. Download `CAD_AI_Studio.exe`.
2. Download the program archives (split parts) from **Releases** — they are password-protected; the password is embedded in the app and self-extraction runs automatically on first launch.
3. Missing or corrupted files are re-downloaded automatically on the next start.
4. **Optional:** install Solid Edge 2026 or FreeCAD separately — they are not bundled (licensing).

### System requirements
- Windows 10/11 (64-bit)
- RAM: 16 GB recommended (more for large LLMs)
- GPU: NVIDIA with CUDA driver recommended
- ~15 GB free disk space

### Features
- Parametric CAD tree with incremental regeneration
- Automatic printability checks (watertight, overhangs, stability)
- Export: STL, STEP, 3MF, OBJ + statistics
- Visual check: OpenGL viewer + optional VTK viewer
- Autonomous correction loop (the AI sees failures and repairs the model)
- SDF mode for organic shapes (elephant, figurines) from description
- Image-to-3D mode (Stable Fast 3D, local via HuggingFace weights)

---

## Русский (оригинал)

### Что это?
CAD AI Studio — Windows-приложение (PySide6), которое соединяет локальную или удалённую LLM с параметрическим CAD-движком. ИИ не «описывает» модель текстом — он вызывает настоящие CAD-инструменты (примитивы, булевы операции, резьбы, шестерни, loft, SDF-поля, image-to-3D), а результат автоматически проверяется на пригодность к печати и экспортируется в STL/STEP/3MF.

### CAD-бэкенды (выбираются в настройках)
- **Autonomous AI CAD** — собственный параметрический движок (build123d/OpenCascade): примитивы, булевы, резьбы, шестерни, паттерны, loft/sweep, SDF-модели для органических форм, image-to-3D через Stable Fast 3D.
- **FreeCAD** — через FreeCAD MCP Server (порт 39280).
- **Solid Edge 2026** — через Solid Edge MCP Bridge (порт 39281), ~68 инструментов.

### Подключение LLM
Работает с любым OpenAI-совместимым endpoint — llama.cpp (`llama-server`), LM Studio или удалённый сервер. Управление моделями (поиск, загрузка, настройки для каждой модели) встроено в диалог настроек.

### Установка
1. Скачайте `CAD_AI_Studio.exe`.
2. Скачайте архивы программы (части) из **Releases** — они защищены паролем; пароль встроен в программу, самораспаковка происходит автоматически при первом запуске.
3. Отсутствующие или повреждённые файлы автоматически докачиваются при следующем запуске.
4. **Опционально:** Solid Edge 2026 или FreeCAD устанавливаются отдельно — не поставляются (лицензионные условия).

### Системные требования
- Windows 10/11 (64-bit)
- RAM: рекомендуется 16 ГБ (больше для больших LLM)
- GPU: рекомендуется NVIDIA с CUDA-драйвером
- ~15 ГБ свободного места

### Возможности
- Параметрическое CAD-дерево с инкрементным пересчётом
- Автоматическая проверка на печать (watertight, нависания, устойчивость)
- Экспорт: STL, STEP, 3MF, OBJ + статистика
- Визуальный контроль: OpenGL-вьювер + опциональный VTK
- Автономный цикл исправлений (ИИ видит ошибки и чинит модель)
- SDF-режим для органических форм по описанию
- Image-to-3D (Stable Fast 3D, локально через веса HuggingFace)

---

## Лицензия / License / Lizenzія

Proprietary / Proprietär / Власницька / Пропрієтарна.
