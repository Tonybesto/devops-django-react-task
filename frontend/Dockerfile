FROM node:10-alpine as build

COPY package.json  ./

RUN npm install && mkdir /frontend && mv ./node_modules ./frontend

WORKDIR /frontend

COPY . .

RUN npm run build


FROM nginx:alpine
WORKDIR /usr/share/nginx/html
RUN rm -rf ./*
COPY --from=build /frontend/build .
EXPOSE 3000 80
ENTRYPOINT ["nginx", "-g", "daemon off;"]