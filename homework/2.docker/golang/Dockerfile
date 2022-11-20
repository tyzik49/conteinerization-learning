FROM golang:1.16

WORKDIR /app

COPY go.mod go.sum ./
RUN go mod download && go mod verify

COPY . ./
RUN go build -o /app

EXPOSE 8080
CMD ["/app"]
