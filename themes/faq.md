---
description: Short answers to the questions people ask first about themes and looks.
---

# Themes FAQ

The questions people ask first, with short answers and a link to the full story.

## How do I get Play or HUD?

On the local edition, download the theme's .autotheme file from the Design Kit's [releases](https://github.com/AutomatosAI/automatos-design-kit/releases), install it with **Settings → Appearance → Themes → Install theme**, then opt in to it. On the hosted edition, add it from **Marketplace → Themes** when it is listed there. See [Get Play or HUD](installing-and-choosing.md#get-play-or-hud).

## I chose a theme, but I see Studio. Why?

| What you saw | Why | What to do |
| --- | --- | --- |
| "The theme could not start, so Studio is showing instead." and "You have not opted in to its private code." | The theme is a private upload, and you haven't opted in to this version. | Open **Settings → Appearance → Themes** and click **Use this theme** to opt in. |
| "The theme could not start, so Studio is showing instead." and "Its theme.json could not be read." | This Automatos can't run the theme. A theme built on Classic always ends here: this release runs only themes built on Studio. | Ask the theme's author for a version built on Studio, or choose another theme. |
| "The theme could not start, so Studio is showing instead." with another reason | It failed once. The reason says how. | Reload. |
| "This theme failed three times in ten minutes, so you are back on Studio." | The theme kept failing in this browser, so your choice was set to Studio. | Choose it again once it is fixed. |
| "This theme was withdrawn, so it is turned off for now." | Its version was withdrawn. You see the theme's base, Studio or Classic. | Wait for a new version, or choose another theme. |
| "Safe mode: themes are off in this tab." | This tab is in safe mode. | Close the tab and open a new one. |
| No notice | The theme was uninstalled (you now see the workspace default), or the workspace no longer lets members choose. | Ask an owner or admin. |
| Studio's layout in a narrow window, a phone browser included | The app draws a theme's frame and pages only in a window 1024 pixels wide or more. | Widen the window. |

See [When a theme fails](managing-themes.md#when-a-theme-fails) and [Safe mode](managing-themes.md#safe-mode).

## Why is "Install theme" greyed?

The reason is written beside it. Either the workspace lets only its owner install themes, or private uploads are off for the workspace or for the whole server. See [Who can add a theme](installing-and-choosing.md#who-can-add-a-theme).

## I uploaded Play (or HUD) and got "Only an Automatos admin can upload a theme under the "automatos" publisher."

That publisher name, used by Play and HUD, is reserved for platform admins. On the local edition, upload it as the person who runs the local edition, who is one. On the hosted edition, add it from **Marketplace → Themes** when it is listed there. A signature file would also let the upload through, but no release is signed yet. See [Get Play or HUD](installing-and-choosing.md#get-play-or-hud).

## Why does my theme say "Private · not reviewed"?

Because nobody at Automatos reviewed it. The scan is automatic, and a person reviews only themes submitted to the Marketplace. An uploaded theme keeps the label whatever its verdict, and each member opts in to it before it runs for them.

A theme added from **Marketplace → Themes** never shows **Private · not reviewed**: a person reviewed every version listed there. It shows **Signed by Automatos** in Settings when its version carries a signature an active Automatos key verifies. No version is signed yet: see [Who vouches for a theme](README.md#who-vouches-for-a-theme).

## Why is "Make default" greyed?

Only a theme that isn't private can be the workspace default, because a default runs for members who never said yes to its code. The reason is written beside the button: "A theme that was not reviewed can’t be the workspace default." Add the theme's Marketplace version instead, if it is listed. A signed upload could be the default too, but no upload can be signed yet. See [The workspace default](installing-and-choosing.md#the-workspace-default).

## I opted in last week. Why does it ask again?

An opt-in covers one version. An update to a new private version asks every member again. Other members' opt-ins are theirs: yours covers only you.

## What do the scan badges mean?

Each check in the scan report has a badge: **Passed** (the check ran and found nothing), **Warning**, **Error** or **Not measured**. The scan never pauses or stops a theme. See [The scan report](installing-and-choosing.md#the-scan-report).

## Every check passed, so why does the verdict say "Needs a reviewer"?

The verdict also counts the AI read of the theme's code, which the report leaves out. When the AI read could not read all of the code (for example, on a server with no Anthropic API key), or when it asked for a person to look, the verdict is **Needs a reviewer**, and a line under it says so. That review matters only for a Marketplace listing: a private upload installs whatever the verdict.

## A theme broke the app. How do I get back in?

Open your Automatos address followed by **/safe-mode**. No theme code runs in that tab. Then choose Studio or Classic in the **Appearance** menu to leave the theme for good. See [Safe mode](managing-themes.md#safe-mode).

## Where is "Customise look…"?

In the **Appearance** menu: the sun, moon or screen button at the top of the app, next to the notifications bell. It shows only while a theme is your style and its layout is showing, in a window 1024 pixels wide or more. Classic and Studio have no looks. See [Looks](looks.md).

## Will an update, a roll back or an uninstall lose my looks?

No. Your looks are kept on the server per theme, not per version. If a new version changes its settings, your looks are carried over to them each time they are read. See [After a theme update](looks.md#after-a-theme-update).

## Do other members see my theme or my looks?

No. Your choice and your looks are yours, in each workspace. Owners and admins can set a workspace default, which you see until you choose a theme yourself, or always if the workspace doesn't let members choose.

## Is there a "Skins" tab?

No. The Marketplace tab for themes is called **Themes**: **Marketplace → Themes**.

## What does my phone get from my theme?

Data, never code. The server keeps your choice, your looks and each theme's phone skin (its colours, fonts and mascot) for Automatos Go, the phone app. See [On Your Phone](on-your-phone.md).

## How do I make my own theme?

With the open-source Automatos Design Kit. See [Building Your Own](building-your-own.md).
