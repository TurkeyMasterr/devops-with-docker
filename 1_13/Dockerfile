FROM golang:1.25-alpine AS builder

WORKDIR /usr/src/app
COPY . .

#ENV PORT=8080 \
#    REQUEST_ORIGIN=https://example.com \
#    REDIS_HOST=6379 \


RUN go build

# Verify installation
RUN go version

RUN go test ./...

EXPOSE 8080

CMD ["./server"]

