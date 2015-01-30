FROM dockerfile/nodejs

ADD package.json /tmp/package.json
RUN cd /tmp && npm install
RUN mkdir -p /var/www/testapp && cp -a /tmp/node_modules /var/www/testapp/

WORKDIR /var/www/testapp

ADD . /var/www/testapp

EXPOSE 3000

CMD ["node", "bin/www"]
