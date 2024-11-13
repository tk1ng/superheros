---
title: Flexion - Exporting iap form google play
deprecated: false
hidden: false
metadata:
  robots: index
---
# Introduction

This document provides information on how to export pricing set up in Google Play using one of two methods:

- Exporting a price CSV
- Google’s developer API

The methods covered in this document will eventually generate a JSON file which can be used to instruct Flexion on how to price your game.

We outline two methods due to the CSV export not always providing full pricing. More specifically – if price templates are used, the CSV export will not provide local pricing information. Hence we also provide information on how to use Google’s Developer API to export prices. This method does provide a full pricing export.

# CSV export

For exporting pricing out of the Google Play, follow these steps.

- Select the App
- Navigate to the In-app products page (Monetise > Products > In-app products
- At the top on the right-hand side there will be an Export button
- The export will generate a CSV which contains your full set of configured items and associated pricing

# Google Developer API export

The Google Play developer API can be used to export (and set) all pricing for your game in Google Play. The export results in a JSON file that Flexion can ingest to configure pricing in Flexion’s channels.  
This guide covers two key areas:

- Using the developer API to extract and export configured pricing
- Setting up the Google Play developer console for API access (if not done already)

Note: the Google Play developer API provides read AND write access to your developer account. This guide provides an overview on how to export pricing. Depending on the solution you use to access your developer account through the developer API you may end up having the ability to export pricing as well as to set pricing and/or add or remove in-app items. You acknowledge that Flexion cannot be held responsible for any issues relating to your pricing in Google Play which may arise from you implementing methods outlined in this guide. It is strongly recommended that the steps outlined here are tested in a safe environment – e.g. a test account – prior to implementing them against your live Google Play account or games.

## Using the developer API to extract and export configured pricing

The Developer API for in-app item prices is a simple CRUD API.

**Base Endpoint:** 

```
<https://androidpublisher.googleapis.com/androidpublisher/v3/applications/{packageName}/inappproducts>
```

**Note**: packageName is the game’s original package name.

**Allowed methods:**<https://developers.google.com/android-publisher/api-ref/rest/v3/inappproducts>

There are 4 methods to call the API:

- cURL
- HTTP
- Javascript
- Java

Regardless of the method of calling the API, you will have to make two HTTP requests, one for requesting the OAuth access token to access the API and one for requesting the item details.

## What you will need

To get item details you will need the following:  
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
   1. Open this URL in a browser, where YOUR_CLIENT_ID is the OAuth Client ID: <https://accounts.google.com/o/oauth2/v2/auth?client_id=YOUR_CLIENT_ID&response_type=code&scope=https://www.googleapis.com/auth/androidpublisher&access_type=offline&redirect_uri=urn:ietf:wg:oauth:2.0:oob>
   2. Log into your account and authorize the request
   3. Copy the authentication code Google generated
2. Request access token
   1. Send a POST request to the OAuth service, you will need to send multiple parameters via the request body in URLencoded form data format (e.g.: parameter1=value1¶meter2=value2)
   2. Copy the access token from the response

| Request Details |                                              |
| :-------------- | :------------------------------------------- |
| Method details  | POST                                         |
| IRÉ             | <https://www.googleapis.com/oauth2/v4/token> |

| Headers      |                                   |
| :----------- | :-------------------------------- |
| Content-type | application/x-www-form-urlencoded |

| Parameters    |                                 |
| :------------ | :------------------------------ |
| client_id     | YOUR_CLIENT_ID                  |
| client_secret | YOUR_CLIENT_SECRET              |
| code          | Authentication code from step 1 |
| redirect_uri  | urn:ietf:wg:oauth:2.0:oob       |
| grant_type    | authorization_code              |
|               |                                 |

<br />

<br />

### Request item details

Send a GET request to the Google Developer API to get the item details

| Request details |                                                                                                                        |
| :-------------- | :--------------------------------------------------------------------------------------------------------------------- |
| Method          | GET                                                                                                                    |
| URL             | <https://androidpublisher.googleapis.com/androidpublisher/v3/applications/PACKAGE_NAME/inappproducts?key=YOUR_API_KEY> |