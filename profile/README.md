<p align="center">
  <img alt="quick systems banner" src="https://raw.githubusercontent.com/quick-systems/.github/main/img/banner.png">
</p>

<h1 align="center">quick systems</h1>

<p align="center">
  <strong>Payment tooling for communities.</strong>
</p>

<p align="center">
  We build the boring half of selling online, so a Discord server, a Minecraft
  network or a plain website can take money without anyone writing a checkout
  flow from scratch.
</p>

<p align="center">
  <a href="https://kotelek.dev">kotelek.dev</a> &nbsp;&bull;&nbsp;
  <a href="https://discord.gg/HJJtYx3jJT">Discord</a>
</p>

---

## The products

<table>
<tr>
<td width="50%" valign="top">

### [quickpay](https://quickpay.kotelek.dev)

The payment layer for **Discord servers and websites**.

Members buy roles and digital goods with `/buy`, or a visitor clicks an
embedded checkout button on any page. Delivery is automatic: the bot grants the
role and DMs the buyer, and your own backend gets a signed webhook.

</td>
<td width="50%" valign="top">

### [quickshop](https://quickshop.kotelek.dev)

A ready made **storefront for Minecraft servers**.

Create a shop, add items, share the link. A player buys a rank on the web and
the plugin runs the command in game a few seconds later. Themeable, and it
handles proxy networks.

</td>
</tr>
</table>

## How the money works

Every payment is created on the **seller's own Stripe account** using Connect
direct charges. Stripe takes its processing fee, we take a small application
fee, and Stripe pays the remainder straight to the seller's bank on its normal
schedule.

We never hold a balance. There is no payout queue to wait on, no float, and no
custody risk. You are the merchant of record for your own sales.

## Open source

Everything we build is open source. Both products, the plugin, the bot and the
themes all live here in full.

| Repo | What it is |
|---|---|
| [**quickshop**](https://github.com/quick-systems/quickshop) | The quickshop web app: storefronts, dashboard, and the delivery API the plugin talks to. |
| [**minecraft-plugin**](https://github.com/quick-systems/minecraft-plugin) | The in game half of quickshop. Polls the delivery API and runs the purchase commands on your server, proxy networks included. |
| [**quickshop-themes**](https://github.com/quick-systems/quickshop-themes) | Community CSS themes for storefronts. A theme is just CSS overriding a documented set of custom properties. See [SPEC.md](https://github.com/quick-systems/quickshop-themes/blob/main/SPEC.md), then open a PR. |
| [**quickpay**](https://github.com/quick-systems/quickpay) | The quickpay web app: Stripe Connect onboarding, hosted checkout, seller dashboard and outgoing webhooks. |
| [**quickpay-bot**](https://github.com/quick-systems/quickpay-bot) | The Discord half of quickpay. discord.js v14 with Components V2, handling `/buy`, role grants and buyer DMs. |

A repo may still 404 while it is being prepared for release. It gets opened as
soon as it is ready, not before.

## Contributing a theme

The lowest friction way to ship something here:

```
themes/
  your-theme-id/
    theme.json    # name, author, version, description
    style.css     # scope everything under .qs-store
    preview.png   # optional
```

Open a pull request against
[quickshop-themes](https://github.com/quick-systems/quickshop-themes). Merged
themes sync into the app and become selectable on every shop.

## Support

Questions, bugs and setup help all go to the
[Discord](https://discord.gg/HJJtYx3jJT). It is the fastest route to a human.

<p align="center">
  <sub>Built in Poland by <a href="https://kotelek.dev">xKotelek</a></sub>
</p>
