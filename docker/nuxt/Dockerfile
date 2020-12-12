FROM node:14.4.0-alpine3.12
WORKDIR /app
ENV NUXT_HOST 0.0.0.0
COPY ./frontend/package*.json ./
COPY ./frontend/.env.local ./.env
RUN npm ci
EXPOSE 3000
CMD ["npm", "run", "dev"]
