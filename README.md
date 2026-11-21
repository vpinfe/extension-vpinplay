# VPinPlay

An official extension for [VPinFE](https://github.com/vpinfe/vpinfe).  It connects VPinFE to VPinPlay, a service where pinball players share their ratings, play times and high scores.  You see what other players rate and play, and you can share yours.

## What it does

- A **Community** group in the Manager's left menu with the service's lists: **Top Rated**, **Most Played**, **Most Time Played**, **Recently Played** and **Most Installed**.  **In Your Library** shows only what you have, ranked by rating, so it is the quick way to pick a game for tonight.
- **Make a Collection** turns the list you are on into a collection that VPinFE and your theme can offer.  Its order follows the service, so it moves as the ratings do.
- Sharing for the players you choose.  It is off for every player until that player turns it on.

## Install it

VPinPlay does not come with VPinFE.  Open **System > Extensions**, find VPinPlay under **Available**, and choose **Install** from its menu.  It is on the [Extension List](https://github.com/vpinfe/extensions), so VPinFE trusts it and asks nothing.  It starts the next time VPinFE starts, and **Community** then appears in the left menu.

## Share your plays

Sharing is set per player, on **Players**.

1. Open your player and give it initials, which the service needs.
2. In the player's VPinPlay section, press **Choose a User ID**.  The dialog shows **Available** once it has checked the name.  If you already have a VPinPlay account, press **Use a Card** instead and pick the card you saved from your other device.
3. Turn **Share** on.  VPinFE asks first and says exactly what is sent: the ID and the player's initials, the games they play from now on with when and for how long, and their ratings and high scores.

Nothing is sent for a player who has not turned it on.  Turning **Share** off stops sending.  What was already sent stays with the service, which cannot rename or delete an account.

The line under the toolbar on **Community** says who is sharing and why nobody is, such as "Not sharing - needs initials".

[Sharing and accounts](docs/sharing.md) covers the card, taking an account to another device and removing one.

## Settings and actions

- **Enabled** switches the extension on and off.  It is on the extension's page under **System > Extensions**.
- **Server** is where scores and ratings are read from and sent.  Leave it blank to use VPinPlay's own server.
- **Send Now** sends games that are still waiting, such as after the service was out of reach.
- **Open VPinPlay** opens the service's website, and **Your Page** opens the public page for your account.
- **Make a Collection** is in the Community toolbar.

## Common problems

- No **Community** in the left menu.  The extension is not installed, or it is off.
- "Not sharing - Share is off".  Turn **Share** on for a player on **Players**.
- "Not sharing - needs initials".  Give that player initials in **Details**.
- "Not sharing - no player has a VPinPlay account".  Choose a user ID for a player, or use a card.
- The list is empty or says it is the last good read.  The service could not be reached.  The last list that worked is kept, and the refresh button beside the line reads it again.
- The card is lost.  Without it the account cannot be used on another device again, so save it with **Save Card** before removing the player or disconnecting.

## Where to ask

Open an [issue](https://github.com/vpinfe/extension-vpinplay/issues) here, or ask in the vpinfe channel of the Virtual Pinball Chat Discord.  VPinFE's Getting Help window builds a zip of your logs to attach.

## For developers

To write your own extension, see the [extension docs](https://github.com/vpinfe/vpinfe/blob/vpinfe-3.0/docs/extensions/README.md).

The tests need a VPinFE checkout, because they drive the real thing.  Clone or link this repository into the checkout's `extensions/vpinplay` folder, then from the checkout's root:

```bash
python -m tests tests/invariants extensions/vpinplay/tests
```

See [Testing your extension](https://github.com/vpinfe/vpinfe/blob/vpinfe-3.0/docs/extensions/testing.md) for the rest.  `tests/` and `.github/` are left out when VPinFE installs the extension.
