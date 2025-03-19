# Разработка Frontend-приложений

## Язык программирования и структура проекта

В качестве языка программирования используется javascript/typescript.

## Фреймворки

В качестве основного фреймворка используется Next.js на базе React.js. Для стилизации компонентов используется tailwind.css.

## Библиотеки

| **Решаемая задача** | **Название библиотеки** | **Ссылка на репозитарий и документацию**  |
| ------------------- | ----------------------- | ----------------------------------------- |
| Интернационализация | I18next                 | <https://github.com/i18next/next-i18next> |
| Линтер              | Eslint                  | <https://eslint.org>                      |
| Форматирование кода | prettier                | <https://prettier.io>                     |

## Основные положения

1. Прохождение Google Page Speed/Lighthouse - не ниже 95 баллов для мобильной и веб-версий
2. Использование PurgeCSS
3. css и js минифицируются
4. Наличие тёмной темы и корректное отображение в ней
5. Все сообщения локализованы
6. Дата и время отображаются с учетом локального времени пользователя
7. Поддержка accessibility standards - WCAG - [https://www.a11yproject.com/checklist/](https://www.a11yproject.com/checklist/)
8. Соответствие чеклисту - [thedaviddias/Front-End-Checklist](https://github.com/thedaviddias/Front-End-Checklist), [thedaviddias/Front-End-Design-Checklist](https://github.com/thedaviddias/Front-End-Design-Checklist) и [thedaviddias/Front-End-Performance-Checklist](https://github.com/thedaviddias/Front-End-Performance-Checklist)

## Вывод проекта в продакшн -- чеклист

### Внешние проекты

1. Наличие политики конфиденциальности
2. Наличие пользовательского соглашения
3. Наличие предупреждения о cookies
4. Соответствие GDPR - [The GDPR Checklist - Your GDPR compliance checklist](https://gdprchecklist.io)
5. Соответствие CCPA
6. Соответствие ФЗ-152 - [https://legal-box.ru/chek-list](https://legal-box.ru/chek-list) и [https://docshell.ru/personal-data/check_list_docs_proverka_rkn_pdn_urlitso/](https://docshell.ru/personal-data/check_list_docs_proverka_rkn_pdn_urlitso/)
7. Наличие шаблона для удаления персональных данных (применимо в случае запроса пользователем удаления персональных данных из системы)
8. Проверить по SEO-чеклисту - [https://backlinko.com/seo-checklist](https://backlinko.com/seo-checklist)
9. Проверить корректность заполнения robots.txt
10. Проверить наличие sitemaps
11. Проверить наличие permalinks
12. Проверить наличие и корректность meta-тегов
13. Проверить наличие и корректность open graph-тегов
14. Проверить наличие аналитики (GA, Metrika, Facebook Pixel), желательно в GTM
15. Добавить сайт в Yandex Webmaster
16. Добавить сайт в Google Search Console
17. Добавить сайт в Bing Webmaster Tools

### Внутренние проекты

TBD
