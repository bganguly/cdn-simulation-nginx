# CDN Simulation with Nginx

This project simulates a CDN layer using Nginx in front of a Node.js API.

## Requirements

* NGINX
* curl
* Node.js 18+ (for the upstream backend in the Redis demo)

Install NGINX:

```bash
# macOS (Homebrew)
brew install nginx
```

Create NGINX temp directories used by config:

```bash
mkdir -p /tmp/nginx_client_temp /tmp/nginx_proxy_temp /tmp/nginx_fastcgi_temp /tmp/nginx_uwsgi_temp /tmp/nginx_scgi_temp /tmp/nginx_cache
```

## Run

Start backend (repo 3):
node ../redis-caching-demo/index.js


Start nginx:
nginx -c $(pwd)/config/nginx.conf


## Test
curl -i http://localhost:8080/api/data
