# Alfred Stripe

An Alfred workflow for searching the Stripe Dashboard. Type `stripe` and then
anything you'd normally type into Stripe's search box, hit Enter, and the results
open in your default browser.

## Install

Download `Stripe-Search.alfredworkflow` and double-click it to install into Alfred.

## Usage

```
stripe ch_3PabcXYZ         charge
stripe pi_3Oabc            PaymentIntent
stripe pm_1Nabc            payment method
stripe sub_1Mabc           subscription
stripe customer@email.com  customer lookup
```

Anything Stripe's search accepts works, since it uses the same search. It opens:

```
https://dashboard.stripe.com/search?query=YOUR_QUERY
```

You need to already be logged into Stripe with the correct account selected. The
search runs in whatever account and mode your browser session is currently in.

## Development

The editable source lives in `workflow/` (`info.plist` and `icon.png`). The
`.alfredworkflow` file is just a zip of those. To rebuild it:

```
cd workflow && zip -r ../Stripe-Search.alfredworkflow info.plist icon.png
```
