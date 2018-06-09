FROM node:carbon

RUN apt-get update

WORKDIR /app

RUN git clone https://github.com/wtfdiov/sammy-app && \
    npm install --production && \
    npm run build

FROM nginx:1.13

COPY --from=0 /usr/src/app/build /usr/share/nginx/html

CMD ["nginx", "-g", "daemon off;"]
