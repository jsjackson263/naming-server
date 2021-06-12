# naming server
spring-cloud-netflix Eureka Discovery Server for currency conversion microservices


## URLS

#### Eureka
- http://localhost:8761/

#### Zipkin
- http://localhost:9411/

#### Currency Exchange Service (direct call)
- http://localhost:8000/currency-exchange/from/USD/to/INR

#### Currency Conversion Service (direct call)
- http://localhost:8100/currency-conversion/from/USD/to/INR/quantity/10
- http://localhost:8100/currency-conversion-feign/from/USD/to/INR/quantity/10

#### API GATEWAY (call services behind the gateway)
- http://localhost:8765/currency-exchange/from/USD/to/INR
- http://localhost:8765/currency-conversion/from/USD/to/INR/quantity/10
- http://localhost:8765/currency-conversion-feign/from/USD/to/INR/quantity/10
- http://localhost:8765/currency-conversion-new/from/USD/to/INR/quantity/10

#### Commands
```
docker run -p 9411:9411 openzipkin/zipkin:2.23
watch -n 0.1 curl http://localhost:8000/sample-api
```
