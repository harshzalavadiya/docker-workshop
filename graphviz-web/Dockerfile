FROM golang:alpine
WORKDIR /
ADD web.go .
RUN go build web.go

FROM alpine
COPY --from=0 /web .
COPY ./index.html .
CMD ["/web"]
