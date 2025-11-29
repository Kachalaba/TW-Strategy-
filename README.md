# 📈 Kamamber (PRO) — SMC + Wyckoff Strategy

[![TradingView](https://img.shields.io/badge/TradingView-Pine%20Script%20v6-blue?logo=tradingview)](https://tradingview.com)
[![License](https://img.shields.io/badge/License-MPL%202.0-green)](https://mozilla.org/MPL/2.0/)

Профессиональная торговая стратегия для TradingView, объединяющая **Smart Money Concepts (SMC)** и **Wyckoff методологию**.

---

## ✨ Основные возможности

### 🔥 Smart Money Concepts
- **Multi-Timeframe Analysis** — анализ структуры на старшем ТФ (HTF) и текущем (LTF)
- **Liquidity Detection** — определение BSL (Buy-Side) и SSL (Sell-Side) ликвидности
- **BOS/CHOCH** — обнаружение Break of Structure и Change of Character
- **Fair Value Gaps (FVG)** — торговля имбалансов с Inversion логикой
- **Inducement (IDM)** — ловушки ликвидности
- **Supply/Demand Zones** — зоны предложения и спроса на HTF

### 📈 Wyckoff VSA Module
- **Volume Spread Analysis** — анализ объёма и спреда свечей
- **Climax Volume** — обнаружение экстремального объёма (потенциальные развороты)
- **Stopping Volume** — поглощение на ключевых уровнях
- **Spring/Upthrust** — ложные пробои с подтверждением
- **SOS/SOW** — Sign of Strength / Sign of Weakness
- **Phase Detection** — Accumulation, Distribution, Markup, Markdown

### 📊 Фильтры
- **VWAP** — дневной и недельный с σ-каналами
- **Market Mode** — TREND / RANGE / CHOPPY (ATR/StDev)
- **Volume Spikes** — фильтрация по перцентилю объёма
- **Kill Zones** — торговля в ключевых сессиях (Asia, London, NY AM, NY PM)
- **Trend Filter** — MA, HH/HL структура, ADX

### 🎯 Risk Management
- **Position Sizing** — Fixed Cash, Risk per Trade ($), Risk % of Equity
- **Multiple TP Modes** — Risk/Reward, Liquidity Target, Prioritized (TP1/TP2/TP3)
- **Partial Closes** — частичные закрытия на разных уровнях
- **Chandelier Stop** — trailing stop на основе ATR
- **Move SL to BE** — перевод стопа в безубыток после TP1

---

## 🚀 Установка

1. Открой [TradingView](https://tradingview.com)
2. Перейди в **Pine Editor**
3. Скопируй содержимое `strategy.pine`
4. Нажми **Add to Chart**

---

## 📁 Файлы

| Файл | Описание |
|------|----------|
| `strategy.pine` | Основная стратегия (SMC + Wyckoff) |
| `strategy_wyckoff.pine` | Standalone Wyckoff версия |
| `FVG_changes_summary.md` | Документация по FVG логике |

---

## ⚙️ Настройки

### 📈 Wyckoff Analysis
```
Enable Wyckoff Analysis    — включить модуль Wyckoff
Show VSA Labels           — показывать метки VSA (◆ ●)
Show Accumulation/Dist    — показывать зоны фаз
Climax Volume Multiplier  — порог для Climax (2.0x от среднего)
Range Detection Lookback  — окно для определения рейнджа (50 баров)
Spring Confirmation Bars  — бары для подтверждения Spring (3)
```

### 🎯 Wyckoff Signals
```
Trade Spring Setups       — торговать Spring (ложный пробой вниз)
Trade Upthrust Setups     — торговать Upthrust (ложный пробой вверх)
Trade Sign of Strength    — торговать SOS
Trade Sign of Weakness    — торговать SOW
Require Volume Confirm    — требовать подтверждение объёмом
```

### 🎨 Визуализация
```
Spring Color     — цвет меток Spring (#00d26a)
Upthrust Color   — цвет меток Upthrust (#ff6b6b)
Climax Color     — цвет Climax Volume (#d4a574)
Accumulation     — фон зоны аккумуляции
Distribution     — фон зоны дистрибуции
```

---

## 📊 Dashboard

Стратегия отображает информационную панель с:
- Тренд HTF/LTF
- HTF Supply/Demand зоны
- Статус сетапа
- Активная Kill Zone
- Текущая позиция
- VWAP Δ%
- Market Mode
- **Wyckoff Phase** (Accumulation/Distribution/Markup/Markdown)
- **Spring/Upthrust Status** (CONFIRMED/PENDING/—)

---

## 🔔 Алерты

- Вход в Kill Zone
- BUY/SELL сигналы с причиной
- Достижение TP1/TP2/TP3
- Перевод SL в безубыток
- Срабатывание Stop Loss

---

## 📖 Wyckoff VSA Паттерны

| Паттерн | Символ | Значение |
|---------|--------|----------|
| Climax Volume | ◆ | Экстремальный объём — потенциальный разворот |
| Stopping Volume | ● | Поглощение — остановка движения |
| SPRING | Label | Ложный пробой поддержки с восстановлением |
| UT | Label | Ложный пробой сопротивления с отказом |
| SOS | Label | Sign of Strength — подтверждение силы |
| SOW | Label | Sign of Weakness — подтверждение слабости |

---

## 📝 Changelog

### v2.0.0 — Wyckoff Integration
- ✨ Добавлен Wyckoff VSA модуль
- ✨ Добавлено определение Spring/Upthrust
- ✨ Добавлено определение фаз рынка
- ✨ Добавлены торговые сигналы Wyckoff
- 🎨 Обновлён Dashboard с Wyckoff информацией
- 📁 Добавлен standalone файл strategy_wyckoff.pine

### v1.0.0 — Initial Release
- 🚀 SMC стратегия с MTF анализом
- 📊 FVG/Imbalance логика
- 🎯 Multi-TP система

---

## 📜 Лицензия

[Mozilla Public License 2.0](https://mozilla.org/MPL/2.0/)

---

## 👤 Автор

**Kamamber0564**

---

*Disclaimer: Данная стратегия предоставляется "как есть" и не является финансовой рекомендацией. Торгуйте на свой риск.*
