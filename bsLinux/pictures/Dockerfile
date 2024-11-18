FROM nginx:1.27

COPY ./dockerComposeKraken.jpg /usr/share/nginx/html
COPY ./dockerWhale.png /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]