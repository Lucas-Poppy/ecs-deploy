FROM node:14.4.0-alpine3.12
WORKDIR /app
COPY ./backend/package*.json ./
RUN npm ci
EXPOSE 8888
CMD ["npm", "run", "dev"]