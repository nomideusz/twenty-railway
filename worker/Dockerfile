FROM twentycrm/twenty:v2.20.0

# BullMQ worker: emails, imports, workflow runs. Migrations and cron
# registration stay on the server (upstream compose does the same).
ENV DISABLE_DB_MIGRATIONS=true \
    DISABLE_CRON_JOBS_REGISTRATION=true \
    STORAGE_TYPE=s3 \
    STORAGE_S3_REGION=auto

CMD ["yarn", "worker:prod"]
