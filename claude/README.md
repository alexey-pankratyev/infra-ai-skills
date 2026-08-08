# Claude Agent Skills

13 скилов в формате Agent Skills (open standard). Каждый скил — папка с `SKILL.md`,
у которого валидный YAML-фронтматтер (`name`, `description`) и markdown-инструкция.

## Состав

| Скил | Назначение |
|------|------------|
| infra-cloud-architect | Инфраструктура и облачные архитектуры (K8s, Terraform, Crossplane, Flux, CI/CD, AI/ML infra) |
| executive-orchestrator | Оркестратор: кросс-функциональные задачи → одно решение |
| ceo-founder-advisor | Бизнес-стратегия, модель, GTM, unit-экономика, инвесторы |
| cto-technology-advisor | CTO-стратегия, архитектура, build-vs-buy, надёжность, команда |
| web-architecture | Веб-инженерия: фронт/бэк, API, БД, распределённые системы |
| frontend-design | UI/UX, типографика, композиция, доступность |
| print-graphic-design | Полиграфия и препресс (CMYK, DPI, bleed, PDF) |
| product-management | Продакт/проджект: discovery, роадмапы, приоритизация, OKR |
| business-data-analytics | Аналитика: KPI, SQL, воронки, когорты, A/B, прогнозы |
| economics-finance | Экономика и финансы: DCF, NPV/IRR, сценарии, бюджеты |
| creative-brand-strategy | Креатив и бренд: позиционирование, кампании, копирайт |
| assumption-challenger | Стресс-тест допущений, поиск слабых мест и рисков |
| decision-analysis | Структурный выбор из альтернатив по критериям |

## Установка

### Claude Code
Папки-скилы кладутся напрямую (zip не нужен):

    cp -r claude/* ~/.claude/skills/          # персональные, во всех проектах
    cp -r claude/* <project>/.claude/skills/  # только в одном проекте

### claude.ai (веб/приложение)
Каждый скил загружается отдельным zip: `Settings → Capabilities` включить
«Code execution and file creation», затем `Customize → Skills → +`.
Заархивировать по одному:

    cd claude && for d in */; do zip -r "../${d%/}.zip" "$d"; done

(в архиве папка скила должна лежать в корне — как здесь).

### Claude API
Загрузка через `/v1/skills` (нужен code execution tool и бета-заголовки
`skills-2025-10-02`, `files-api-2025-04-14`).
