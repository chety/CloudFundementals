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
 
