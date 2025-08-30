# Twitch.tv Clutter Removal CSS
![Version](https://img.shields.io/badge/version-1.8blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Stylus](https://img.shields.io/badge/stylus-compatible-brightgreen.svg)

A simple CSS stylesheet that removes distracting UI elements from Twitch.tv for a cleaner, more focused viewing experience.

## 🎯 What It Does

This CSS hides various clutter elements on Twitch.tv without breaking core functionality:

-   **Navigation & Stories**: Removes Stories sections and navigation clutter.
-   **Monetization**: Hides Get Bits, Cheer, Gift a Sub, and One-Tap Combos modal buttons.
-   **Social Elements**: Removes Share buttons, and subscriber goals.
-   **Profile**: Hides "About [Username]" headers.
-   **Directory**: Hides category buttons (Games, IRL, Music, Creative).
-   **Chat**: Removes chat collapse button.
-   **Discovery**: Hides "Upcoming Streams" panels and "show more" separators.
-   **Content Recap**: Removes recap banners and promotional content.
-   **Visual Polish**: Makes info boxes transparent and removes search bar borders.
-   **Viewer Count Styling**: Clean, unified display for viewer count and stream statistics.
-   **Optional Features (disabled by default)**: Limiting displayed tags, hiding leaderboards, and the "Gift a Sub" button. (at the bottom)

## 🚀 Installation

### Browser Extension (Recommended)

1.  Install a userCSS extension like [Stylus](https://chrome.google.com/webstore/detail/stylus/clngdbkpkpeebahjckkjfobafhncgmne) (Chrome/Edge) or [Stylus](https://addons.mozilla.org/en-US/firefox/addon/styl-us/) (Firefox).
2.  **Option A**: Use the raw GitHub URL directly: [Twitch Clutter Removal CSS Raw](https://raw.githubusercontent.com/OD728/CleanTwitch/refs/heads/main/twitch_clutter_removal.css).
3.  **Option B**: Copy the CSS code from [Twitch Clutter Removal CSS](https://github.com/OD728/CleanTwitch/blob/main/twitch_clutter_removal.css) and manually paste it into your Stylus extension.
4.  Create a new style, set the domain to `twitch.tv`, and save.


## 🎨 Recommended Enhancements

Want to further enhance your Twitch experience? Here are some recommended additions that pair well with this CSS:

### 🌙 Theming
-   **[Catppuccin for Twitch](https://github.com/catppuccin/userstyles/tree/main/styles/twitch)** - Beautiful, soothing pastel theme that works great with this clutter removal CSS
-   **[Twitch Title Truncator](https://github.com/OD728/STwitchT)** - A lightweight userscript that automatically truncates long Twitch stream titles and displays the full title on hover.

### 🔧 Browser Extensions
-   **[FrankerFaceZ](https://github.com/FrankerFaceZ/FrankerFaceZ)** - Comprehensive Twitch enhancement extension with extensive customization options

#### Recommended FrankerFaceZ Add-ons
Once you have FrankerFaceZ installed, consider these useful add-ons:

-   **7TV Emotes** - Access 7TV emotes without installing separate extension
-   **BetterTTV Emotes** - Access BTTV emotes without installing separate extension
-   **Smokey's Utilities** - Additional utilities and quality-of-life improvements
-   **The FrankerFaceZ Add-On Pack - Core** - Essential add-on pack with core features
-   **Trubbel's Utilities** - More utilities for enhanced Twitch functionality

#### FrankerFaceZ (FFZ) Elements
⚠️ **Important**: Some viewer count CSS rules only work with specific FFZ settings enabled:

**Required FFZ Settings** (Channel → Metadata):
- ✅ **Enable Player Statistics** - Required for player stats display
- ✅ **Enable Hide Twitch's Native Stream Uptime** - Required for FFZ uptime display

**What gets styled with FFZ**:
- **FFZ uptime** - Clock icon removed, clean time display
- **FFZ player stats** - Gauge icon removed, shows only latency value
- **Centered metadata tray** - All stats aligned and centered

## 📋 Changelog

#### August 2025
- ✅ **Added**: Optional rule to hide promotional event banners (e.g., SUBtember banner).
- 🔧 **Removed**: Viewer count and uptime text styling

#### July 2025
- 🚀 Optimized: Code optimization – reduced file size by ~60% (from 8KB to 3KB) without losing functionality.
- ✅ **Added**: Chat Bits "new item indicator" element – removed the "new item indicator" element next to the Bits button.
- ✅ **Added**: Hide pinned chat messages (optional, commented out by default) – New rules hide pinned messages in chat, including cheer messages and other paid-for pinned content.
- ✅ **Added**: Hide Bits Leaderboard (optional, commented out by default) – A new rule hides the rotating Bits Leaderboard that displays top cheerers/sub gifters.

#### June 2025
- 🔧 **Fixed**: Collaboration viewer sorting information bubble in directory/all.
- 🔧 **Fixed**: Subscription/follower goals hiding with a more effective selector.
- 🔧 **Fixed**: "About [Username]" header section and section panel background transparency.
- 🔧 **Fixed**: Hide extra tags beyond the first 3.
- 🔧 **Fixed**: Button overlap issue between collapse and sort buttons in the sidebar.

## 🤝 Contributing

Found an element that should be hidden or CSS stopped working? Create an **Issue** or submit a **Pull Request**.

## ⚠️ Disclaimer

This CSS only modifies the visual appearance of Twitch.tv, does not collect or modify data, and does not interfere with streaming or chat. It may require updates when Twitch changes its interface. Use at your own discretion. Not affiliated with Twitch Interactive, Inc.
