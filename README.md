oauth2-example-orion-client
===========================

Oauth2 authentication example for Orion Context Broker applications. The example shows how to send a 'version/' request,
this is the relevant part in server.js file:

```
        var optionsget = {
            host : 'orion.lab.fi-ware.eu',
            port : 1026,
            path : '/version',
            method : 'GET',
            headers: {
                'X-Auth-Token': auth_token
            }
        };
```

However, you can adapt this example to send more interesting NGSI request :)

## Running it

- Software requirements:

	+ nodejs 
	+ npm

- Install the dependencies: 

	npm install

- Configure OAuth2 credentials in config.js file (you will find theme in your IDM account)

- Start example server

	sudo node server

- Connect to http://localhost to try the example. You will see a text with the Orion Context Broker (running at 
  orion.lab.fi-ware.eu:1026) version string

* Connect to http://localhost/logout to delete session cookies once you have logout in IDM portal

