<a target="_blank" href="https://chrome.google.com/webstore/detail/#">![Try it now in CWS](https://raw.github.com/GoogleChrome/chrome-app-samples/master/tryitnowbutton.png "Click here to install this sample from the Chrome Web Store")</a>

# Managed In App Payments

## Overview of Chrome In App Payments API

You can use the Chrome In-App Payments API (Chrome IAP API) to sell digital 
and virtual goods within a Chrome App. When you use the Chrome IAP API, the 
Chrome In-App Payments Service (embedded in Chrome) communicates with:
 * The Chrome Web Store to get the list of available products, including:
   * Items available for purchase
   * Items purchased by the user
 * The Google Wallet servers to handle all the required checkout details.

This means that you do not need to handle inventory, licesning, or process 
any financial transactions. The actual integration work to enable in app 
payments is similar to using the 
[Google Wallet digital goods API](https://developers.google.com/commerce/wallet/digital/docs/) 
for websites except that the Chrome IAP API requires you to embed a piece of 
JavaScript ([buy.js](https://raw.github.com/GoogleChrome/chrome-app-samples/master/in-app-payments/buy.js)) 
within your app to trigger the payment flow.

## Sample app
Here’s a sample app that calls into the Chrome IAP API and provides options 
to trigger payments via the sandbox server as well as the production server:

*INSERT LINK HERE*

The above sample app has been published on the webstore - you can install it 
on Chrome and try out the in-app-payment flows:

*INSERT LINK HERE*

When testing with the sandbox, you can use the following credit card numbers, 
which pass basic checks by the Google Wallet for digital goods system:

https://developers.google.com/commerce/wallet/digital/docs/testing


*Note*: If you want to test this app with a list of pre-populated items to 
sell, you will need to set the key in the manifest the value listed below. 

```
"key": "MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAoUq1cKlKbPLfHlA+x/eTxPA5ZSz4bd/fgKInayClJQTc6RRATDfRshCXjn8Eu7VpgsfEG3nLGD0C+8SdDxSGxj51k5elLRcRhDLODjxMshjPpziRm8wxalrGDEVOjD8GX6DG1YXQDMq6Hd9fxSj/ZEBjGvDWtoL3wBZ1M2/+aop/5Z6y9rQDOKI8PmCaIpWmIBS1+zZub9wc/RVNA2glGaSb0N71FxN/W5PhlWwJciG/iIJHhCM888kIPODJq8JgFKz1jO8/3L8YfO9/lzbKZLPnRMrN5q5KZDbG22l6BccSXnqYu4JX9RzXK0HcRzO5SI1l5XPAeZAhNY5M+rZULwIDAQAB"
```