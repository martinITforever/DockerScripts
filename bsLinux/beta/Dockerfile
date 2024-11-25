FROM nginx:1.27

COPY ./index.html /usr/share/nginx/html
COPY ../stylesheets/style.css /usr/share/nginx/html/stylesheets

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]