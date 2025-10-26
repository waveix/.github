# 💁 Welcome 

📚 This is a list of definitions and their descriptions so that we can speak the same language within the Waveix.

## 📌 Prefix in repositories name:
- `be-` - Backend
- `bf-` - Backend For ... `aka API`
- `fe-` - Frontend
- `tv-` - TV
- `ios-` - IOS
- `android-` - Android
- `ops-` - Operations `aka CI/CD etc.`

## 📌 Suffix in repositories name:
- `-schema` - Schema of interaction between services or layers.
- `-kit` - A set of utilities.
- `-app` - Personal Application. (Single-tenant)
- `-worker` - Worker, runs on request. (Multi-tenant)
- `-job` - Job, work occasionally, or once `aka run app`. (Multi-tenant)
- `-service` - Service, always works `aka deamon`. (Multi-tenant)

## 📓 Definitions:

- 👉 `Serverless` - ты не управляешь серверами, провайдер делает это за тебя.
Обычно это FaaS (functions-as-a-service), где функции запускаются по событию и масштабируются автоматически.
Состояние (state) чаще всего хранится внешне — в базе, S3, Redis и т.д.
- 👉 `Serverful` - ...

- 👉 `Stateless` - не хранит состояние (каждый запрос независим). Это характеристика самого приложения.
Stateless-приложение = не хранит данные сессии/состояния внутри себя, каждая операция обрабатывается независимо.
Пример: HTTP API, где всё состояние хранится в базе или cache.
Легко масштабируется: можно запустить 10 копий, и они все одинаковы.
👉 Главное: не помнит прошлых запросов, состояние хранится вне процесса.
- 👉 `Stateful` - хранит состояние (сессии, соединения, данные). хранит состояние (например, сессии, соединения, кэш) внутри себя.
Примеры: Базы данных (PostgreSQL, MongoDB), Stateful-сервисы (Kafka broker, Redis).
Масштабировать сложнее: нужна синхронизация состояния между инстансами.
👉 Главное: помнит прошлое, зависит от своего состояния.

- 👉 `Single-tenant` - ...
- 👉 `Multi-tenant` - одна система обслуживает несколько клиентов (например, SaaS для разных компаний).

- 👉 `Idempotent` - операция, которую можно выполнить несколько раз без побочных эффектов (например, PUT /resource в REST).
- 👉 `High Availability` - устойчивая система с резервированием.
- 👉 `Elastic scaling` - автоматическое увеличение/уменьшение ресурсов.
- 👉 `Fault tolerance` - система продолжает работать при сбоях.

## Repository List:

1. 👤 `be-user-service` - User Service (SSO, Auth, Roles, etc.), use: Ory Krakos, Hydra

2. 🎬 `be-catalog-service-schema` - Catalog GraphQL API (Scheme and Types for Go and NPM Managers)
3. 🎬 `be-catalog-service` - Catalog Service (Movies, Series, TV shows, TV networks, etc.)
4. 🎬 `be-catalog-sitemap-job` - Catalog Job Sitemap (Manage Sitemap Files)
5. 🎬 `be-catalog-data-provider-job` - Catalog Job Data Provider (Fetching from TMDB, IMDb, JustWatch, etc.)

6. 📊 `be-user-service-stats` - User Service Stats (Actions, History, Like, etc.)

7. 🎲 `be-recsys-service-schema` - Recommender system GraphQL API (Scheme and Types for Python and NPM Managers)
8. 🎲 `be-recsys-service` - Recommender system Service
9. 🎲 `be-recsys-ml-job` - Recommender system Job, gym for Model (Machine Learning)

10. 🤑 `be-payment-service` - Payment Service (Gateway for handling payments)

11. 👁️ `be-ad-service-schema` - Catalog GraphQL API (Scheme and Types for Go and NPM Managers)
12. 👁️ `be-ad-service` - Ad Service (Advertising, Banners, Roles, etc.)

13. 🎞️ `be-video-converter-job` - Video Job Converter (Video file prepare slice Video file)

14. 🚀 `fe-vod-worker` - Video on Demand (Distribution, CDN, etc.)
15. 🚀 `fe-iod-worker` - Image on Demand (Distribution, CDN, etc.)

16. 🏢 `bf-back-office-worker-schema` - Back Office API GraphQL (Scheme and Types for Go and NPM Managers)
17. 🏢 `bf-back-office-worker` - Backend for Back Office (API Gateway to Services via GraphQL Federation)
18. 🏢 `fe-back-office-worker` - Manages Website Waveix (Single-Page Application, SPA)

19. 🍿 `bf-front-office-worker-schema` - Front Office API GraphQL (Scheme and Types for Go and NPM Managers)
20. 🍿 `bf-front-office-worker` - Backend for Front Office (API Gateway to Services via GraphQL Federation)
21. 🍿 `fe-front-office-worker` - Website Waveix (Multi-Page Application, MPA)

22. 🤖 `bf-mcp-worker` - Backend for MCP (API Gateway to Services via GraphQL Federation)

23. 💼 `go-pkg-kit` - Golang Package Kit
24. 💼 `ts-pkg-kit` - TypeScript Package Kit
25. 💼 `ops-kit` - Operation Kit for Security, Development and Operations (Security by Design)
