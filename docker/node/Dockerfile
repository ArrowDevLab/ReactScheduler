FROM node:6.12

ADD app /app_dev
WORKDIR /app_dev
RUN ls

RUN npm install

EXPOSE 3001

CMD ["node", "server.js"]
