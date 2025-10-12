# Welcome to the team 🙌

## Prefix in repositories name

`be-` - Backend

`bf-` - Backend For ... `aka API`

`fe-` - Frontend

`ios-` - For IOS

`android-` - For Android

`tv-` - For TV

`mock-` - Mock Service

`ops-` - Operations

## Suffix in repositories name

`-service` - Service, always works `aka deamon`. (Multi-tenant)

`-job` - Job, work occasionally, or once `aka run app`. (Multi-tenant)

`-worker` - Worker, runs on request. (Multi-tenant)

`-app` - Personal Application. (Single-tenant)

`-schema` - Schema of interaction between services or layers.

`-kit` - A set of utilities.

---

Stateless/Stateful = характер приложения (хранит ли оно состояние).

Serverless = модель развертывания (не думаешь о серверах).
Stateless → не хранит состояние (каждый запрос независим).
Stateful → хранит состояние (сессии, соединения, данные).
Idempotent → операция, которую можно выполнить несколько раз без побочных эффектов (например, PUT /resource в REST).
Multi-tenant → одна система обслуживает несколько клиентов (например, SaaS для разных компаний).
Elastic scaling → автоматическое увеличение/уменьшение ресурсов.
High Availability (HA) → устойчивая система с резервированием.
Fault tolerance → система продолжает работать при сбоях.


Serverless  👉 Архитектурная модель: ты не управляешь серверами, провайдер делает это за тебя.
Обычно это FaaS (functions-as-a-service), где функции запускаются по событию и масштабируются автоматически.
Состояние (state) чаще всего хранится внешне — в базе, S3, Redis и т.д.

Stateless
Это характеристика самого приложения.
Stateless-приложение = не хранит данные сессии/состояния внутри себя, каждая операция обрабатывается независимо.
Пример: HTTP API, где всё состояние хранится в базе или cache.
Легко масштабируется: можно запустить 10 копий, и они все одинаковы.
👉 Главное: не помнит прошлых запросов, состояние хранится вне процесса.

Stateful
Противоположность stateless.
Stateful-приложение = хранит состояние (например, сессии, соединения, кэш) внутри себя.
Примеры: Базы данных (PostgreSQL, MongoDB), Stateful-сервисы (Kafka broker, Redis).
Масштабировать сложнее: нужна синхронизация состояния между инстансами.
👉 Главное: помнит прошлое, зависит от своего состояния.

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
👀 Contribution guidelines - how do team members dive in?
👩‍💻 Useful resources - where do you keep your docs? Is there anything else the team should know?
🍪 Fun facts - what is your team's favorite snack?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
