---
description: Pair Automatos Go with an Automatos server you run, using a one-time code from Studio.
---

# Connect Your Own Server

If you run Automatos on your own server, the phone doesn't sign in. It **pairs** once with a one-time code from Studio, and from then on the server knows this phone as yours.

<!-- IMAGE: Connect to your own server screen with the Server address and Pairing code fields -->

## Before you start

The person who runs the server turns on pairing for phones and gives the server an address your phone can reach. Their guide is [Connect a phone](https://github.com/AutomatosAI/automatos-ai/blob/main/docs/getting-started/self-hosting.md#connect-a-phone-automatos-go), with the short steps in [Reach your install from your phone](https://github.com/AutomatosAI/automatos-ai/blob/main/QUICKSTART.md#reach-your-install-from-your-phone-optional).

{% hint style="warning" %}
Once pairing is on, every browser that opens Studio also asks for a code, the browser on the server too. The guide says how to make the first code on the server itself.
{% endhint %}

## Step 1: Get a pairing code in Studio

1. In Studio, go to **Settings → Phones & devices**.
2. Under **Pair a phone**, click **Get a pairing code**.
3. Studio shows an 8-character code, such as `ABCD-EFGH`, and "Expires in" with a countdown.

The code works once, for 10 minutes. Click **Get a new code** if it runs out. An owner or admin of the workspace gets the code. **Pair a phone** shows only when the server takes phones.

The first time, Studio may ask "Send notifications to phones through Expo's push service?" before it shows the code. Click **Yes** or **Not now**. You can change the answer later in **Settings → Phones & devices**.

## Step 2: Pair the phone

1. Open Automatos Go and tap **Connect to your own server**.
2. In **Server address**, type the address phones use to reach the server. Ask the person who runs it. It is often not the address you open Studio at: for example `https://api.example.com`, or `http://192.168.1.20:8000` on a home network.
3. In **Pairing code**, type the code from Studio. Capitals and the dash don't matter.
4. Tap **Continue**. The app shows "Checking the server…".
5. The app shows **Pair with this server?** with the server's edition and address. Check that this is your server, then tap **Pair**.

Nothing pairs until you tap **Pair**. The phone then shows in Studio's list as "Automatos Go on iPhone", and the app opens your workspace.

The card also says where your data goes. Your chats, files and reports stay on your server. The app itself checks Expo (the service that delivers the app's updates and notifications) for app updates and, if the server's operator agrees, sends notifications through Expo and Apple. The note mentions crash reports too: the app doesn't send them yet. See [Privacy & AI](privacy-and-ai.md).

{% hint style="info" %}
The pairing link Studio shows under the code names a server address. If it starts with localhost or 127.0.0.1, a phone can't use it: ask the person who runs the server for the address phones use. If the app says "This address doesn't answer like an Automatos server that pairs phones", you may have typed the Studio address instead.
{% endhint %}

## Scanning the QR code

On a server with the latest Automatos, Studio shows the pairing code as a QR code too. The scanner is already in the app: in Automatos Go, tap **Scan the code in Studio** and point the camera at it. The app fills in the address and the code, and still stops at **Pair with this server?**. The app asks to use the camera the first time. If you'd rather not, tap **Type the code**.

{% hint style="warning" %}
Scan the code from inside Automatos Go. The iPhone's Camera app opens the server's web page, which can't pair the phone.
{% endhint %}

## Home network or https

The server address starts with `https://` or `http://`.

| Address | What it means |
| --- | --- |
| `https://` | What the phone and the server send each other is encrypted. Any address on the internet needs it. |
| `http://` | Not encrypted. The app allows it only for an address on your home network: one that starts with 192.168, 10, or 172.16 to 172.31, or a name ending in `.local`. |

On an `http://` address, the confirm card says **Unencrypted home network**: anyone on the same network could read what the phone and the server send. Pair only on a network you trust. While you use the server, a line at the top of every screen says "Unencrypted home network" and the server's address, for example 192.168.1.20:8000.

* **localhost or 127.0.0.1** doesn't work: on a phone, that address is the phone itself. Use the server's address on your network.
* **Tailscale**: use the server's https name that ends in `.ts.net`, not its 100.x number.

## Remove a phone

**From the phone:** open **Settings** and tap **Remove this phone and forget this server**. The app asks first. The server removes the phone, and the phone forgets the server. If the server can't be reached, the phone still forgets it, and Studio may still list the phone: remove it there too.

**From Studio:** go to **Settings → Phones & devices**, find the phone and click **Revoke**. The phone's next request is refused. The phone then says "This phone was removed from" the server, and goes back to Connect. To come back, it pairs again with a new code.

You see your own phones in **Phones & devices**. A workspace owner or admin sees everyone's.

## Switch to another server

The app uses one server at a time. To use another one, remove this phone and forget this server (above). The app goes back to Welcome: tap **Connect to your own server** and pair with the new one.

If you open a pairing link while the phone uses a server, the app asks **Connect to another server?**, with **Connect instead** and **Stay connected**. Nothing changes until you check the new server and pair with it.

## Related

* [Getting Started](getting-started.md): the app's screens
* [Troubleshooting](troubleshooting.md#connecting-to-your-own-server): pairing messages and what to do
* [Privacy & AI](privacy-and-ai.md): what the phone keeps
