---
description: What Automatos Go notifies you about, answering from a notification, Face ID before approving, and the settings.
---

# Notifications

Automatos Go can tell you when work is waiting on you: a question to answer, a ticket to review, or a message from Auto.

{% hint style="info" %}
**Coming soon.** Notifications need an update of the app and an update to Automatos on the server. This page describes them as they are being built, so details may change.
{% endhint %}

<!-- IMAGE: Settings → Notifications with This phone, What notifies you and Daily digest -->

## What notifies you

| Switch | What it covers |
| --- | --- |
| **Needs an answer** | Questions, approvals and Mission plans waiting for you |
| **Ready for review** | A ticket reaches Review |
| **Auto messaged you** | Auto writes to you without being asked, and your daily digest |

Each switch is for you in this workspace, on every phone you use. Every notification names who it is from and carries the AI mark, for example "Auto · AI".

## Turn notifications on

The app asks once something is waiting for you, or from the second time you open it. It never asks the moment the app opens. **Get a notification when Auto needs you** offers **Turn on** and **Not now**. **Turn on** shows the iPhone's own permission prompt.

**Not now** holds the question back for a week. After two **Not now**s, the app stops asking: turn notifications on in **Settings → Notifications** instead.

## Settings → Notifications

Open **Settings** and tap **Notifications**.

| Section | What it does |
| --- | --- |
| **This phone** | One sentence on whether this phone gets notifications, and at most one button, such as **Turn on notifications** or **Open Settings** |
| **What notifies you** | The three switches above |
| **Daily digest** | Auto's morning brief, as Auto's message in your Auto thread. On or off, and a time: 07:00, 08:00 or 09:00 in this phone's time zone. It starts on, at 08:00. With more than one phone, the digest follows the one you used last. |
| **Question text** | **Hide question text in notifications**: a question then says only that one is waiting. Only a workspace owner or admin can change it, for the whole workspace. |
| **Approvals and answers** | **Face ID before approve or answer**. See below. |

## Answer from a notification

* **A question** offers **Reply…** and **Open**. **Reply…** works on an unlocked phone: type your answer and tap **Send**. The phone then says, for example, "Answered #0419." or "That question was already answered."
* **Everything else** offers **Open**, which takes you to it in the app.

There is no Approve button on a notification. You approve in the app, where you can see what you are approving.

If what a notification points to has moved on, the app says so, for example "That question was already answered or closed."

The number on the app icon is the number of things that need you. It is updated while the app is open.

## Face ID before approve or answer

With this switch on, the app asks for Face ID, or your passcode, before it sends:

* an answer to a question
* an approval of a ticket, a Mission plan or a social post
* permission for a tool to run

It never asks when you say no: reject, deny, withdraw, dismiss, send back, request changes or report. If you cancel or Face ID doesn't match, the app says "Nothing was sent."

* The switch is on to start with. Turning it off asks for Face ID first.
* Face ID is checked on this phone only.
* A phone with no passcode and no Face ID is not asked.
* **Reply…** on a notification doesn't ask for Face ID: unlocking the phone is the check.

## On your own server

Notifications go through Expo's push service (Expo is the service that delivers the app's updates and notifications) and Apple. On a server you run, they start only once its operator agrees in Studio, in **Settings → Phones & devices**. Until then, **This phone** says that the server doesn't send notifications to phones.

## Remove this phone

Once this phone gets notifications, **Settings** on hosted Studio shows **Remove this phone**. It removes this phone from your workspace's devices. Notifications stop on it until you turn them on again, and you stay signed in. On your own server, use **Remove this phone and forget this server**. See [Connect Your Own Server](connect-your-own-server.md#remove-a-phone).

## Related

* [Command Centre](command-centre.md): where questions and reviews wait
* [Privacy & AI](privacy-and-ai.md): what a notification shows
