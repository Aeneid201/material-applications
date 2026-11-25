#pull ubuntu
FROM ubuntu:24.04

#configure container dir
WORKDIR /usr/src/app

#expose container port
EXPOSE 8080

#update local packages and install golang
RUN apt-get update && apt install -y golang-go

#installing certificates
RUN apt-get install -y  ca-certificates

#copy files
COPY . .

RUN go build

CMD ["./server"]
