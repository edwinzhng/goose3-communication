FROM golang:latest

WORKDIR /wloop/test_client

RUN \
	go get github.com/waterloop/wcomms/wjson

COPY . .

ENV \
  POD_PORT=42000 \
  DATA_PORT=42000 \
  COMMAND_PORT=42001

EXPOSE $POD_PORT $DATA_PORT $COMMAND_PORT

CMD ["go", "run", "test_client.go"]