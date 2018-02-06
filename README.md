# Dockerized Logrotate

## How to run

* Your logrotate config files should be mapped in the `/etc/logrotate.d` inside the container
* The cron job will run daily at 00:00:00 UTC time by default. You can override the cron schedule by overwriting the `CRON_SCHEDULE` environment variable.
* Run the following to run the docker container.

```bash
    docker run -d -v $(pwd)/config/:/etc/logrotate.d/ stakater/logrotate
```

## References

* How to write a logrotate config file: https://serversforhackers.com/c/managing-logs-with-logrotate