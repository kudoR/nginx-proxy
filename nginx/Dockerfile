FROM jwilder/nginx-proxy
RUN sed -i 's|try_files $uri =404;|try_files $uri $uri/ /index.html;|' /app/nginx.tmpl
RUN { \
      echo 'server_tokens off;'; \
      echo 'client_max_body_size 20m;'; \
      echo 'proxy_buffer_size 128k;'; \
      echo 'proxy_buffers 4 256k;'; \
      echo 'proxy_busy_buffers_size 256k;'; \
    } > /etc/nginx/conf.d/my_proxy.conf