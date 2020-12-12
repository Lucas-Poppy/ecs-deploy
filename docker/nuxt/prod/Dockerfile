FROM node:14.4.0-alpine3.12
WORKDIR /app
ENV NUXT_HOST 0.0.0.0
ENV NUXT_PORT=80
COPY ./frontend/ ./
COPY ./frontend/.env.prod ./.env
RUN npm ci
RUN npm run build
CMD ["npm", "run", "start"]
