# sabre-handler
Nodejs Module for access SABRE SOAP and REST APIs (( Development fase ))

## Details
This module is yet under construction, so avoid to use it for now, just follow and when it's done you'll be noticed.

## Functionalities

- [x] REST.getToken() : Returns a valid Rest Auth Token ( with Refresh validation)
- [x] SOAP.getTokenStateless() : Returns an 'BinarySecurityToken'. Note that there are no stateless tokens on SABRE SOAP, this module emulates this behavior controlling the conversationId and idle status. DO NOT USE "SABRE AAA" WITH THIS TOKEN.
- [x] SOAP.getTokenStateful() : Returns an 'BinarySecurityToken' whith a given Conversation Id, If the token do not exists yet, a new one will be created.
- [x] SOAP.dismissToken() : Closes a given statefull token;
- [x] scheduled Token Sanitize : An schedule routine that refreshes existing tokens (SOAP & REST);
- [x] SOAP.getPayloadSchema() : Returns a JSON (converted from XML using xml2js) with the Payload schema;
  
  -this is actually in progress, the functionality is ready, but just some schemas are loaded in;

- [x] SOAP.sendPayload() : Sends an filled schema to SABRE and returns the response converted to JSON (with xml2js)

  -this is actually in progress, the functionality is ready, but just some schemas are loaded in;

## TODO
- [ ] Remove from payload tags and attributes not filled;
- [ ] Add All SOAP XML payloads templates;
- [ ] Control Idle time for statefull SOAP tokens end close automatically after 40 mins of inactivity;
- [ ] Control stateless SOAP tokens to avoid simultaneous use;



> PS: Pardon my English
