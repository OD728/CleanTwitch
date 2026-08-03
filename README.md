# CleanTwitch: Twitch Clutter Removal CSS

CleanTwitch is a CSS stylesheet designed to remove distracting UI elements from Twitch.tv for a focused viewing experience. It is optimized for use with FrankerFaceZ (FFZ).

## Features

* **Monetization and Promos**: Removes "Get Bits," "Gift Turbo," "Go Ad-Free," Hype Train, and promotional banners.
* **Navigation**: Hides Stories, "Upcoming Streams," and unnecessary sidebar headers.
* **Stream Info**: Removes subscriber goals, share buttons, and user card whisper buttons.
* **Chat**: Hides new item indicators for bits and gifts.
* **Visual Improvements**: Applies transparency to the "About" panel and unifies FFZ metadata styling.

## Installation

1. Install a CSS manager extension such as Stylus.
2. Copy the content of `twitch_clutter_removal.css`.
3. Create a new style in Stylus, paste the code, and set the domain to `twitch.tv`.

## Recommended Configuration

For proper metadata styling, the following FrankerFaceZ settings are required under Channel > Metadata:
* Enable Player Statistics.
* Enable Hide Twitch's Native Stream Uptime.

## Theming and Utilities

* **[Catppuccin for Twitch](https://github.com/catppuccin/userstyles/tree/main/styles/twitch)**: A beautiful, soothing pastel theme that complements the clutter removal.
* **[Twitch Title Shortener](https://github.com/OD728/STwitchT)**: A userscript to keep long stream titles concise.

## Recent Updates

### Version 3.13
- **New Features:** Added options to hide the Plus Program eligibility banner, TwitchCon promotional footer, and category info banners.
- **Navigation Cleanup:** Added selectors to hide the Roblox navigation link and the "Recommended Categories" sidebar section.
- **Bug Fixes:** Fixed the Channel Leaderboard selectors and updated the "Gift a Sub" button selector for compatibility with recent Twitch updates.
- **Performance:** Optimized CSS selectors and removed redundant rules for better loading speed.
- **Visuals:** Improved alignment and styling for FFZ viewer count and uptime displays.
- **Maintenance:** Updated selectors for "Go Ad-Free for Free" buttons and other late-2025 promotional banners.
