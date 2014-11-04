Plista REST API Services
========================

How to use our REST based API services:

visit https://api.plista.com/statistics/docs/index.html

  * Click on the 'main' link - and you will be presented with the different URLs you are allowed to call, as well as the type of request you need to make
  * Select a URL you are interested it - some information appears including a 'Try it out' button
  * Select 'Try it out' - you will see some information - Important to note is the **Response Headers** section
  * Pay attention to the *Access-Control-Allow-Headers* header - it tells us how we need to authenticate our REST requests:
  * Option 1. 
    * X-PLISTA-USER-EMAIL: your-email@address.com
    * X-PLISTA-USER-PASSSWORD : your-plista-password
  * Option 2.
    * X-PLISTA-USER-EMAIL: your-email@address.com
    * X-PLISTA-USER-TOKEN: your-md5-user-token-received-as-cookie-when-logged-in

  * When you supply these headers (either combination 1. or 2. above), your request will be authenticated and you will be able to make requests and get valid responses.
  * Soon you will also be able to use a generated API Token to authenticate
