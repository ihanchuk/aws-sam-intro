| Команда | Описание |
|--------|----------|
| `sam init` | Создаёт новый SAM-проект из шаблона (Lambda, API Gateway, Step Functions). |
| `sam build` | Собирает функции, зависимости, Docker-образы, готовит артефакты для деплоя. |
| `sam validate` | Проверяет шаблон SAM/CloudFormation на ошибки. |
| `sam deploy` | Деплой приложения в AWS (через CloudFormation). Может быть guided. |
| `sam delete` | Удаляет задеплоенное SAM приложение (CloudFormation stack). |
| `sam local invoke` | Локально вызывает конкретную Lambda-функцию с тестовым событием. |
| `sam local start-api` | Эмулирует локальный API Gateway, позволяет тестировать REST API. |
| `sam local start-lambda` | Запускает локальное окружение LambdaRuntime API (для тестирования SDK). |
| `sam local generate-event` | Генерирует шаблон события (S3 event, API Gateway event, SNS и т.п.). |
| `sam local start-dynamodb` | Запускает локальную DynamoDB (через официальный AWS docker образ). |
| `sam logs` | Показывает CloudWatch Logs для Lambda-функций. |
| `sam traces` | Показывает AWS X-Ray traces (если включено). |
| `sam sync` | Быстро синхронизирует локальный код в облако (без полного деплоя). |
| `sam package` | Создаёт ZIP/образы и загружает в S3. Генерирует подготовленный CF шаблон. |
| `sam publish` | Публикует серверлесс-приложение в AWS Serverless Application Repository. |
| `sam pipeline init` | Создаёт пайплайн CI/CD (GitHub Actions, CodePipeline). |
| `sam pipeline bootstrap` | Подготавливает AWS-аккаунт для CI/CD (ролей, бакетов). |
| `sam pipeline deploy` | Деплой через пайплайн. |
| `sam list endpoints` | Показывает URL всех API после деплоя. |
| `sam list resources` | Список всех ресурсов стека SAM (Lambda, API, Bucket). |
