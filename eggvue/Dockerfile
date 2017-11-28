FROM node
ARG CODE=https://github.com/hubcarl/egg-vue-webpack-boilerplate.git
RUN git clone $CODE code \
  && cd code \
  && npm i --registry=https://registry.npm.taobao.org \
  && npm i easywebpack-cli -g --registry=https://registry.npm.taobao.org \
  && npm run build-prod
CMD cd /code \
  && npm run start-prod
EXPOSE 7001

# docker run -t -i -p 7001:80 <image>