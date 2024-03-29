# Postman Collection for TradeTapp API 

[![Postman](https://img.shields.io/badge/Postman-v7-orange.svg)](https://www.getpostman.com/)

[![Model Properties API](https://img.shields.io/badge/Model%20Properties%20API-v2-yellowgreen)](https://forge.autodesk.com/en/docs/acc/v1/overview/field-guide/model-properties)

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

   <p align="center"><img src="https://gist.github.com/assets/969404/40aef673-e4d6-4df7-9ead-e23e60e72007" width="800" ></p>  

5. In context menu of collection >> **Edit**, switch to the tab **Authorization**. Click **Get New Access Token**, input the variables as below:

   - Grant Type `Authorization Code`
   - Callback URL  `https://www.getpostman.com/oauth2/callback`
   - Auth URL  `https://developer.api.autodesk.com/authentication/v1/authorize`
   - Access Token URL  `https://developer.api.autodesk.com/authentication/v1/gettoken`

   - Client ID `{{CLIENT_ID}}`
   - Client Secret `{{CLIENT_SECRET}}`
   - Scope `data:read`

   <p align="center"><img src="https://gist.github.com/assets/969404/58be80fd-84a8-4ef2-86a8-2df8ba585ba4" width="800" ></p> 
     
 
6. Click **Get New Access Token**, it will direct to login Autodesk account, after it succeeds, the token will be generated. Click **Use Token**.  
   
   Trade Tapp API requires to work with 3-legged token. This collection takes **[Inheriting auth](https://learning.getpostman.com/docs/postman/sending-api-requests/authorization/#inheriting-auth)** to apply 3-legged token to every endpoint in the collection automatically, which means it does not need to input the token in the header explicitly.

## API Test

1. Assume the steps of **Setup** have been performed and the access token is ready.

2. Try running some requests and explore the output: 
   <p align="center"><img src="https://gist.github.com/assets/969404/ae288d8a-aff1-4219-ac1b-858cfe941a51" width="800" ></p>   

 
 
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
