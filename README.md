# Traefik vs Nginx Benchmark

```
# Traefik v3.0
wrk -t20 -c1000 -d3s -H "Host: benchmark.whoami" --latency  http://127.0.0.1:8000/bench

# Traefik v2.9
wrk -t20 -c1000 -d3s -H "Host: benchmark.whoami" --latency  http://127.0.0.1:8002/bench

# Nginx
wrk -t20 -c1000 -d3s -H "Host: benchmark.whoami" --latency  http://127.0.0.1:8001/bench

# Pure Whoami
wrk -t20 -c1000 -d3s -H "Host: benchmark.whoami" --latency  http://127.0.0.1:8003/bench
```