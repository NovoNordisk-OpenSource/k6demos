# K6 demo

Demo on using k6 for load testing and with custom extensions.  

## Prerequisites
https://docs.docker.com/get-docker/ <br />
https://learn.microsoft.com/en-us/windows/wsl/install <br />
https://go.dev/doc/install <br />

## Get XK6-OpenTelemetry extension
git clone https://github.com/thmshmm/xk6-opentelemetry.git && cd xk6-opentelemetry

## Compile new local k6 binary with extensions
xk6 build --with xk6-opentelemetry=. --with github.com/mostafa/xk6-kafka

## Run tests
./k6 run ../test-traces.js && ./k6 run ../api-test.js
