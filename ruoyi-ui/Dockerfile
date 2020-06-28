FROM python:2.7
RUN wget https://nodejs.org/dist/v12.14.1/node-v12.14.1-linux-x64.tar.xz \
    && tar xf node-v12.14.1-linux-x64.tar.xz -C /opt/
ENV PATH=$PATH:/opt/node-v12.14.1-linux-x64/bin

COPY . /app
WORKDIR /app
RUN cat /etc/*-release && whoami \
    && npm config set registry http://registry.npm.taobao.org/ \
    && npm install --unsafe-perm
CMD npm start