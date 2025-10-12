# 💁 Welcome 

📚 This is a list of definitions and their descriptions so that we can speak the same language within the Waveix.

## 📌 Prefix in repositories name:
- `be-` - Backend
- `bf-` - Backend For ... `aka API`
- `fe-` - Frontend
- `tv-` - TV For ...
- `ios-` - IOS For ...
- `android-` - Android For ...
- `mock-` - Mock Service
- `ops-` - Operations

## 📌 Suffix in repositories name:
- `-service` - Service, always works `aka deamon`. (Multi-tenant)
- `-job` - Job, work occasionally, or once `aka run app`. (Multi-tenant)
- `-worker` - Worker, runs on request. (Multi-tenant)
- `-app` - Personal Application. (Single-tenant)
- `-kit` - A set of utilities.
- `-schema` - Schema of interaction between services or layers.

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

