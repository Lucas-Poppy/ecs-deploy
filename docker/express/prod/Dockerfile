FROM node:14.4.0-alpine3.12
WORKDIR /app
COPY ./backend/ ./
RUN npm ci
EXPOSE 8888
# 今回はnpm run devも startも同じだが開発環境のみnodemonを使っていることもあるため別のdockerfileを用意
CMD ["npm", "run", "start"]