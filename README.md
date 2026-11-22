# SMS-Man: Virtual Phone Numbers, Online SMS Reception & API Guide

**Languages:** English · [简体中文](README.zh-CN.md) · [Tiếng Việt](README.vi.md)

[SMS-Man](https://go2lk.pages.dev/ea9735) is an online service for purchasing virtual phone numbers, receiving SMS verification messages, and renting numbers for supported use cases. This repository is an **independent, community-maintained information guide**. It is not the official SMS-Man source code or documentation.

Use this guide to understand how SMS-Man works, compare one-time SMS activation with number rental, review the official API options, and find practical safety considerations before using a virtual number.

- **Official website:** [https://sms-man.com/](https://go2lk.pages.dev/ea9735)
- **Official help center:** [https://sms-man.com/help](https://sms-man.com/help?ref=ceLde1noXEm-)
- **Official API documentation:** [https://sms-man.com/api](https://sms-man.com/api?ref=ceLde1noXEm-)
- **Compatible API documentation:** [https://sms-man.com/api/compatible](https://sms-man.com/api/compatible?ref=ceLde1noXEm-)

> **Important:** SMS-Man is a third-party commercial service. Availability, supported countries and applications, prices, payment methods, product rules, and API behavior can change. Confirm current details on the official website before making a purchase or integrating the API.

## Contents

- [SMS-Man: Virtual Phone Numbers, Online SMS Reception \& API Guide](#sms-man-virtual-phone-numbers-online-sms-reception--api-guide)
  - [Contents](#contents)
  - [What is SMS-Man?](#what-is-sms-man)
  - [How SMS-Man works](#how-sms-man-works)
  - [Main features](#main-features)
  - [One-time SMS vs. number rental](#one-time-sms-vs-number-rental)
  - [Countries and supported services](#countries-and-supported-services)
  - [How to receive an SMS with SMS-Man](#how-to-receive-an-sms-with-sms-man)
  - [SMS-Man API for developers](#sms-man-api-for-developers)
    - [API v2.0](#api-v20)
    - [Compatible API](#compatible-api)
    - [API security checklist](#api-security-checklist)
  - [Pricing, availability, and refunds](#pricing-availability-and-refunds)
  - [Privacy and security considerations](#privacy-and-security-considerations)
  - [Troubleshooting](#troubleshooting)
  - [Frequently asked questions](#frequently-asked-questions)
    - [Is SMS-Man free?](#is-sms-man-free)
    - [Can I receive SMS online without a physical SIM card?](#can-i-receive-sms-online-without-a-physical-sim-card)
    - [Can one SMS-Man number receive multiple messages?](#can-one-sms-man-number-receive-multiple-messages)
    - [Does SMS-Man support every website or app?](#does-sms-man-support-every-website-or-app)
    - [Does SMS-Man provide an API?](#does-sms-man-provide-an-api)
    - [Where can I find my API key?](#where-can-i-find-my-api-key)
    - [Are SMS-Man numbers suitable for important accounts?](#are-sms-man-numbers-suitable-for-important-accounts)
    - [Where can I get support?](#where-can-i-get-support)
  - [Official resources](#official-resources)
  - [Disclaimer](#disclaimer)

## What is SMS-Man?

SMS-Man is an online virtual-number and SMS-reception platform. Depending on current inventory and service rules, a user can select a country and an application or service, purchase a number for an SMS activation, and view the received message in their SMS-Man account. The platform also documents a number-rental option for use cases that require receiving more than one message during a rental period.

A virtual number is not the same as a personal mobile subscription. It may be shared, recycled, temporary, or subject to restrictions imposed by the destination website or mobile operator. A number being listed on SMS-Man does **not** guarantee that a third-party platform will accept it.

## How SMS-Man works

The general workflow is:

1. Create an account on the official SMS-Man website.
2. Review the available countries, services, number types, and displayed prices.
3. Choose a number option that matches the intended, permitted use.
4. Follow the instructions shown in your SMS-Man account.
5. View the incoming message in the account dashboard, if delivery succeeds.
6. Cancel or manage the activation according to the current service rules.

For the exact current flow, consult the [official help center](https://sms-man.com/help?ref=ceLde1noXEm-).

## Main features

Features described in the official materials include:

- **Online SMS reception:** view incoming SMS messages through an online account.
- **Country selection:** browse available numbers by country or region, subject to inventory.
- **Service selection:** select from the applications and services currently listed by the platform.
- **One-time activations:** obtain a number for a single SMS activation where offered.
- **Number rental:** rent a number for a defined period when repeated SMS reception is required and supported.
- **Developer API:** automate supported operations such as checking balance, viewing availability or prices, requesting a number, retrieving SMS, and changing activation status.
- **Compatible API:** an additional documented API interface for integrations that use a compatible request format.

The list above is a summary, not a promise that every feature is available in every country or for every service.

## One-time SMS vs. number rental

| Item | One-time SMS activation | Number rental |
|---|---|---|
| Typical purpose | A single verification message | Repeated messages during a rental period |
| Duration | Activation-based | Defined rental period |
| Multiple messages | Do not assume this is supported | Depends on the rental product and its rules |
| Availability | Depends on country, service, and stock | Depends on country, rental term, and stock |
| Best suited to | Low-risk, one-off use where permitted | A legitimate workflow that needs continued access |

The official help center says numbers in the **Receive SMS** section are intended for one SMS, while rented numbers are the option for receiving more than one SMS. Always check the current product description before ordering: [SMS-Man Help](https://sms-man.com/help?ref=ceLde1noXEm-).

## Countries and supported services

SMS-Man provides country and service selection through its website and API. The available inventory can change, so a static list in a GitHub README would quickly become outdated.

To check current availability:

1. Open the official [SMS-Man website](https://go2lk.pages.dev/ea9735).
2. Select the relevant country or region.
3. Select the intended service, if it is listed.
4. Review the current price and availability before ordering.

Do not rely on old screenshots, third-party lists, or country lists copied into this repository as proof of current stock.

## How to receive an SMS with SMS-Man

The exact interface may change, but the documented process generally follows these steps:

1. **Register or sign in** at [sms-man.com](https://go2lk.pages.dev/ea9735).
2. **Check the product details.** Confirm the selected country, service, number type, price, and any restrictions.
3. **Select an available number** using the official interface.
4. **Use the number only for a permitted purpose.** Enter it on the destination service only if that service allows virtual numbers and the activity complies with its terms.
5. **Check the SMS-Man account** for the incoming message.
6. **Complete verification** only when the destination service accepts the number and delivers the message.
7. **Manage the activation or rental** according to the official instructions.

If a message does not arrive, use the cancellation, retry, or support process described in the official help center. Refund eligibility is governed by the provider's current policy; do not assume every unsuccessful attempt is refundable.

## SMS-Man API for developers

SMS-Man publishes API documentation for software integrations. The official documentation currently describes an API v2.0 interface and a compatible API. Read the provider's documentation before writing an integration:

- [API v2.0 documentation](https://sms-man.com/api?ref=ceLde1noXEm-)
- [Compatible API documentation](https://sms-man.com/api/compatible?ref=ceLde1noXEm-)

### API v2.0

The official API v2.0 documentation describes requests to:

`https://api.sms-man.com/control/`

The documented operations include:

| Operation | Purpose |
|---|---|
| Balance request | Retrieve the account balance |
| Get limits | Check number availability for country/service combinations |
| Request a phone number | Request a number for a selected application |
| Get SMS | Retrieve the message associated with a request |
| Change request status | Update an activation status |
| Get current prices | Retrieve current price and availability data |
| List countries | Retrieve the supported country list |
| List services | Retrieve the supported service list |

Requests use an account API token. The exact parameters, HTTP method, response format, and status values are defined in the [official API reference](https://sms-man.com/api?ref=ceLde1noXEm-).

### Compatible API

The compatible API documentation specifies this endpoint:

`https://api.sms-man.com/stubs/handler_api.php`

It documents an `api_key` parameter and actions such as balance lookup, price lookup, number requests, country and service lists, and activation status operations. Refer to the [compatible API reference](https://sms-man.com/api/compatible?ref=ceLde1noXEm-) for the exact request and response formats.

### API security checklist

- Keep API tokens in environment variables or a secrets manager.
- Never commit API keys, session cookies, passwords, or personal data to Git.
- Do not expose API credentials in browser-side JavaScript or public examples.
- Rotate a token immediately if it is accidentally published.
- Add request timeouts, error handling, and rate-limit awareness.
- Log request identifiers and non-sensitive diagnostics, not SMS contents or credentials.
- Use the API only for lawful, authorized workflows and in accordance with SMS-Man's and the destination service's terms.

This repository does not contain an API client, does not proxy SMS messages, and does not collect credentials.

## Pricing, availability, and refunds

SMS-Man prices and number availability can vary by country, service, number type, rental period, and current inventory. There is no fixed price table in this repository because static prices can become inaccurate.

Before paying, verify:

- the selected country and service;
- whether the product is a one-time activation or a rental;
- the displayed price and currency;
- the number's current availability;
- cancellation and refund conditions;
- any limitations imposed by the destination service.

For billing or refund questions, use the provider's current [help center]([https://sms-man.com/help](https://sms-man.com/help?ref=ceLde1noXEm-) and official policy pages. A historical blog post or a community README should not be treated as the binding refund policy.

## Privacy and security considerations

Virtual numbers can be useful for testing and other permitted workflows, but they introduce risks:

- **Account recovery:** you may not control the number later, so it may be unsuitable for accounts that need future SMS recovery.
- **Number reuse:** temporary or recycled numbers may later be assigned to another user.
- **Shared access:** a virtual number should not be treated as a private, permanent phone line.
- **Third-party restrictions:** services may block virtual numbers or prohibit their use.
- **Sensitive accounts:** avoid using temporary numbers for banking, financial services, healthcare, government services, or accounts containing sensitive personal information.
- **Legal and contractual compliance:** follow applicable law and the terms of both SMS-Man and the destination service.

Do not use virtual numbers to impersonate others, evade platform safeguards, create deceptive accounts, bypass access controls, or facilitate spam, fraud, harassment, or other abuse.

## Troubleshooting

| Problem | What to check |
|---|---|
| No number is available | Check another supported country or service later; inventory changes over time. |
| SMS has not arrived | Follow the wait, cancellation, and retry instructions in the official help center. |
| Destination service rejects the number | The service may not accept virtual or previously used numbers. Do not assume another number will work. |
| API authentication fails | Verify the API key, endpoint, required parameters, and the relevant API version. Never paste your key into a public issue. |
| API returns an error | Check the official API error list and confirm that the activation/request ID and status are valid. |
| Billing or refund question | Contact SMS-Man support and consult its current policy. |

## Frequently asked questions

### Is SMS-Man free?

SMS-Man is a commercial service. Check the official website for current prices, payment methods, and any available promotions.

### Can I receive SMS online without a physical SIM card?

SMS-Man is designed to provide online access to messages sent to numbers offered through its platform. Availability and successful delivery depend on the selected number and destination service.

### Can one SMS-Man number receive multiple messages?

According to the official help center, numbers in the Receive SMS section are for one SMS. The number-rental product is intended for multiple messages during the rental period. Check the current product terms.

### Does SMS-Man support every website or app?

No. The available service list changes, and third-party platforms may reject virtual numbers. A listed service or available number does not guarantee successful verification.

### Does SMS-Man provide an API?

Yes. SMS-Man publishes API v2.0 and compatible API documentation. See the [official API page](https://sms-man.com/api?ref=ceLde1noXEm-).

### Where can I find my API key?

The official help center says the API key is available in the user's profile. Keep it private and do not publish it in source code.

### Are SMS-Man numbers suitable for important accounts?

A temporary or rented number may not remain under your control indefinitely. For important accounts, use a phone number or verification method that you control and that the service officially supports.

### Where can I get support?

Use the contact and support options linked from the [official SMS-Man website](https://go2lk.pages.dev/ea9735) and [help center](https://sms-man.com/help?ref=ceLde1noXEm-).

## Official resources

| Resource | Link |
|---|---|
| Official website | [https://sms-man.com/](https://go2lk.pages.dev/ea9735) |
| Help center |[https://sms-man.com/help](https://sms-man.com/help?ref=ceLde1noXEm-) |
| API v2.0 | [https://sms-man.com/api](https://sms-man.com/api?ref=ceLde1noXEm-) | 
| Compatible API | [https://sms-man.com/api/compatible](https://sms-man.com/api/compatible?ref=ceLde1noXEm-) |
| Chinese help center | [https://sms-man.com/help](https://sms-man.com/help?ref=ceLde1noXEm-) |
| Chinese API documentation | https://sms-man.com/cn/api |

## Disclaimer

This repository is an independent informational resource. It is not affiliated with, authorized by, or endorsed by SMS-Man. “SMS-Man” and related names or marks belong to their respective owners. Product descriptions and links are provided for reference; the official provider's current terms and documentation take precedence.

This repository does not encourage violating third-party terms, evading verification safeguards, or using virtual numbers for unlawful or abusive activity. Users are responsible for ensuring that their use is lawful and permitted by the relevant services.

---

If this guide is useful, consider starring the repository and checking the official SMS-Man documentation for the latest information.
