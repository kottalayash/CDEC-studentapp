FROM ubuntu:latest
RUN apt update && apt install nodejs npm -y

COPY . /app
WORKDIR /app
RUN npm install
RUN npm run build

RUN apt install nginx -y
RUN cp -r /app/dist/* /usr/share/nginx/html/
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]