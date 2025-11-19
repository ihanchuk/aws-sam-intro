### Ограничения при работе с Лямбдами

# Лимиты AWS Lambda

# Лимиты AWS Lambda (проверено по официальной документации)

| Ресурс / Параметр | Лимит | Примечания / источник |
|---|---:|---|
| **Память (Memory)** | **128 MB – 10 240 MB** | Memory влияет на CPU; можно задавать с шагом 1 MB. :contentReference[oaicite:0]{index=0} |
| **Макс. время выполнения (Timeout)** | **15 минут (900 сек)** | Жёсткий верхний предел. :contentReference[oaicite:1]{index=1} |
| **Ephemeral storage (/tmp)** | **512 MB – 10 240 MB** | Можно настраивать в 1-MB шагах; данные временные (очищаются при терминации окружения). :contentReference[oaicite:2]{index=2} |
| **Synchronous invocation payload (Invoke, sync)** | **6 MB** | Ограничение при синхронных вызовах (API/Gateway/SDK). :contentReference[oaicite:3]{index=3} |
| **Asynchronous invocation payload (Invoke, async)** | **1 MB (с 24 Oct 2025)** | AWS увеличил лимит асинхронного payload с 256 KB до 1 MB — учитывай ограничения downstream (например, SNS может иметь свои лимиты). :contentReference[oaicite:4]{index=4} |
| **ZIP (compressed) при прямой загрузке** | **50 MB** | При загрузке через консоль/API/SDK: 50 MB. Для больших файлов используйте S3. :contentReference[oaicite:5]{index=5} |
| **Uncompressed (развёрнутый) пакет (code + deps + layers)** | **250 MB (unzipped)** | Общий развёрнутый объём кода и слоёв. :contentReference[oaicite:6]{index=6} |
| **Container image** | **10 GB** | Если деплоишь Lambda как контейнерный образ. :contentReference[oaicite:7]{index=7} |
| **Размер переменных окружения (все вместе)** | **~4 KB (документ: 4 KB)** | Суммарный объём всех env-переменных ограничен (официально указано 4 KB). :contentReference[oaicite:8]{index=8} |
| **Concurrent executions (по умолчанию)** | **1000 (soft limit, регионально)** | Этот квот можно запросить увеличить; для отдельных функций — Reserved Concurrency. (см. Service Quotas). :contentReference[oaicite:9]{index=9} |
| **Max number of layers attached** | **5 layers** | Ограничение на число слоёв у функции. (см. общие лимиты) |
| **/tmp (file descriptors / processes)** | **специфично для runtime; FD/threads ограничены** | Практически: следи за file descriptors / thread usage (н-р, 1024). |

