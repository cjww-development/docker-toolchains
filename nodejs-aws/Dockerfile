FROM bash:5.1.16-alpine3.15
RUN apk add --update nodejs npm
RUN npm install -g yarn
RUN apk add --no-cache aws-cli
RUN apk --no-cache add zip
RUN apk --no-cache add jq
RUN aws --version
CMD ["/usr/local/bin/bash"]
