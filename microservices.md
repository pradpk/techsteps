
Microservices is an architechtural approach to develop applications which is by decomposing business domain models into services. These services are (supposed to be) small, autonomous and isolated, but provide a complete business functionality when they work together.

Advantages
- Freedom to develop and deploy independently.
- Services can be developed independently in any language.
- Easy implementation of continuous delivery.
- Easy to scale and re-use.
- Easy for containerization.
- Complement for cloud activities.
- Security issue is isolated as the applications are deployed on different servers.

Authorization and authentication
Since microservices are independent components, authorization and authentication for each component can be duplicated, but it creates a dependency during maintenance. Some of the solutions we can think of are :
- Sticky sessions: To ensure all requests from same user goes to same server. Disadvantage is if the user is shifted to different server, loses all of their session data.
- Session replication: synchronizing session through network, adds network overhead. 
- Centralized session storage: this needs to be well protected.
- Using tokens: Tokens are generated first time and will be sent to client. Client will store the tokens in the cookie and during subsequent requests, token will be validated with SSO agent or auth server. We can also have API gateway to handle the authentication and autorization with the token.


