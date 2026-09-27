# Серверне вебпрограмування — загальні правила

Дисципліна організована як робота невеликих команд над реальними серверними проєктами.
Кожна команда створює один ASP.NET Core API; кожен студент має власні задачі та власні бали.

| Команда | Репозиторій | Предметна область |
|---|---|---|
| Team 1 | [team-01-university](../team-01-university) | University Management API |
| Team 2 | [team-02-hotel](../team-02-hotel) | Hotel Booking API |
| Team 3 | [team-03-library](../team-03-library) | Library Management API |
| Team 4 | [team-04-clinic](../team-04-clinic) | Clinic Appointment API |
| Team 5 | [team-05-store](../team-05-store) | Online Store / Warehouse API |

Стек: ASP.NET Core 10, EF Core 10, PostgreSQL 17, JWT, SignalR, xUnit + Testcontainers, Docker, GitHub Actions.

Повний опис організації курсу — [docs/organizatsiya.txt](docs/organizatsiya.txt).

## Робочий цикл

1. Відкрийте дошку своєї команди, виберіть задачу в **Ready**.
2. Призначте issue на себе, перемістіть у **In Progress**.
3. `git switch dev && git pull && git switch -c feat/<номер>/<опис>`
4. Реалізуйте задачу разом із тестами.
5. PR у `dev` з `Closes #<номер>`, заповніть чекліст, перемістіть у **Review**.
6. Попросіть одногрупника про рев'ю, виправте зауваження.
7. Рев'ю викладача → короткий усний захист → squash merge → **Done**.

Деталі — у `CONTRIBUTING.md` вашого репозиторію.

## Правила

- **WIP-ліміт:** максимум 1 задача в In Progress і 1 у Review на студента.
- **7 днів** без коміту або PR — задача повертається в Ready.
- **Не більше 3 захистів** за одне заняття — не відкладайте все на кінець.
- **Міграції EF Core** — у PR тієї задачі, що змінює модель; перед merge — rebase на `dev`.
- **AI дозволено**, але задача зараховується лише після захисту: ви маєте пояснити кожен рядок.

## Бали

| Розмір | Бали | Приклади |
|---|---|---|
| S | 1 | health checks, сутність + міграція, Swagger UI |
| M | 2 | CRUD-контракт, EF-реалізація сервісу, зв'язок 1:N, upload файлу |
| L | 3 | JWT login, refresh-токени, SignalR hub, Docker Compose |
| XL | 5 | складна бізнес-логіка: конкурентність, резервування, розклад |

## Оцінювання

| Частина | Вага | Як рахується |
|---|---|---|
| Індивідуальні Task Points | 70 | 22 бали і більше = 70; менше — пропорційно. Для максимуму — задачі з ≥ 5 категорій, інакше не більше 56 |
| Командний проєкт | 20 | збирається і тести зелені (5), `docker compose up` працює (5), демо-сценарій (5), якість і документація (5) |
| Підсумковий захист | 10 | індивідуальна розмова про ваш код |

Категорії: `http`, `api`, `ef-core`, `database`, `architecture`, `security`, `testing`, `docker`, `signalr`, `files`.

## Спринти

| Спринт | ЛР | Тема |
|---|---|---|
| S1 | ЛР1 | Проєкт та HTTP API |
| S2 | ЛР2 | REST endpoints (контракт, in-memory) |
| S3 | ЛР3 | EF Core і PostgreSQL |
| S4 | ЛР4 | Складніша модель даних |
| S5 | ЛР5 | Архітектура і бізнес-логіка |
| S6 | ЛР6 | Middleware, помилки, логування |
| S7 | ЛР7 | Authentication / Authorization |
| S8 | ЛР8 | SignalR, файли, тести |
| S9 | ЛР9 | Docker, CI/CD, фінальний захист |
