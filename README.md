<div align="center">

<!-- BANNER -->
<svg width="800" height="180" viewBox="0 0 800 180" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="bg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#0f0f0f"/>
      <stop offset="100%" style="stop-color:#1a1a2e"/>
    </linearGradient>
    <linearGradient id="accent" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" style="stop-color:#e63946"/>
      <stop offset="100%" style="stop-color:#ff6b6b"/>
    </linearGradient>
  </defs>
  <rect width="800" height="180" fill="url(#bg)" rx="12"/>
  <rect x="0" y="0" width="4" height="180" fill="url(#accent)" rx="2"/>
  <!-- Grid lines -->
  <line x1="50" y1="0" x2="50" y2="180" stroke="#ffffff08" stroke-width="1"/>
  <line x1="150" y1="0" x2="150" y2="180" stroke="#ffffff08" stroke-width="1"/>
  <line x1="250" y1="0" x2="250" y2="180" stroke="#ffffff08" stroke-width="1"/>
  <line x1="350" y1="0" x2="350" y2="180" stroke="#ffffff08" stroke-width="1"/>
  <line x1="450" y1="0" x2="450" y2="180" stroke="#ffffff08" stroke-width="1"/>
  <line x1="550" y1="0" x2="550" y2="180" stroke="#ffffff08" stroke-width="1"/>
  <line x1="650" y1="0" x2="650" y2="180" stroke="#ffffff08" stroke-width="1"/>
  <line x1="750" y1="0" x2="750" y2="180" stroke="#ffffff08" stroke-width="1"/>
  <!-- Tag -->
  <rect x="30" y="28" width="130" height="22" rx="4" fill="#e6394620"/>
  <text x="95" y="43" font-family="monospace" font-size="11" fill="#e63946" text-anchor="middle">CLAUDE SKILL v2.0</text>
  <!-- Title -->
  <text x="30" y="90" font-family="Georgia, serif" font-size="36" font-weight="bold" fill="#ffffff">detectAI</text>
  <text x="195" y="90" font-family="Georgia, serif" font-size="36" font-weight="bold" fill="#e63946">·</text>
  <text x="215" y="90" font-family="Georgia, serif" font-size="36" font-weight="bold" fill="#ffffff">humanizer-ru</text>
  <!-- Subtitle -->
  <text x="30" y="120" font-family="monospace" font-size="14" fill="#888888">Убирает ИИ из русских текстов. 40 паттернов.</text>
  <!-- Stats -->
  <rect x="30" y="140" width="80" height="24" rx="4" fill="#ffffff10"/>
  <text x="70" y="156" font-family="monospace" font-size="11" fill="#aaaaaa" text-anchor="middle">40 паттернов</text>
  <rect x="120" y="140" width="90" height="24" rx="4" fill="#ffffff10"/>
  <text x="165" y="156" font-family="monospace" font-size="11" fill="#aaaaaa" text-anchor="middle">2 прохода</text>
  <rect x="220" y="140" width="110" height="24" rx="4" fill="#ffffff10"/>
  <text x="275" y="156" font-family="monospace" font-size="11" fill="#aaaaaa" text-anchor="middle">калибровка голоса</text>
  <!-- Right decoration -->
  <text x="680" y="100" font-family="monospace" font-size="60" fill="#ffffff06">AI</text>
  <line x1="620" y1="50" x2="760" y2="50" stroke="#e6394615" stroke-width="1"/>
  <line x1="620" y1="130" x2="760" y2="130" stroke="#e6394615" stroke-width="1"/>
</svg>

<br/>

[![Telegram](https://img.shields.io/badge/Telegram-Digital--трафик-2CA5E0?style=flat-square&logo=telegram&logoColor=white)](https://t.me/trafficisobar)
[![Website](https://img.shields.io/badge/Сайт-pawetta.com-black?style=flat-square&logo=safari&logoColor=white)](https://pawetta.com)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)

</div>

---

## Что это

Claude skill, который убирает признаки ИИ-генерации из русскоязычных текстов и возвращает живой голос автора. Без воды, без «важно отметить», без «данного подхода».

Написан на основе реальных наблюдений за тем, как русскоязычные LLM портят тексты.

---

## Как работает

```
Входной текст (ИИ-слог)
        ↓
  Проход 1: 40 паттернов
  — канцелярит
  — пустые эпитеты
  — слова-паразиты
  — артефакты чат-бота
  — ритм и голос
        ↓
  Проход 2: антиИИ-аудит
  — чеклист из 7 пунктов
  — калибровка под голос автора
        ↓
Живой текст
```

---

## Пример

**До — ИИ:**

> Данный инструмент представляет собой инновационное решение, которое позволяет пользователям осуществлять эффективное управление задачами. В рамках текущего подхода система обеспечивает высокий уровень производительности. Важно отметить, что подобные решения являются неотъемлемой частью современного рабочего процесса. Таким образом, можно сделать вывод о том, что внедрение данного инструмента представляется целесообразным.

**После — человек:**

> Инструмент помогает управлять задачами. Работает быстро — мы проверили. Без него команда тратила на планирование два часа в неделю. Теперь — двадцать минут.

---

## Что убирает

| Блок | Паттерны |
|------|----------|
| **Канцелярит** | «данный», «является», «осуществляет», «в рамках», «обеспечивает», «реализация» |
| **Пустые слова** | «инновационный», «комплексный», «синергия», «релевантный», «проактивный» |
| **Заявки на важность** | «важно отметить», «следует подчеркнуть», «нельзя недооценивать» |
| **Переходы-паразиты** | «таким образом», «в целом», «более того», «стоит отметить» |
| **Артефакты бота** | «отличный вопрос», «рад помочь», «надеюсь, это было полезно» |
| **Ритм и голос** | одинаковые предложения, отсутствие позиции, симметрия, повтор-резюме |

---

## Установка

1. Скачай [`digitaltraffic-detectai.skill`](https://github.com/YAMAKAYAMACO/digitaltraffic-detectai/raw/main/digitaltraffic-detectai.skill)
2. В Claude.ai: **Settings → Skills → Install from file**
3. Готово

**Вызов:** `/digitaltraffic-detectai` или просто напиши «очеловечь текст» — скилл включится автоматически.

---

## Автор

**Никита Вихров** — маркетолог и SEO-специалист, 10+ лет в digital.

Специализация: SEO, перфоманс-маркетинг, трафик, который продаёт.  
Автор Telegram-канала [Digital-трафик](https://t.me/trafficisobar) — 24 000+ подписчиков.  
Кейсы, инструменты и калькуляторы: [pawetta.com](https://pawetta.com)

---

<div align="center">
<sub>Сделано с раздражением к канцелярному слогу © 2025</sub>
</div>
