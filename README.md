# CDN Simulation with Nginx

This project simulates a CDN layer using Nginx in front of a Node.js API.

## Run

Start backend (repo 3):
node ../redis-caching-demo/index.js


Start nginx:
nginx -c $(pwd)/config/nginx.conf


## Test
curl -i http://localhost:8080/api/data
