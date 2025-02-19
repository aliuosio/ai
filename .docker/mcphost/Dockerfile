ARG GO_IMAGE_VERSION
FROM golang:${GO_IMAGE_VERSION:-1.23.6-alpine3.21}

RUN apk update && \
    apk upgrade
    
RUN go install github.com/mark3labs/mcphost@latest

COPY .bashrc /root/.bashrc