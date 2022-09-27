FROM klakegg/hugo:0.101.0-alpine AS build
COPY . /src
RUN hugo build

FROM nginx:1.19.4-alpine
COPY --from=build /src/public /usr/share/nginx/html
EXPOSE 80