# Filename: Dockerfile 
FROM node:10-alpine as builder
WORKDIR /app
COPY package*.json .
RUN npm install
COPY . .
# CMD ["npm", "start"]

#stage 2
FROM nginx:1.19.0-alpine
WORKDIR /usr/share/nginx/html
RUN rm -rf ./*
COPY --from=builder /app/build .
ENTRYPOINT ["nginx", "-g", "daemon off;"]