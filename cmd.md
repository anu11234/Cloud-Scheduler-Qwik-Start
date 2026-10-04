# Cloud Scheduler: Qwik Start || **GSP401**

**Command:**

```bash
gcloud pubsub topics create cron-topic && \
gcloud pubsub subscriptions create cron-sub --topic=cron-topic && \
gcloud scheduler jobs create pubsub my-scheduler-job \
    --schedule="* * * * *" \
    --topic=cron-topic \
    --message-body="hello cron!" \
    --location=us-east1
