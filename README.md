# library-gateway
Application utilizing spring cloud gateway to handle routing of services and authentication into the trusted domain. 

The gateway handles routing to the following services:
1. Book inventory service
2. checkout service
3. returns service
4. fines service
5. user auth service

All services by default are locked down through Spring Security. The userauth service authenticates over basic auth and provides a token with authorities in the claims. 
The token can then be provided to each call to authorize access to the resources by the authorities on the token.
