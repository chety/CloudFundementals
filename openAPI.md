>  `OpenAPI` is a  specification  for documenting _REST APIs._ 
- 💻  Standard and language-agnostic way to describe a RESTful API.(Either in JSON or YAML)
-  Specification: A set of rules to do something.
- `Swagger` uses _Open API specification(Formerly known as Swagger specification)_ for documenting APIs
- `Swagger` is a set of open source tools build around OpenAPI Specification.(Swagger Codegen, Swagger UI)
- Why we need documentation of an API
	- 🥇 Available endpoints
	- 🥇 Available operations at each endpoint
	- 🥇 What parameters to pass and their data type
	- 🥇 What will the API return and the data type
	- 🥇 Authentication methods to use 


### Good API properties

- Limit the number of allowed API calls
   - Prevent DDOS attack by using throttling
- Caching response to improve performance
- Securing the API and providing access by gating access with API keys.
- Documentation
- Developer portal for on-boarding developers
- API analytics
- Last but not least transform APIs on the fly without code changes

`AZURE API Management` has above features to support your api management.It has `APIGATEWAY` which is basically works like a proxy on your backend APIs. 
**You call to APIGATEWAY and then it routes to the proper endpoint.**
