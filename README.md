# Postman Collection for TradeTapp API 

[![Postman](https://img.shields.io/badge/Postman-v7-orange.svg)](https://www.getpostman.com/)

[![TradeTapp API](https://img.shields.io/badge/TradeTapp%20API-v2-yellowgreen)](https://aps.autodesk.com/en/docs/buildingconnected/v2/developers_guide/field_guide/tradetapp/)

![Beginner](https://img.shields.io/badge/Level-Beginner-green.svg)
[![License](https://img.shields.io/:license-MIT-blue.svg)](http://opensource.org/licenses/MIT)

## Description

This repository provides a postman collection that facilitates learning the [Trade Tapp API](https://aps.autodesk.com/en/docs/buildingconnected/v2/tutorials/tradetapp/).

The API supports **3 legged token** only.

## What's Postman?

Postman is a popular tool that provides an easy-to-use interface to send HTTP requests. Postman is able to parse the responses that APS sends you and save response parameter values to variables. These parameters can then be reused in subsequent requests through these variables. The Postman collections in this repository use this ability to provide pre-populated HTTP requests to help you follow the tutorial workflow with minimal effort. You can also modify the requests and experiment without having to write a single line of code. 

- You can learn how to install and use Postman from [here](https://learning.getpostman.com/docs/postman/launching_postman/installation_and_updates).

- You can download the Postman installer from [here](https://www.getpostman.com/downloads/).


## Setup



1.  **APS Account**: Learn how to create a APS Account, activate the subscription and create an app by [this tutorial](http://aps.autodesk.com/tutorials/#/account/). Get APS _client id_, _client secret_ and  _callback url_. Please register APS app with the _callback url_ as 
    
    
    `https://www.getpostman.com/oauth2/callback`  
   
2. Clone this repository or download it. It's recommended to install [GitHub Desktop](https://desktop.github.com/). To clone it via command line, use the following (**Terminal** on MacOSX/Linux, **Git Shell** on Windows):

    `git clone https://github.com/autodesk-platform-services/aps-tradetapp-postman.collection`

3. Import the collection and environment files to Postman

4. In environment, input **CLIENT_ID** and **CLIENT_SECRET** variables you got from APS into corresponding `Current value` fields:

   <p align="center"><img src="https://private-user-images.githubusercontent.com/969404/318059816-40aef673-e4d6-4df7-9ead-e23e60e72007.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTE3MTk5OTAsIm5iZiI6MTcxMTcxOTY5MCwicGF0aCI6Ii85Njk0MDQvMzE4MDU5ODE2LTQwYWVmNjczLWU0ZDYtNGRmNy05ZWFkLWUyM2U2MGU3MjAwNy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwMzI5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDMyOVQxMzQxMzBaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT01MGE5MTU0N2Y1YzNiZTc0MWYxNmI4OWM5YzgyODI0MmU5M2NmYTQ2YzA0YjJiNjQzMGUwNDUzMjRjZWM2ZmExJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.cUWzXWJk0lWVv6jk6OVUJAWYZYPS0ueKPU42SVVThU4" width="800" ></p>  

5. In context menu of collection >> **Edit**, switch to the tab **Authorization**. Click **Get New Access Token**, input the variables as below:

   - Grant Type `Authorization Code`
   - Callback URL  `https://www.getpostman.com/oauth2/callback`
   - Auth URL  `https://developer.api.autodesk.com/authentication/v1/authorize`
   - Access Token URL  `https://developer.api.autodesk.com/authentication/v1/gettoken`

   - Client ID `{{CLIENT_ID}}`
   - Client Secret `{{CLIENT_SECRET}}`
   - Scope `data:read`

   <p align="center"><img src="https://private-user-images.githubusercontent.com/969404/318061275-58be80fd-84a8-4ef2-86a8-2df8ba585ba4.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTE3MjA0ODIsIm5iZiI6MTcxMTcyMDE4MiwicGF0aCI6Ii85Njk0MDQvMzE4MDYxMjc1LTU4YmU4MGZkLTg0YTgtNGVmMi04NmE4LTJkZjhiYTU4NWJhNC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwMzI5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDMyOVQxMzQ5NDJaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT02MDc1MDFjNjIzNWM1MDFjZTNhNDY3NDc4YWQ2OGU4NGU2OGIwOGUzZWQzMWI1MjNmNmFjM2VmZDUzNGFjNWI4JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.72pcN5zgeT2exjyRAl3ZBd9s0IcnHrQRQ7GWgxnVcOw" width="800" ></p> 
     
 
6. Click **Get New Access Token**, it will direct to login Autodesk account, after it succeeds, the token will be generated. Click **Use Token**.  
   
   Trade Tapp API requires to work with 3-legged token. This collection takes **[Inheriting auth](https://learning.getpostman.com/docs/postman/sending-api-requests/authorization/#inheriting-auth)** to apply 3-legged token to every endpoint in the collection automatically, which means it does not need to input the token in the header explicitly.

## API Test

1. Assume the steps of **Setup** have been performed and the access token is ready.

2. Try running some requests and explore the output: 
   <p align="center"><img src="https://private-user-images.githubusercontent.com/969404/318063610-ae288d8a-aff1-4219-ac1b-858cfe941a51.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTE3MjEyNDAsIm5iZiI6MTcxMTcyMDk0MCwicGF0aCI6Ii85Njk0MDQvMzE4MDYzNjEwLWFlMjg4ZDhhLWFmZjEtNDIxOS1hYzFiLTg1OGNmZTk0MWE1MS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwMzI5JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDMyOVQxNDAyMjBaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1hNWEzZjliYzZjOWQxMWJlZjg2ZGY1YjI0ZmQ1OTUyOWY3NTJmMGY0Mjc5YWNlODE3NDE4N2JiYmVjOGIyZTgyJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.1Y1a-2ynF6PXQqKw1NcJy3mUBAAjuFG4CHqhFxkXb1U" width="800" ></p>   

 
 
## Further Materials
- [Trade Tapp API Tutorial](https://aps.autodesk.com/en/docs/buildingconnected/v2/tutorials/tradetapp/)
- [Trade Tapp API Reference](https://aps-stg.autodesk.com/en/docs/buildingconnected/v2/reference/http/tradetapp-financials-GET/)


**Blogs**:
- [APS Blog](https://forge.autodesk.com)
- [Field of View](https://fieldofviewblog.wordpress.com/), a BIM focused blog

## Troubleshooting

Please contact us via https://aps.autodesk.com/en/support/get-help.

## License

This sample is licensed under the terms of the [MIT License](http://opensource.org/licenses/MIT).
Please see the [LICENSE](LICENSE) file for more details.
