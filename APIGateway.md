> _APIGateway_ is a concept that enables you to manage your  `backend microservices` in a central location. It behaves as a proxy.

![apigateway2](https://user-images.githubusercontent.com/11644710/116974868-6ea97200-acc7-11eb-9667-30144df7ebb4.png)

![apigateway3](https://user-images.githubusercontent.com/11644710/116975894-05c2f980-acc9-11eb-95cf-45ea184b7d45.png)
***
### Advantages of APIGateway
- :fire: All microservices IP are private now. Microservices and APIGateway are in the same `secured network`
- :fire: Only APIGateway IP address is publicly exposed over internet. **That means less surface for attackers, more secure**
- ✔️ `Latency` problem is solved by `aggregate pattern`. Instead of making http call to each  microservices than aggreate these data
in frontend, we just make a http call to APIGateway and than it handles the rest. Since they are in the same secured network
it is much more performant
- ✔️ `Cross Cutting Concerns` can be implemented centrally.
- ✔️ `Authentication/Authorization` can be implemented on gateway centrally instead of implementing on each microservices. That saves us
from _lots of code duplication_ 
- ✔️ `Response caching`, `Retry/circuit breaker`(Call every 3 seconds if it fails, make 10 call in total),
- ✔️ `Load balancing`, `Logging/tracing`, `Query transformation`(add header to request for auth)
- ✔️ `IP Whitelisting`, `Rate limiting`(limit call to specific endpoints/microservices)
- ⚠️ The disadvantage of this mechanism is `Single Point Of Failure`. If our APIGateway is gone then our whole app will be crashed too
For this scenerio we can create multiple instance of APIGateway
