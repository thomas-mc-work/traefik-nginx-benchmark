# Traefik vs Nginx Benchmark

```
# initial startup
docker compose up -d

# Pure Whoami
wrk -t20 -c1000 -d3s -H "Host: benchmark.whoami" --latency  http://127.0.0.1:8080/bench

# Nginx
wrk -t20 -c1000 -d3s -H "Host: benchmark.whoami" --latency  http://127.0.0.1:8001/bench

# Traefik v2.9
wrk -t20 -c1000 -d3s -H "Host: benchmark.whoami" --latency  http://127.0.0.1:8029/bench

# Traefik v3.0
wrk -t20 -c1000 -d3s -H "Host: benchmark.whoami" --latency  http://127.0.0.1:8030/bench

# Traefik v3.3
wrk -t20 -c1000 -d3s -H "Host: benchmark.whoami" --latency  http://127.0.0.1:8033/bench

# Traefik v3.4-RC1
wrk -t20 -c1000 -d3s -H "Host: benchmark.whoami" --latency  http://127.0.0.1:8034/bench

# final shutdown
docker compose down
```