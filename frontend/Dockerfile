FROM node:18

WORKDIR /app

COPY package.json package-lock.json ./

RUN npm ci

COPY . .

RUN npm run build

RUN mkdir -p /frontend_static && cp -r build/* /frontend_static/

