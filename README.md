# Vanilla Javascript SDK Sample App

This is a public code sample demonstrating how to integrate the Link Money Pay by Bank Web SDK into your own vanilla javascript application

## Requirements

Please ensure that you have interfaced with someone at Link Money in order to whitelist your redirect url. Also ensure that you have a valid client ID and secret from your merchant backend plus a valid merchant ID provided by Link Money. In order to acquire a valid Link Money merchant ID, [please reach out to us](https://www.link.money/contact).

## Installation

Please ensure that the correct credentials for the merchant backend, the URL and path to the merchant backend services and the Link merchant ID correspond to the appropriate environment. The available Link Money environments are `sandbox` and `production`. This repo will be defaulted to `sandbox`. You will need to fill in the correct values to the `config` object that is in the `index.html` file.

Once this is setup you can simply open the `index.html` file in any browser or run a local server of your choosing.

Your sample app should look like this:

<img width="386" alt="sample-app" src="https://github.com/Link-Money-Public/vanilla-javascript-sdk-sample-app/assets/20342632/f4725708-b4b0-4148-b9c0-f076de76f8c4">

<hr />

and once you click the "Pay by Bank" button you should be shot over to our Link Money Client, which looks like this:


<img width="573" alt="link-money-client" src="https://github.com/Link-Money-Public/vanilla-javascript-sdk-sample-app/assets/20342632/dae01463-e889-43b4-b716-fe36ecce7251">

## Linking and Payment

The linking and payment process can be broken into four steps.

1.  Merchant backend generates an access token.
2.  Merchant backend generates a session key.
3.  User’s account is linked using the Link Money Pay by Bank SDK with a customer ID being generated.
4.  Merchant backend makes a payment request using the appropriate tokens plus the customer ID.

For further information please refer to [our documentation](https://developer.link.money/).

## Customer Information and Accounts

Once you have successfully created a customer within our system and retrieved a customer id, you can then easliy retrieve that customer's information and accounts using the SDK.

1.  Save customer ID upon returning from linking flow.
2.  Generate an access token if you haven't already.
3.  Enter both values into either the `getCustomer` or `getAccounts` functions provided by the SDK.

> Note: Both of these functions return a promise, so you will have to await their calls.

For further information please refer to [our documentation](https://developer.link.money/products/sdks#get-customer-by-id).
