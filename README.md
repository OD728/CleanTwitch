# CleanTwitch: Twitch Clutter Removal CSS

CleanTwitch is a CSS stylesheet designed to remove distracting UI elements from Twitch.tv for a focused viewing experience. It is optimized for use with FrankerFaceZ (FFZ).

## Features

* **Monetization and Promos**: Removes "Get Bits," "Gift Turbo," "Go Ad-Free," Hype Train, and promotional banners.
* **Navigation**: Hides Stories, "Upcoming Streams," and unnecessary sidebar headers.
* **Stream Info**: Removes subscriber goals, share buttons, and user card whisper buttons.
* **Chat**: Hides new item indicators for bits and gifts.
* **Visual Improvements**: Applies transparency to the "About" panel and unifies FFZ metadata styling.
* **Check the toggle options**

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

### Version 3.20

#### Overnight Twitch UI Updates
Twitch rolled out major DOM updates overnight, breaking existing selectors across navigation, carousels, and promotional panels. This release adapts our stylesheet to restore clean layouts.

#### Refinement & Scoping Fixes
* **Turbo / Ad-Free Promo**: Switched to strict direct-child SVG path matching (`> button svg path[...]`) to stop parent container rules from wiping out the top nav bar.
* **Channel Leaderboards**: Isolated leaderboard selectors so shared carousel control arrows (`Previous`/`Next`) no longer accidentally hide non-leaderboard panels (like Plus Program).
* **Collapse Chat Button**: Removed an overly broad selector (`right-column__toggle-collapse-btn`) that was mistakenly hiding the native collapse chat toggle.
* **About Section & Chat Goal Trackers**: Targeted the new "Plus Program" goal panel (`a[href*="/article/plus-program"]`) across both the About section and the chat sidebar carousel.
* **Browse Directory Header**: Added URL-scoped targeting to hide the main `<h1>` title strictly on `/directory`.

#### Codebase Cleanup & Deprecation
* **Leaderboards & Turbo Promos**: Shifted to permanent hiding in Core Section 2; deprecated `hide-leaderboard`, `hide-turbo`, and `hide-pinned` dropdowns.
* **Hype Train Banner**: Updated to `aria-label` matching to replace deprecated class names and renamed toggle to `hide-hypetrain`.
* **Sub Goal Banner**: Removed legacy `aria-label="Sub Goal"` selector and dropdown due to underlying DOM deprecation.

#### New Options & Banners
* **Goal Trackers Toggle**: Added a consolidated `@advanced` dropdown covering HYPE, Goal, Bits, and Plus Program panels.
* **Promo Banners**: Added rules targeting the "Gift Sub Discount" and sponsored "Bonus Subs" banners above chat.
