FROM node:8.5.0
ENV TZ=Asia/Tokyo
ENV APP_ROOT /usr/src/react-scheduler
RUN groupadd -g 500 ec2-user && useradd -g ec2-user -u 500 --create-home ec2-user

COPY . $APP_ROOT
RUN chown -R ec2-user:ec2-user $APP_ROOT

USER ec2-user
WORKDIR $APP_ROOT
RUN npm install

ENTRYPOINT ["npm","start"]