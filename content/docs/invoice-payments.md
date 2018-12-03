---
title: Invoice Payments
---

# Accepting Invoice Payments

RemoteOne allows you to easily create invoices to send to your clients.
You can currently either download a PDF (`.pdf`) file or send them a link to an [online invoice](/online-invoices).

Using our online invoices you can accept online payments from *within* an invoice using
<a href="https://stripe.com" target="_blank" rel="noopener noreferrer">Stripe</a>.

You can accept payment in any of our [suported currencies](/supported-currencies).
There is a small additional conversion cost when receiving payments in currencies other than USD.
Click
<a href="https://stripe.com/gb/pricing" target="_blank" rel="noopener noreferrer">here</a>
to read more about Stripe fees.

## Getting started with Stripe

Stripe is an online payment processing service.
RemoteOne uses Stripe's tools to allow simple and secure card payments for
your invoices.

### Create an account

The first thing to do is
<a href="https://dashboard.stripe.com/register" target="_blank" rel="noopener noreferrer">create a Stripe account</a>
if you don't have one already.

Next make sure you're account is verified.

1. Verify your email address by clicking the link which Stripe sent you.
2. Click the "Activate your account" on the right side of the Stripe dashboard.
3. Fill in the form providing details of your business and bank account.

*You may also have to upload proof of ID before Stripe allow payouts. However this is not needed to revive payments*.

### Getting your API keys

An API (application programming interface) is a way for two applications to communicate.
To prevent others from accessing your data through this API, Stripe
provide two unique passwords (called keys or tokens) which are needed to add charges
to your account.

There are two types of API key in Stripe; **test keys** and **live keys**.
As you'd expect, the test keys are for testing perposes only and charges
to them are fictional.

Live keys are only available on activated accounts. You can still follow the
setup now using the test keys, but please remember to enter your
live keys when your account is verified.

Head over the the API keys page in the Stripe Dashboard:

![Stripe Dashboard API Keys Link](/images/invoice-payments/api-keys-sidebar.png)

We recommend creating a dedicated restricted key for use with RemoteOne. This is
the most secure way to interact with the Stripe API as it allows access only to the
features you choose. To accept payments RemoteOne only needs access to
"Read and write" the "Charges" service. Learn more about Stripe keys
<a href="https://stripe.com/docs/keys" target="_blank" rel="noopener noreferrer">here</a>.

Create a new restricted key:

<img src="/images/invoice-payments/restricted-api-keys.png" alt="Restricted API keys" style="width: 100%" />

Name your restricted key "RemoteOne", allow read and write access to charges **only** and save the key:

<img src="/images/invoice-payments/create-restricted-api-key.png" alt="Create new restricted API key" style="width: 100%" />

RemoteOne needs your "Publishable key" along with your new restricted key.
You'll need to click the _reveal_ button to view your restricted key.

<img src="/images/invoice-payments/copy-api-keys.png" alt="Copy public and restricted keys" style="width: 100%" />

## Setting up RemoteOne

Once you've got your API keys set up you can enter them into RemoteOne.
Open up your 
<a href="https://web.remote.one/settings" target="_blank" rel="noopener noreferrer">account settings</a>
and click on the "Invoice Payments" sidebar button.

Next, copy and paste both keys into their input boxes and click "Save changes":

<img src="/images/invoice-payments/paste-keys.png" alt="Enter your API keys into RemoteOne" style="width: 100%" />

You should see a message verifying your tokens have been saved.

Thats it! Now your online invoices will display a "Pay With Card" button at the top:

<img src="/images/invoice-payments/invoice.png" alt="RemoteOne Invoice" style="width: 100%" />

## Testing

You can test the payment flow before sending it to your clients by using your test API keys and
completing a payment on a test invoice. The checkout process will show a "Test mode" banner to
confirm you're not making a real payment:

<img src="/images/invoice-payments/test-mode.png" alt="Test payment flow" style="width: 100%" />

Stripe provides the credit card number `4242424242424242` which you can
use for testing with any expiry date and CVC number.
