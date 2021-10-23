# ref https://stackoverflow.com/questions/21866477/nginx-use-environment-variables

FROM nginx:1.17.8-alpine
COPY ./nginx.conf.template /nginx.conf.template

COPY cert.crt /etc/nginx/cert.crt
COPY cert.key /etc/nginx/cert.key

CMD ["/bin/sh" , "-c" , "envsubst < /nginx.conf.template > /etc/nginx/nginx.conf && exec nginx -g 'daemon off;'"]

# FROM nginx:1.19-alpine
# COPY nginx.conf /etc/nginx/nginx.conf
# COPY ./nginx.conf.conf /etc/nginx/templates/
# CMD ["/bin/sh" , "-c" , "exec nginx -g 'daemon off;'"]



# FROM nginx:1.19-alpine
# COPY nginx.conf /etc/nginx/nginx.conf
# COPY default.conf.conf /etc/nginx/templates/
# COPY cert.crt /etc/nginx/cert.crt
# COPY cert.key /etc/nginx/cert.key
# EXPOSE 443