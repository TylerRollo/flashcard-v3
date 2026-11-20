FROM node:20-alpine AS build

WORKDIR /src

COPY package*.json ./
RUN npm ci || npm install

COPY . .

ENV HOST=0.0.0.0
ENV PORT=80

EXPOSE 80

CMD ["npm", "start"]


