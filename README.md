
## UPP REST API Documentation

UPP REST APIs provide programmatic access to read, update and delete various UPP objects.  

The REST API is based on open standards and are protected with HTTP Basic authentication.All responses are in JSON format.  

It allows developers to seamlessly integrate UPP accounts, deals, followups, products, orders, tickets and custom objects into their application.

### Authentication

Upp REST APIs requires a valid API key to authenticate your request. Only an account administrator can access or generate API Key.   

In your HTTP request header, use **api-key** parameter to specify the API key.  

#### Following guide explains how to generate an API key

* In console, click on user icon, Settings -> API Access. "Team API Access" popup will be displayed.  
![apikey_setting](https://github.com/UppCRM/UppApiDocs/wiki/images/apikey_setting.png)
* Click on "Generate NEw Key", button. API KEY will be generated.
* Select the "user".
* Make sure you fill all the mandatory details and click save button.  
![apikey_dialog](https://github.com/UppCRM/UppApiDocs/wiki/images/apikey_dialog.png)
* API KEY will be generated successfully.

### Example to get list of accounts
**Url** - http://app.upp.io/rest/v1/accounts/

**Method** - GET

### Response
	{
		"success": true,
		"errors": null,
		"result":{
			"data":[{
				"id": "58a6b00d4de5a86115229489",
				"companyName": "Account1",
				"name": "acc1",
				"email": "account1@demo.com",
				"phone": "+31-123-456-789",
				"image": "account1.png",
				"address": {
					"street": "Gabberstraat",
					"streetNumber": "32A",
					"postcode": "3283BV",
					"city": "Amsterdam",
					"country": "Nederlands"
				},
				"noDeals":"4",
				"noActivity": "3",
				"noContacts": "6",
				"customFields": [
					{
						identifier: "transactionsThisMonth",
						value: 20
					}
				],
				"createdOn": "ISODate("2016-09-03T09:01:53.354Z")",
				"modifiedOn": "ISODate("2016-09-03T09:01:53.354Z")"
			},{
				"id": "58a6b00d4de5a8611522948b",
				"companyName": "Account2",
				"name": "acc2",
				"email": "account2@demo.com",
				"phone": "+31-123-456-789",
				"image": "account2.png",
				"address": {
					"street": "Gabberstraat",
					"streetNumber": "32B",
					"postcode": "3283BV",
					"city": "Amsterdam",
					"country": "Nederlands"
				},
				"noDeals":"3",
				"noActivity": "4",
				"noContacts": "3",
				"customFields": [
					{
						identifier: "transactionsThisMonth",
						value: 50
					}
				],
				"createdOn": "ISODate("2016-09-03T09:01:53.354Z")",
				"modifiedOn": "ISODate("2016-09-03T09:01:53.354Z")"
			}],
			"total":2,
			"limit":0,
			"skip":0
		}
	}

### Accounts API
* [GET accounts - List existing accounts](https://github.com/UppCRM/UppApiDocs/wiki/API-Account-Get)
* [GET accounts/:id - Get information about an existing account](https://github.com/UppCRM/UppApiDocs/wiki/API-Account-Details)
* [POST accounts - Create a new account](https://github.com/UppCRM/UppApiDocs/wiki/API-Account-Create)
* [PUT accounts/:id - Update an existing account](https://github.com/UppCRM/UppApiDocs/wiki/API-Account-Update)
* [DELETE accounts/:id - Remove an existing account](https://github.com/UppCRM/UppApiDocs/wiki/API-Account-Delete)

### Deals API
* [GET deals - List existing deals](https://github.com/UppCRM/UppApiDocs/wiki/API-Deal-Get)
* [GET deals/:id - Get information about an existing deal](https://github.com/UppCRM/UppApiDocs/wiki/API-Deal-Details)
* [POST deals - Create a new deal](https://github.com/UppCRM/UppApiDocs/wiki/API-Deal-Create)
* [PUT deals/:id - Update an existing deal](https://github.com/UppCRM/UppApiDocs/wiki/API-Deal-Update)
* [DELETE deals/:id - Remove an existing deal](https://github.com/UppCRM/UppApiDocs/wiki/API-Deal-Delete)

### Products API
* [GET products - List existing products](https://github.com/UppCRM/UppApiDocs/wiki/API-Product-Get)
* [GET products/:id - Get information about an existing product](https://github.com/UppCRM/UppApiDocs/wiki/API-Product-Details)
* [POST products - Create a new product](https://github.com/UppCRM/UppApiDocs/wiki/API-Product-Create)
* [PUT products/:id - Update an existing product](https://github.com/UppCRM/UppApiDocs/wiki/API-Product-Update)
* [DELETE products/:id - Remove an existing product](https://github.com/UppCRM/UppApiDocs/wiki/API-Product-Delete)

### Orders API
* [GET orders - List existing orders](https://github.com/UppCRM/UppApiDocs/wiki/API-Order-Get)
* [GET orders/:id - Get information about an existing order](https://github.com/UppCRM/UppApiDocs/wiki/API-Order-Details)
* [POST orders - Create a new order](https://github.com/UppCRM/UppApiDocs/wiki/API-Order-Create)
* [PUT orders/:id - Update an existing order](https://github.com/UppCRM/UppApiDocs/wiki/API-Order-Update)
* [DELETE orders/:id - Remove an existing order](https://github.com/UppCRM/UppApiDocs/wiki/API-Order-Delete)

### Tickets API
* [GET tickets - List existing tickets](https://github.com/UppCRM/UppApiDocs/wiki/API-Ticket-Get)
* [GET tickets/:id - Get information about an existing ticket](https://github.com/UppCRM/UppApiDocs/wiki/API-Ticket-Details)
* [POST tickets - Create a new ticket](https://github.com/UppCRM/UppApiDocs/wiki/API-Ticket-Create)
* [PUT tickets/:id - Update an existing ticket](https://github.com/UppCRM/UppApiDocs/wiki/API-Ticket-Update)
* [DELETE tickets/:id - Remove an existing ticket](https://github.com/UppCRM/UppApiDocs/wiki/API-Ticket-Delete)

### Activity API
* [GET activity - List existing tickets](https://github.com/UppCRM/UppApiDocs/wiki/API-Activity-Get)
* [GET activity/:id - Get information about an existing ticket](https://github.com/UppCRM/UppApiDocs/wiki/API-Activity-Details)
