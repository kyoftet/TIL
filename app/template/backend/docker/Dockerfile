FROM golang:1.24-alpine

WORKDIR /app

RUN curl -sSf https://atlasgo.sh | sh

RUN go install github.com/air-verse/air@latest

COPY go.mod go.sum ./
RUN go mod download

CMD ["air", "-c", ".air.toml"]
