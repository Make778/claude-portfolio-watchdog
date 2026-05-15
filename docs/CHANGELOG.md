# Changelog

## [1.0.0] — 2026-05-16

### Initial release

#### Features
- 7 типов мониторинга: insider (SEC Form 4), analyst ratings,
  price movements, news (Claude-фильтр), earnings, macro, volatility.
- Ежедневная утренняя сводка в Telegram.
- Еженедельный PDF-отчёт на 10+ страниц с графиками
  (тёмная и светлая темы, акцентный цвет настраивается).
- Risk-аналитика: Beta, корреляции, max drawdown, VaR, концентрация.
- Performance vs benchmark, top movers, Sharpe.
- Claude Insights генератор для executive summary, position commentary,
  risk commentary, forward outlook, рекомендаций.
- IBKR CSV-импорт: Activity Statement / Flex Query / Portfolio Analyst /
  Simple — с авто-детектом формата.
- 4 GitHub Actions workflow: hourly monitor, daily summary, weekly PDF,
  demo (manual-only).
- Welcome-сообщение при первом запуске.
- Демо-режим с примерами всех типов уведомлений.
- Healthcheck-скрипт (`python -m src.healthcheck`).

#### Technical
- Python 3.11+, pydantic v2 для валидации config.
- anthropic ≥0.39, tenacity для retry, yfinance для рыночных данных,
  reportlab + matplotlib для PDF.
- pytest-тесты с моками внешних API.
- Black + Ruff в pre-commit; detect-secrets для предотвращения утечек.

#### Configurable
- Список тикеров, пороги, расписание cron, язык (ru/en), бенчмарк,
  таймзона, валюта, тема PDF, акцентный цвет, стиль Claude-insights.
