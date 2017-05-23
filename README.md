# Simple NGINX SII SSL Proxy

[NGINX Proxy Module](http://nginx.org/en/docs/http/ngx_http_proxy_module.html#proxy_ssl_certificate)

This allow us to use a AEAT valid certificate in a independent server to increment the **security**.

The webservice clients has to make requests againts the proxy
(with a valid SSL client provided by the proxy) and the proxy
will resend this request to the AEAT SII system with a valid
certificate.

## Running in a docker

```sh
docker run --name sii-proxy -v /path/nginx.conf:/etc/nginx/nginx.conf:ro \
  -v /path/ssl:/etc/nginx/ssl:ro -p 4443:443 nginx
