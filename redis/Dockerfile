FROM redis:7-alpine

# No config file → redis binds all interfaces including IPv6 (required on
# Railway's private network). noeviction matches upstream compose — BullMQ
# queues must never be evicted. appendonly + a small volume at /data keeps
# queued jobs across restarts.
CMD ["sh", "-c", "redis-server --appendonly yes --maxmemory-policy noeviction --requirepass \"$REDIS_PASSWORD\""]
