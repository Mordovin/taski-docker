FROM node:18

WORKDIR /app

COPY package.json package-lock.json ./

RUN npm ci

COPY . .

RUN npm run build

RUN rm -rf /frontend_static/* && mkdir -p /frontend_static && cp -r build/* /frontend_static
