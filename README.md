# ПОЛИВОКС — Android Synthesizer

Советский синтезатор Поливокс на Android. WebView + Web Audio API.

## Функции

- **2 осциллятора** (пила / прямоугольник / треугольник) с детюном и строем
- **Фильтр НЧ** с резонансом, огибающей и клавиатурным слежением  
- **ADSR огибающая**
- **LFO** (синус / прямоугольник / пила) → частота / фильтр / усилитель
- **Кольцевая модуляция** (уникальная фича оригинального Поливокса)
- **16-шаговый арпеджиатор** с режимами ↑↓↕?
- **2-октавная клавиатура** со сдвигом
- **VU-метр**

## Сборка APK

### Требования
- GitHub репозиторий
- Gradle wrapper jar (нужно добавить вручную — см. ниже)

### Шаг 1 — Получить gradle-wrapper.jar

На компьютере или через Termux:
```bash
curl -L "https://services.gradle.org/distributions/gradle-8.4-bin.zip" -o gradle.zip
# Или скачай готовый wrapper jar:
# https://raw.githubusercontent.com/gradle/gradle/v8.4.0/gradle/wrapper/gradle-wrapper.jar
```

Положи `gradle-wrapper.jar` в `gradle/wrapper/`.

### Шаг 2 — Push в GitHub

```bash
git init
git add .
git commit -m "init: Поливокс синтезатор"
git remote add origin https://github.com/USERNAME/polivoks-android.git
git push -u origin main
```

### Шаг 3 — GitHub Actions собирает APK

Actions → Build Polivoks APK → Artifacts → `polivoks-release`

## Структура

```
app/src/main/
  assets/index.html    ← весь синтезатор
  java/.../MainActivity.java
  AndroidManifest.xml
```
