# dane-assistant-pinger

Pings a personal server's `/health` endpoint every 10 minutes so the free hosting
tier doesn't put it to sleep. The server's URL is stored as the `PING_URL`
repository secret, not in this repo.

A run fails (and GitHub emails the owner) only if the server doesn't answer
after three tries over about five minutes. A monthly heartbeat commit keeps
GitHub from pausing the schedule.
