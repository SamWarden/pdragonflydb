# pdragonflydb

This is a simple docker-compose setup for [Dragonfly](https://github.com/dragonflydb/dragonfly)

To launch Dragonfly server just run 

```bash
make up
```

The server will listen port `6378` to avoid conflict with Redis, though by default Dragonfly uses the same `6379`. You can specify the `PDRAGONFLYDB_PASSWORD` environment variable to secure the server. You will can connect to it using redis-cli

```bash
redis-cli -p 6378 -a pass
```

To remove container  run

```bash
make clean
```

To remove container with its volume run

```bash
make full_clean
```
