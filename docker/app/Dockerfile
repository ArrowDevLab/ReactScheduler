FROM node:8.5.0
ENV TZ=Asia/Tokyo
ENV APP_ROOT /app

COPY ../../:$APP_ROOT

WORKDIR $APP_ROOT
RUN npm install

ENTRYPOINT ["npm","start"]