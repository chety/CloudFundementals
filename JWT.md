> Json Web Token(JWT) is a secure method to provide `authorization`.
- ⚠️ `JWT` is not used for `authentication`, only for `authorization`

### Sessions
Before `JWT` basically sessions were used. Here are the sessions details 
- First You login to your system with a username and a password. Server saves a unique session id
 with your infos in its memory if your are a valid user. Then this session-id is sent back to your browser
- Session id will be stored in browser via `cookies`
- After that with every request your session-id will be sent along the request. Server will search session-id
whether if it has in memory. If it has it will grap your information from memory and then authorize client.

### Drawbacks
- ⚠️ If the system we use has more than one server(obviously) , There will be sync problem between servers' session
storages. If our infos are saved in a server and this server crashes, we will have to login again in another system's server
just because this new server does not have our session-id

![cookie](https://user-images.githubusercontent.com/11644710/117159131-b5cb5c00-adc8-11eb-9fb3-9847d9acf10b.png)

***
 ### JWT(JSON Web Tokens)
 
 - JWT uses web tokens. When you login a system, your info  are `encoded`,`serialized` by the server and then send back to you
 - Your json token is saved in your browser. But there is nothing saved in the server.
 - If you send another request, your json token will be sent with your request.
 - Server will check your jwt if it is valid or not. And grap your infos from token. No information is saved in server
 - If you change anything with your token, server will check and find the problem and refuse you.

### Advantages
 - You are independent from servers. There is no such a server sync problems
 - If your app has lots of servers then again no problem. Because all the information is saved in client browser
 - No server delay when checking and grabbing user information from memory

![jwt](https://user-images.githubusercontent.com/11644710/117170826-034cc680-add3-11eb-8fc1-399d59722f35.png)

