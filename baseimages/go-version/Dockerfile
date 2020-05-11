#FROM google/golang as builder
FROM golang as builder
WORKDIR /go/src/app
COPY hello.go .
RUN go build -ldflags="-w -s" hello.go

FROM scratch
COPY --from=builder /go/src/app/hello /
CMD ["/hello"]
