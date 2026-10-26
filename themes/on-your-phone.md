---
description: Play and HUD in a phone's browser, and your theme choice, your looks and each theme's phone skin as the server keeps them for Automatos Go, the phone app.
---

# On Your Phone

A theme reaches a phone in two ways:

- **In the phone's browser**, Automatos is the web app, and a theme draws itself as it does on a laptop, from the narrowest window it supports.
- **In Automatos Go, the phone app**, the app draws its own screens. The theme you choose and the looks you save on the web are kept on the server, so the app reads the same records. A theme never sends code to the app: only colours, font files and mascot images.

## In your phone's browser

Play 1.2.0 and HUD 1.1.0 draw from 360 pixels wide, so a phone's browser shows their own phone layouts. Voice works there too: hold the voice button to talk to Auto (see [Voice Chat](../chat/voice.md)). A theme that needs a wider window shows Studio's layout on a phone instead.

{% tabs %}
{% tab title="Play" %}
<figure><img src="../images/play-390-chat-ember.png" alt="Play's chat in a phone's browser: Auto's reply with a document card, the message box with the voice button and Send, and Chats and Shelf at the top." width="300"><figcaption><p>Play's phone layout, Ember look.</p></figcaption></figure>
{% endtab %}

{% tab title="HUD" %}
<figure><img src="../images/hud-390-chat-arc.png" alt="HUD's chat in a phone's browser: Auto in the console ring, the reply with a document card, and Hold to talk between Type and Stop." width="300"><figcaption><p>HUD's phone layout, Arc look.</p></figcaption></figure>
{% endtab %}
{% endtabs %}

## In Automatos Go

What follows is what the server keeps and serves for Automatos Go.

### What the server keeps for a phone

- **Your choice.** The server keeps one theme choice per member per workspace. A phone gets the same answer a browser gets: your choice, else the workspace default, else Studio. See [Which theme you see](installing-and-choosing.md#which-theme-you-see).
- **Your looks.** Looks are kept on the server per member, per workspace and per theme, for a theme installed in the workspace. A phone reads the same records as the web. See [Where your looks are kept](looks.md#where-your-looks-are-kept).
- **The phone skin.** A theme can carry a phone block. The server turns it into data for a phone: colours, the theme's font files and its mascot's clips or still images. It never gives a phone the theme's code or style sheet.

### The phone skin

| Part | What it is |
| --- | --- |
| **Colours** | Either the theme's own light colours (and dark ones, if it has them), or your active look for that theme turned into colours. With no look of your own saved, that is the theme's default look. |
| **Light or dark** | With the theme's own colours, the phone's own light or dark setting decides. With colours from your look, the tone comes from the theme and your look: the theme's fixed tone, the tone your look sets, or else light or dark by how dark your look's ground is. |
| **Fonts** | Up to three: a sans, a serif and a mono face. |
| **Mascot** | Video clips with still images, still images only, or none, one per mascot state. |

When the colours come from your look, a phone gets the look you last saved on the server, not one still being edited in a browser tab.

{% hint style="info" %}
The scan report measures the contrast of every theme with a phone block: each text colour on its own fill (eight pairs) at 4.5:1, and the primary and focus-ring colours on the ground at 3:1. A pair under its minimum is an **Error**, so that version can't be listed in the Marketplace. A private upload still installs. See the **Contrast (AA)** row of the [scan report](installing-and-choosing.md#the-checks).
{% endhint %}

### When a phone gets no skin

| Case | Why |
| --- | --- |
| The theme isn't installed in the workspace the phone uses | A paired phone belongs to exactly the workspace it was paired in. A phone signed in as you can use any workspace you belong to. |
| A private theme you haven't opted in to | A phone gets no skin for a private version until you opt in to that version in **Settings → Appearance → Themes**. See [Opting in to a private theme](installing-and-choosing.md#opting-in-to-a-private-theme). |
| The theme has no phone block | A theme without one gives a phone nothing. |
| The version was withdrawn and turned off | A turned-off version gives a phone nothing. See [Withdrawn themes](managing-themes.md#withdrawn-themes). |

To pair a phone, use **Settings → Phones & devices**.

To give your own theme a phone skin, see [Building Your Own](building-your-own.md).
