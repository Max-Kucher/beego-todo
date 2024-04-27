FROM golang:1.22.2-bookworm

WORKDIR /app

# Копируем исходный код
COPY src/quickstart/ .

# Устанавливаем Beego и Bee
RUN go get github.com/beego/beego/v2@latest
RUN go get github.com/beego/bee/v2@latest
RUN go install github.com/beego/bee/v2@latest

ENV PATH="${PATH}:/go/bin"

RUN go mod tidy

EXPOSE 8080

CMD ["bee", "run"]
