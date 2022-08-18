# liboauth
### Minimal C oauth 2.0 authentication ilbrary using libcurl

This library is insipred by https://github.com/slugonamission/OAuth2
but aims to add extra missing functionality like access token refresh, 
state saving, response caching, etc.
The project is now working but do expect bugs
and breaking API changes while the project matures.

### Working functionality

- [x] Syncronous API requests with request caching.
- [x] Compatibility with my URI scheme handler.
- [x] Supports all major API request types (PUT, PATCH, POST, GET, DELETE...)
- [x] State saving of "tokens" and other variables (simple .ini file)
- [x] Auto refresh "access token" with zero overhead for the user.

### Missing functionality

- [ ] Handling on auth callback different than
application/json (AKA XML)

- [ ] Add async request support for the same oauth
module with the same client_id. This may not work on some
APIs since they might limit incoming trafic but will be
usefull for many others.

- [ ] <b>IMPORTANT</b> Decent return type for the response. Currently the 
bare header and response are returned. The response code
and any errors should be handled.

- [ ] Simplification of the codebase for tighter
integration of the libraries used as well as general
bugfixing (remove all unnecessary libraries). 

- [ ] Compatibility with Windows/Linux/Apple

### Contributing

Any contribution is welcome and should be done through a pull request. Currently
help is mostly needed with request error handling and documentation.

### Cretit

Credit goes to:<br>
Rafa Garcia from https://github.com/rafagafe/tiny-json<br>
Ozan Tezcan from https://github.com/tezc/sc<br>
Rodion Efremov from https://github.com/coderodde/coderodde.c.utils<br>
for their amazing libraries.
