---
title: Flexion - Exporting iap form google play
deprecated: false
hidden: false
metadata:
  robots: index
---
# Introduction

This document provides information on how to export pricing set up in Google Play using one of two methods:

* Exporting a price CSV
* Google’s developer API

The methods covered in this document will eventually generate a JSON file which can be used to instruct Flexion on how to price your game.

We outline two methods due to the CSV export not always providing full pricing. More specifically – if price templates are used, the CSV export will not provide local pricing information. Hence we also provide information on how to use Google’s Developer API to export prices. This method does provide a full pricing export.

# CSV export

For exporting pricing out of the Google Play, follow these steps.

* Select the App
* Navigate to the In-app products page (Monetise > Products > In-app products
* At the top on the right-hand side there will be an Export button
* The export will generate a CSV which contains your full set of configured items and associated pricing

# Google Developer API export

The Google Play developer API can be used to export (and set) all pricing for your game in Google Play. The export results in a JSON file that Flexion can ingest to configure pricing in Flexion’s channels.\
This guide covers two key areas:

* Using the developer API to extract and export configured pricing
* Setting up the Google Play developer console for API access (if not done already)

Note: the Google Play developer API provides read AND write access to your developer account. This guide provides an overview on how to export pricing. Depending on the solution you use to access your developer account through the developer API you may end up having the ability to export pricing as well as to set pricing and/or add or remove in-app items. You acknowledge that Flexion cannot be held responsible for any issues relating to your pricing in Google Play which may arise from you implementing methods outlined in this guide. It is strongly recommended that the steps outlined here are tested in a safe environment – e.g. a test account – prior to implementing them against your live Google Play account or games.

## Using the developer API to extract and export configured pricing

The Developer API for in-app item prices is a simple CRUD API.

**Base Endpoint:**

```
<https://androidpublisher.googleapis.com/androidpublisher/v3/applications/{packageName}/inappproducts>
```

**Note**: packageName is the game’s original package name.

**Allowed methods:**

```
<https://developers.google.com/android-publisher/api-ref/rest/v3/inappproducts>
```

There are 4 methods to call the API:

* cURL
* HTTP
* Javascript
* Java

Regardless of the method of calling the API, you will have to make two HTTP requests, one for requesting the OAuth access token to access the API and one for requesting the item details.

## What you will need

To get item details you will need the following:\
•	Package name of the game
•	API key
•	OAuth client ID
•	OAuth client secret

## Getting item details

There are two steps to get item details:

1. request OAuth access token
2. request the item details from the API

### Request OAuth access token

There are two steps to get the access token.

1. Request authentication code by logging in with your Google account
   1. Open this URL in a browser, where YOUR\_CLIENT\_ID is the OAuth Client ID: `<https://accounts.google.com/o/oauth2/v2/auth?client_id=YOUR_CLIENT_ID&response_type=code&scope=https://www.googleapis.com/auth/androidpublisher&access_type=offline&redirect_uri=urn:ietf:wg:oauth:2.0:oob>`
   2. Log into your account and authorize the request
   3. Copy the authentication code Google generated
2. Request access token
   1. Send a POST request to the OAuth service, you will need to send multiple parameters via the request body in URLencoded form data format (e.g.: parameter1=value1¶meter2=value2)
   2. Copy the access token from the response

| Request Details |                                                |
| :-------------- | :--------------------------------------------- |
| Method details  | POST                                           |
| IRÉ             | `<https://www.googleapis.com/oauth2/v4/token>` |

| Headers      |                                   |
| :----------- | :-------------------------------- |
| Content-type | application/x-www-form-urlencoded |

| Parameters     |                                 |
| :------------- | :------------------------------ |
| client\_id     | YOUR\_CLIENT\_ID                |
| client\_secret | YOUR\_CLIENT\_SECRET            |
| code           | Authentication code from step 1 |
| redirect\_uri  | urn:ietf:wg:oauth:2.0:oob       |
| grant\_type    | authorization\_code             |
|                |                                 |

<br />

<br />

### Request item details

Send a GET request to the Google Developer API to get the item details

| Request details |                                                                                                                          |
| :-------------- | :----------------------------------------------------------------------------------------------------------------------- |
| Method          | GET                                                                                                                      |
| URL             | `<https://androidpublisher.googleapis.com/androidpublisher/v3/applications/PACKAGE_NAME/inappproducts?key=YOUR_API_KEY>` |

| Headers       |                      |
| :------------ | :------------------- |
| Authorization | Bearer ACCESS\_TOKEN |
| Accept        | application/json     |

<br />

## Methods to call the API

### cURL

```curl curl
'https://androidpublisher.googleapis.com/androidpublisher/v3/applications/[PACKAGENAME]/inappproducts?key=[YOUR_API_KEY]' 
  --header 'Authorization: Bearer [YOUR_ACCESS_TOKEN]' 
  --header 'Accept: application/json' 
  --compressed`
```

\[PACKAGENAME] - game’s original package name

\[YOUR\_API\_KEY] - API key generated by the game’s developer

\[YOUR\_ACCESS\_TOKEN] - access token requested manually from the OAuth service, see `<https://www.jhanley.com/google-oauth-2-0-testing-with-curl/>`

### HTTP

```http
GET https://androidpublisher.googleapis.com/androidpublisher/v3/applications/[PACKAGENAME]/inappproducts?key=[YOUR_API_KEY] HTTP/1.1`  
`Authorization: Bearer [YOUR_ACCESS_TOKEN]
Accept: application/json`
```

\[PACKAGENAME] - game’s original package name\
\[YOUR\_API\_KEY] - API key generated by the game’s developer
\[YOUR\_ACCESS\_TOKEN] - access token requested manually from the OAuth service, see `<https://www.jhanley.com/google-oauth-2-0-testing-with-curl/>`

**Note**: using HTTP to call the API allows you to get the pricing details from Google without any software development. This can be achieved through calling the API from a browser using a plugin which can add or modify required HTTP headers.

### Javascript

```javascript
<script src="https://apis.google.com/js/api.js"></script>
<script>  
/*
_Sample JavaScript code for androidpublisher.inappproducts.list  
\_See instructions for running APIs Explorer code samples locally:  
\_<https://developers.google.com/explorer-help/guides/code_samples#javascript>  
_/\*/

  function authenticate() {
    return gapi.auth2.getAuthInstance()
        .signIn({scope: "https://www.googleapis.com/auth/androidpublisher"})
        .then(function() { console.log("Sign-in successful"); },
              function(err) { console.error("Error signing in", err); });
  }
  function loadClient() {
    gapi.client.setApiKey("YOUR_API_KEY");
    return gapi.client.load("https://androidpublisher.googleapis.com/$discovery/rest?version=v3")
        .then(function() { console.log("GAPI client loaded for API"); },
              function(err) { console.error("Error loading GAPI client for API", err); });
  }  
  // Make sure the client is loaded and sign-in is complete before calling this method.  
  function execute() {  
    `return gapi.client.androidpublisher.inappproducts.list({
      "packageName": "PACKAGE_NAME"
    })
        .then(function(response) {
                // Handle the results here (response.result has the parsed body).
                console.log("Response", response);
              },
              function(err) { console.error("Execute error", err); });
  }
  gapi.load("client:auth2", function() {
    gapi.auth2.init({client_id: "YOUR_CLIENT_ID"});
  });
