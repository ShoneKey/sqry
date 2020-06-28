FROM python:2.7
RUN wget https://nodejs.org/dist/v12.14.1/node-v12.14.1-linux-x64.tar.xz \
    && tar xf node-v12.14.1-linux-x64.tar.xz -C /opt/
ENV PATH=$PATH:/opt/node-v12.14.1-linux-x64/bin

COPY . /app
WORKDIR /app
RUN cat /etc/*-release && whoami \
    && npm config set registry http://registry.npm.taobao.org/ \
    && sudo rm -rf ~/.node-gyp \
    && npm cache clean -f \
    && npm install -g n \
    && n stable \
    && npm i --unsafe-perm
CMD npm run dev