FROM node:12-alpine
COPY . /app
WORKDIR /app
RUN npm config set registry http://registry.npm.taobao.org/ \
    && npm install 
CMD 'npm start'