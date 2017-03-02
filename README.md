
##UPP REST API Documentation

UPP REST APIs provide programmatic access to read, update and delete various UPP objects.  

The REST API is based on open standards and are protected with HTTP Basic authentication.All responses are in JSON format.  

It allows developers to seamlessly integrate UPP accounts, deals, followups, products, orders, tickets and custom objects into their application.

###Authentication

Upp REST APIs requires a valid API key to authenticate your request. Only an account administrator can access or generate API Key.   

In your HTTP request header, use **api_key** parameter to specify the API key.  

####Following guide explains how to generate an API key

* In console, click on user icon, Settings -> API Access. "Team API Access" popup will be displayed.  
![apikey_setting](https://github.com/UppCRM/UppApiDocs/wiki/images/apikey_setting.png)
* Click on "Generate NEw Key", button. API KEY will be generated.
* Select the "user".
* Make sure you fill all the mandatory details and click save button.  
![apikey_dialog](https://github.com/UppCRM/UppApiDocs/wiki/images/apikey_dialog.png)
* API KEY will be generated successfully. 

###Example to get list of accounts
**Url** - http://v2.app.io/rest/v1/accounts/
**Method** - GET

###Response
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

###Accounts API
* [GET accounts - List existing accounts](https://github.com/UppCRM/UppApiDocs/wiki/API-Account-Get)
* [GET accounts/:id - Get information about an existing account](https://github.com/UppCRM/UppApiDocs/wiki/API-Account-Details)
* [POST accounts - Create a new account](https://github.com/UppCRM/UppApiDocs/wiki/API-Account-Create)
* [PUT accounts/:id - Update an existing account](https://github.com/UppCRM/UppApiDocs/wiki/API-Account-Update)
* [DELETE accounts/:id - Remove an existing account](https://github.com/UppCRM/UppApiDocs/wiki/API-Account-Delete)

