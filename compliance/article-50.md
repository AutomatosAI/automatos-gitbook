---
description: What Automatos AI provides for EU AI Act Article 50, surface by surface, and what you as the deployer still do.
---

# EU AI Act: Article 50

Article 50 of the EU AI Act (Regulation (EU) 2024/1689) puts transparency duties on two parties. The **provider** of an AI system is Automatos AI. The **deployer** is you: the customer who uses Automatos AI in your own business. (Automatos AI is also the deployer for its own sites and posts.) This page lists, surface by surface, what Automatos AI is building for Article 50 and what you still have to do.

This page is not legal advice, and it claims no conformity or certification. Counsel has not yet reviewed this reading.

{% hint style="warning" %}
**Every item on this page is in progress: it is being built now.** A notice or a mark counts only once it is live in production. Until then, add the disclosure in your own copy.

The posture page at [automatos.app/eu-ai-act](https://automatos.app/eu-ai-act) is the record of what is live. It changes only after each notice and mark has been checked in production. Where this page and the posture page differ, the posture page is the current state.
{% endhint %}

## The duties in short

The dates follow the AI Omnibus, Regulation (EU) 2026/1744, which left Article 50 in place and added one grace period, for 50(2) only. The European Commission's Article 50 Guidelines, C(2026) 5054 final (20 Jul 2026), explain how the duties are read.

| Article | Duty | Whose duty | Applies from |
| --- | --- | --- | --- |
| **50(1)** | A person is told they are dealing with an AI, unless that is obvious. An AI agent says it is an AI and on whose behalf it acts. A notice only in the Terms, a URL, documentation, a brand name or metadata is not enough. | Provider | 2 Aug 2026 |
| **50(2)** | Generated audio, images, video and text are marked in a machine-readable format and can be detected as AI-generated, by the people who see them. Marks carry no personal data. Short strings such as UI labels, captions and alt text, and source code, are out of scope. | Provider | 2 Aug 2026 for systems placed on the market after that date; 2 Dec 2026 for systems already on the market |
| **50(3)** | Emotion recognition and biometric categorisation: inform the people exposed | Deployer | 2 Aug 2026 |
| **50(4)** | Deep fakes (realistic AI images, audio or video of real people, places or things, and cloned voices) are disclosed. AI text published to inform the public on matters of public interest is disclosed, unless a person reviewed it and holds editorial responsibility. | Deployer | 2 Aug 2026 |
| **50(5)** | The notice is clear and distinguishable, given at the latest at first exposure, and accessible | Provider and deployer | 2 Aug 2026 |

The open-source exemption does not cover Article 50, so the local edition will carry the same notices and marks as Automatos Studio, the hosted app.

## Telling people they are dealing with an AI (50(1))

No workspace setting, widget setting, theme, persona or environment setting will turn an Automatos AI notice off.

| Surface | What Automatos AI provides | What you do | Status |
| --- | --- | --- | --- |
| **Chat widget** | A fixed AI badge beside the title (`AI`; `IA` in Portuguese, Spanish, French and Italian; `KI` in German) that a title override doesn't remove, and a first line before any answer: "You are chatting with an AI assistant for {site}.", where `{site}` is your Site's public display name. The proactive and cart-idle popups say "AI assistant". | You may reword the first line, as long as it keeps your language's AI term; the badge can't be changed. Don't cover or hide the badge with site CSS. If you build your own widget client instead of using the Automatos AI SDK, show the `ai_disclosure` field from the widget config yourself: the badge for the whole session and the line before the first answer. | In progress |
| **Website chats and the Shopify theme embed** | They load the published widget, so they get the widget's badge and first line. | Nothing beyond the widget row. | In progress |
| **In-app chat** (Chat, Mission Mode, the Play chat, a theme's own chat) | "Auto is an AI" (or "{agent} is an AI") by the input, drawn by the app outside the theme's area. If a theme hides it, the chat input pauses. Every agent's instructions end with a rule to answer truthfully that it is an AI. | If you build a theme, you can't remove, cover or restyle the label away. | In progress |
| **Hold to talk** (voice in Chat, the Play chat, a theme's own chat) | Before Auto's first spoken answer in a browser tab: "Hi, this is Auto, your AI assistant." (with the answering agent's name in place of Auto's). "AI voice assistant" shows beside the voice button while you talk and while Auto answers, drawn by the app where no theme can hide it. | If you build a theme, you can't remove, cover or restyle the caption. | In progress |
| **Auto Live voice** | The call opens with "Hi, this is Auto, your AI assistant." before the caller speaks. It is said once per call; a self-hosted instance can add a spoken reminder after a reconnect and at an interval. "AI voice assistant" shows on the call panel for the whole call. | Nothing. On a self-hosted instance you may change the greeting; one that doesn't say it is an AI is replaced by the default. | In progress |
| **Telegram, Slack, Discord and WhatsApp bots** | "AI assistant for {principal}." before the first reply to a person, again after a long gap, and when someone asks if they are talking to a human. | If you receive agent messages through a generic webhook and show them to people, show the `ai_disclosure` field with the text. Set your business profile's company name so the notice names you. | In progress |
| **Email and messages an agent sends** | The first line of the body: "Written and sent by an AI agent on behalf of {principal}." It is added before you approve the send, so you approve the final text. | Don't remove the line from approved sends. Messages a person writes directly are unchanged. | In progress |
| **Automatos Academy tutors** (web and app) | "AI tutor" in the tutor's header and first turn, and the tutor answers truthfully that it is an AI. | Nothing: the tutors are Automatos's own product. | In progress |

**Who `{principal}` is.** The notice names your business profile's company name. If there is none, it uses your workspace name, but only when that isn't the automatic "{name or email}'s Workspace" form and contains no "@". Otherwise the notice names no one, because a workspace name can carry a person's name or email address.

## Marking generated content and making it detectable (50(2))

| Content | What Automatos AI provides | What you do | Status |
| --- | --- | --- | --- |
| **Rendered videos, images and audio** (Socials and media renders) | An IPTC "AI-generated" mark (`DigitalSourceType`) in the file's metadata, then a signed C2PA manifest (Content Credentials). Renders made only from templates and your own uploads get no AI mark. | Don't strip the metadata before you publish. A file you edit or re-encode yourself is a new file: it no longer carries the Automatos AI marks, and the public check has no record of it. | In progress |
| **Generated PDFs, Word and Excel files** | PDF: the IPTC mark in the document metadata. Word and Excel: custom document properties that mark the file as AI-generated. A document a person fills in by hand is not marked. | Don't remove the properties. | In progress |
| **Generated images** (the image tool, images in chat answers) | PNG and JPEG get the IPTC mark. An image that already carries a C2PA manifest from its model is kept unchanged. WebP and GIF are not marked. | Don't strip the metadata. | In progress |
| **Chat answers** | Each AI answer is flagged as AI-generated in the data the app and the widget receive. | If you build your own client, keep the flag where you pass messages on. | In progress |
| **Blog posts an agent wrote** | The blog API flags agent-written posts as AI-generated until a person marks them reviewed. The blog widget shows "AI-generated" on them and marks them as AI-generated in the page's structured data. | See public-interest text below. | In progress |
| **Checking a file** | A public check page: anyone can pick a file, and their browser works out its fingerprint (a SHA-256 hash) and asks whether Automatos AI made it. The file never leaves their machine, no account is needed, and the answer says only yes or no, the kind of media and the date. Each file Automatos AI marks gets its own random id, so two files made from the same input never share a fingerprint. | Point people who ask to the check page. The local edition answers for the files it made itself. | In progress |

Automatos AI is not adding an invisible watermark at this stage. The marks above are metadata and signed manifests.

## Your duties, and the tools for them (50(3) and 50(4))

These duties are yours by law. Automatos AI provides tools and defaults; you decide, and you stay responsible.

| Duty | What Automatos AI provides | What you do | Status |
| --- | --- | --- | --- |
| **Deep fakes** | In Socials, a setting, "Realistic AI people, places, products or voice: label as AI-generated", on by default when a post carries AI media. When it's on: a visible "AI-generated" label on the video at the start and at intervals, "AI-generated." at the start of the caption, and a spoken line for audio-only posts. Each network's own AI flag is set at publish where its API has one, and the post's receipt says what was set for each channel. | Decide for each post. If you switch the label off, disclosing the deep fake is yours. Disclose deep fakes you publish anywhere else. | In progress |
| **Public-interest text** | Agent-written blog posts are labelled "AI-generated" until a workspace member marks them reviewed. Editing a post clears the review. | Mark a post reviewed only when a person has reviewed it and holds editorial responsibility for it. Disclose AI text you publish on matters of public interest outside the blog widget. | In progress |
| **Emotion recognition, biometric categorisation** | Automatos AI has no such feature. | If you build one with Automatos AI, informing the people exposed is yours. | — |

## What every deployer does

* **Keep the notices.** Don't remove, cover or hide an AI notice or badge, whether with CSS, a theme, a custom client or a template. You may reword the widget's first line, as long as it keeps your language's AI term.
* **Don't strip the marks.** Don't remove the metadata, Content Credentials or document-property marks from files Automatos AI made. If you edit or re-encode a file, the result is a new file without them, and how you disclose it is your decision.
* **Disclose what the law puts on you:** deep fakes and public-interest text you publish (50(4)), and any emotion-recognition or biometric-categorisation use (50(3)).
* **Name yourself.** Set your business profile's company name, so channel bots and agent sends say on whose behalf they act.
* **Until a notice is live** (the [posture page](https://automatos.app/eu-ai-act) lists what is), add the disclosure in your own copy.

{% hint style="info" %}
The Terms of Service are being updated to say the same: don't remove, hide or alter the AI notices and marks, and your Article 50(3) and 50(4) duties are your own. Automatos AI's tools help with them but don't take them on.
{% endhint %}
