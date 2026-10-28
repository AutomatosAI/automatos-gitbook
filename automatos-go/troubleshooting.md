---
description: What a message in Automatos Go means and what to do about it.
---

# Troubleshooting

Each message below is what Automatos Go shows, word for word, with what to do next.

## Signing in

| What you see | What to do |
| --- | --- |
| "Sign-in is not configured in this build" | This version of the app was made without its sign-in settings. Install the newest build from TestFlight. |
| "Sign-in is not set up for Automatos Go on this server yet." | Nothing on your phone fixes this: it is set up on the server. Use Studio on the web for now. |
| "This account needs a verification step Automatos Go can't complete yet." | Your account asks for a second step the app doesn't have. Use Studio on the web for now. |
| "Passkeys aren't available on this phone. Use an email code or your password." | Tap **Email me a code** or **Use my password** instead. |
| "Your session has ended. Sign in again to carry on." | Sign in again. |

## Opening your workspace

| What you see | What to do |
| --- | --- |
| "Couldn't reach Automatos" or "Couldn't open your workspace" | Check your connection, then tap **Try again**. |
| "Workspace paused" | Your workspace is paused. Ask your workspace owner. |
| "Workspace not available" | You are no longer a member of this workspace. Ask its owner to add you again. |
| "This server needs a newer Automatos Go" | Install the newest build from TestFlight. |
| "Couldn't open this phone's saved server" | Unlock your phone, then tap **Try again**. |

## Connecting to your own server

| What you see | What to do |
| --- | --- |
| "This address needs https://. Only an address on your home network, like 192.168.1.20 or nas.local, can use http://." | Use the server's https address, or connect on your home network. See [Home network or https](connect-your-own-server.md#home-network-or-https). |
| "On a phone, that address is the phone itself." | You typed localhost or 127.0.0.1. Type the server's address on your network, like 192.168.1.20. |
| "This address doesn't answer like an Automatos server that pairs phones." | Check the address. Phones often use a different address from Studio: ask the person who runs the server. |
| "That code didn't work. Codes last 10 minutes and work once." | Get a new code in Studio, in **Settings → Phones & devices**. |
| "This server isn't taking phones yet." | The person who runs the server turns pairing on. See [Connect Your Own Server](connect-your-own-server.md#before-you-start). |
| "Too many pairing tries from this network." | Wait a few minutes, then try again. |
| "This is the Automatos hosted server. Use Sign in to Automatos instead." | Go back and tap **Sign in to Automatos**. |
| "Can't reach" and your server's name | The server isn't answering. It may be stopped, or the phone can't reach it from here. Use the phone on the same network as the server, or ask for its https address. If you run the server, the screen shows the command that starts it. To start over, tap **Remove this phone and forget this server**. |
| "This phone was removed from" your server | Someone revoked this phone in Studio. Pair it again with a new code. |
| "only answers paired phones" or "This phone's connection to" your server "ended" | Pair the phone again from Studio, in **Settings → Phones & devices**. |
| "Automatos Go couldn't use this phone's keychain." | Unlock your phone, then try again. |

## When Auto can't finish a reply

A reply that fails ends with a short line in Auto's box, and **Try again** where trying again can help. **When Auto can't answer** in [Chat](chat.md) lists each line. Other messages you may see:

| What you see | What to do |
| --- | --- |
| "Can't reach Automatos. Check your connection and try again." | Check your connection, then try again. |
| "Automatos couldn't finish that. Try again in a moment." | Wait a moment, then try again. |
| "The reply was interrupted. Try again." | Tap **Try again**. |
| "That changed while you were working on it. Refresh and try again." | Pull down to refresh, then try again. |
| "You don't have permission to do that in this workspace." | Your role doesn't allow it. Ask your workspace owner. |
| "Automatos sent something this version can't read. Try again, or update the app." | Install the newest build from TestFlight. |

## Photos and files

| What you see | What to do |
| --- | --- |
| "Automatos Go can't use the camera" | Tap **Open Settings** and allow **Camera** for Automatos Go. Or use **Photo library** instead. |
| "Files can be up to 50 MB." | Send a smaller file. |
| "A message can carry up to 20 files." | Send the rest in another message. |
| "Auto can't take this kind of file." | Try another format, such as PDF or JPEG. |
| "The image couldn't be prepared to send." | Choose the photo again. |

You can't send a video. The camera and the photo library take photos only.

## A link opens the wrong place

"This page isn't in Automatos Go" means the link is for Studio on the web, or for a newer version of the app. Tap **Go home**, or open the link in Studio.

## Getting the latest version

Most updates download by themselves:

1. Open Automatos Go and wait a moment. The update downloads.
2. Close the app fully: swipe up from the bottom of the screen and swipe Automatos Go away.
3. Open it again. You now have the update.

Some updates need a new build. When TestFlight shows a newer build of Automatos Go, install it.

{% hint style="warning" %}
Builds 5, 6 and 7 can't receive updates. If TestFlight shows one of these on your phone, install the newest build.
{% endhint %}

## Related

* [Getting Started](getting-started.md)
* [Connect Your Own Server](connect-your-own-server.md)
