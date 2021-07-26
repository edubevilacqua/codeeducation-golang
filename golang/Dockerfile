FROM golang as builder

COPY ./main.go /go
RUN go build main.go

FROM scratch

COPY --from=builder /go/main .
CMD ["./main"]

