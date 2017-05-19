# Simple NGINX SII SSL Proxy

[NGINX Proxy Module](http://nginx.org/en/docs/http/ngx_http_proxy_module.html#proxy_ssl_certificate)

## Running in a docker

```sh
docker run --name sii-proxy -v /path/nginx.conf:/etc/nginx/nginx.conf:ro \
  -v /path/ssl:/etc/nginx/ssl:ro -p 4443:443 nginx
