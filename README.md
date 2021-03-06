Plista REST API Services
========================

How to use our REST based API services:

visit https://api.plista.com/statistics/docs/index.html

  * Click on the 'main' link - and you will be presented with the different URLs you are allowed to call, as well as the type of request you need to make
  * Select a URL you are interested it - some information appears including a 'Try it out' button
  * Select 'Try it out' - you will see some information - Important to note is the **Response Headers** section

  Pay attention to the *Access-Control-Allow-Headers* header - it tells us how we need to authenticate our REST requests:

##Authentication Option 1 
  * X-PLISTA-USER-EMAIL: your-email@address.com
  * X-PLISTA-USER-PASSSWORD : your-plista-password

##Authentication Option 2
  * X-PLISTA-USER-EMAIL: your-email@address.com
  * X-PLISTA-USER-TOKEN: your-md5-user-token-received-as-cookie-when-logged-in
  
##Authentication Option 3
  * Soon you will also be able to use a generated API Token to authenticate - it will be X-PLISTA-API-TOKEN

  When you supply these headers (either combination above), your request will be authenticated and you will be able to make requests and get valid responses.

##Testing the REST API Services
  * The interface provided under https://api.plista.com/statistics/docs/index.html provides you also the possibility to make actual API requests and see what the response would be. You are encouraged to play around with the tools provided and familiarize yourself with the response types and outputs.

##Versioning
  * As soon as it is not possible to change the API without breaking the backwards compatibility, the Minor version number will be increased. By this definition, adding new functions, will never lead to a number change.
  * As soon as the system changes in its structure, the Major number will be increased. An example could be the authorization system or switching between SOA and Rest
  * To specify which API version to use - note the versions availabe at the top of the interface
  * Specify the 'Accept' header to the version you need, ex. application/json will get the latest version. To use a specific version, ex. version 0.1 always, specify the following header:
  * Accept: application/vnd.plista.0.1+json