</script>
```

`<button onclick="authenticate().then(loadClient)">authorize and load</button>   <button onclick="execute()">execute</button>`

YOUR\_API\_KEY - API key generated by the game’s developer\
PACKAGE\_NAME - game’s original package name
YOUR\_CLIENT\_ID - OAuth client ID generated by the game’s developer

### Java

Google has a Java library for their Developer API, which works similarly to javascript.

API: `<https://github.com/googleapis/google-api-java-client-services/tree/master/clients/google-api-services-androidpublisher/v3>`

# Setting up the Google Play developer console for API access

Follow the below steps to get the Google Play developer console configured to allow API access for pricing management. Note – the access created is read and write – hence, pay special attention to

## HOW TO GENERATE API CREDENTIALS

Follow the below steps in order to generate your API credentials

* Go to `<https://play.google.com/console>`
* Select API Access in the Setup section

### Google Cloud Project not yet linked

1. Link existing project
   1. Select Link existing project
   2. Select your Google Cloud project from the dropdown list
2. Create new project
   1. Select Create new project
   2. Click Link project

### Google Cloud Project already linked

1. View project
2. Go to APIs and Services
3. Enable API
4. Click + ENABLE APIS AND SERVICES
   1. Search for Google Play Android Developer API
   2. Select first match.
   3. Click Enable if it’s not already enabled.
5. Create API key
   1. Go to Credentials
   2. Click + CREATE CREDENTIALS
   3. Select API Key
6. Click Save
7. Create OAuth Client
   1. Click + CREATE CREDENTIALS
   2. Select OAuth client ID
8. Make the following changes
   1. Application type >>> Desktop Application
   2. Name >>> Can be whatever name you want
9. Click Create

<br />

<br />

Flexion Mobile Plc. 2024. All Rights Reserved

\| Confidential |