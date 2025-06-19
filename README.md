# Twitch.tv Clutter Removal CSS

A simple CSS stylesheet that removes distracting UI elements from Twitch.tv for a cleaner, more focused viewing experience.

## 🎯 What It Does

This CSS hides various clutter elements on Twitch.tv without breaking core functionality:

- **Stories & Navigation**: Removes Stories sections and navigation clutter
- **Monetization**: Hides Get Bits, Cheer, Gift a Sub, and One-Tap Combos modal buttons
- **Social Elements**: Removes Share buttons, and subscriber goals
- **Profile Elements**: Hides "About [Username]" headers and titles
- **Directory Clutter**: Hides category buttons (Games, IRL, Music, Creative)
- **Chat Cleanup**: Removes chat collapse button (Leaderboard as well but it's default off)
- **Stream Discovery**: Hides "Upcoming Streams" panels and "show more" separators
- **Content Recap**: Removes recap banners and promotional content
- **Visual Polish**: Makes info boxes transparent and removes search bar borders
- **Viewer Count Styling**: Clean, unified display for viewer count and stream statistics
- **Tag Management**: Optional feature to limit displayed tags (disabled by default)
- **Leaderboard Management**: Optional feature to hide leaderboard sections (disabled by default)
- **Gift a Sub Button**: Optional feature to hide the "Gift a Sub" button (disabled by default)

## 🚀 Installation

### Method 1: Browser Extension (Recommended)

1. Install a userCSS extension:
   - **Chrome/Edge**: [Stylus](https://chrome.google.com/webstore/detail/stylus/clngdbkpkpeebahjckkjfobafhncgmne)
   - **Firefox**: [Stylus](https://addons.mozilla.org/en-US/firefox/addon/styl-us/)
   - **Safari**: [Cascadea](https://apps.apple.com/us/app/cascadea/id1432182561)

2. **Option A**: Use the raw GitHub URL directly: [Twitch Clutter Removal CSS Raw](https://raw.githubusercontent.com/ODRise/CleanTwitch/refs/heads/main/twitch_clutter_removal.css)
   - Clicking this link will allow you to directly install the CSS as a **userstyle** in Stylus (or compatible extensions).
   
   OR

   **Option B**: Copy the CSS code from [Twitch Clutter Removal CSS](https://github.com/ODRise/CleanTwitch/blob/main/twitch_clutter_removal.css)
   - Manually copy the CSS, then paste it into your Stylus extension.

3. Create a new style in your extension
4. Set the domain to `twitch.tv`
5. Paste the CSS code or URL and save

> **Tip**: After installation, you can optionally enable additional features (e.g., hiding extra tags, leaderboard sections, etc.) by uncommenting the relevant sections in the CSS.


### Method 2: Browser Developer Tools (Temporary)

1. Open Twitch.tv
2. Press `F12` to open Developer Tools
3. Go to **Console** tab
4. Copy the CSS from [Twitch Clutter Removal CSS](https://github.com/ODRise/CleanTwitch/blob/main/twitch_clutter_removal.css)
5. Paste this code and press Enter:

```javascript
const style = document.createElement('style');
style.textContent = `/* PASTE CSS HERE */`;
document.head.appendChild(style);
```

*Note: This method only lasts until you refresh the page*

## 📋 CSS Code

### Quick Access
- **📁 [Download CSS File](https://github.com/ODRise/CleanTwitch/blob/main/twitch_clutter_removal.css)** - Right-click and "Save as" to download
- **🔗 [Raw CSS File](https://raw.githubusercontent.com/ODRise/CleanTwitch/refs/heads/main/twitch_clutter_removal.css)** - Direct link for browser extensions

### Installation Methods

**For Stylus/Cascadea:**
1. Copy the CSS from the file above, OR
2. Use the raw GitHub URL directly in your extension

**For Browser Dev Tools:**
1. Copy the CSS from [Twitch Clutter Removal CSS](https://github.com/ODRise/CleanTwitch/blob/main/twitch_clutter_removal.css)
2. Follow the Developer Tools method above

## ✨ What Gets Hidden

### ✅ Removed Elements

- **"Following" text header** on following page
- **"Browse" text header** on browse/directory pages
- **"Sort by" label** on browse/directory pages
- **Stories sections** in main area and sidebar
- **"Open Stories" button** in sidebar
- **Search icon** button
- **Search bar borders** for cleaner appearance
- **Story borders** around profile pictures
- **Follow/unfollow buttons** on channel pages
- **Share buttons** on channel pages
- **"About [Username]" headers** and titles on channel pages
- **Subscriber and follower goals** (channel page goals section)
- **Gift a Sub buttons** (channel header and goals)
- **Category buttons** in directory (Games, IRL, Music, Creative)
- **Upcoming Streams panels** (titles and content grids)
- **"Show more" line separators** on directory pages
- **Recap banners** and promotional content links
- **Get Bits/Turbo button**
- **Cheer button (Chat)**
- **One-Tap Combos modal button**
- **Chat collapse button**
- **Viewer count SVG icon for Stream Together and normal Stream**
- **Clock icon** in uptime display (FFZ)
- **Gauge icon** in player stats (FFZ)

### ⚠️ Removed Elements Optional

- **Leaderboard sections** (commented out by default)
- **Hide Extra tags beyond first 3** (commented out by default)
- **Gift a Sub button** (commented out by default)
- **Leaderboard hiding** (commented out by default)

### 💡 Modified Elements
- **Viewer count and uptime display** - Centered and standardized font sizes
- **About section panels** - Made transparent background
- **Native Twitch viewer count** - Unified styling with FFZ stats
- **Stream statistics** - Clean, icon-free display

### 🎨 Viewer Count Elements

The CSS includes comprehensive styling for stream metadata displays:

#### Native Twitch Elements
- **Viewer count** - Removes people icon (Normal and Stream Together) and "XXX viewers" text, shows only the number
- **Stream uptime** - Removes descriptive text, shows only the time
- **Unified font styling** - Consistent 1.3rem size, 400 weight across all stats

#### FrankerFaceZ (FFZ) Elements
⚠️ **Important**: Some viewer count CSS rules only work with specific FFZ settings enabled:

**Required FFZ Settings** (Channel → Metadata):
- ✅ **Enable Player Statistics** - Required for player stats display
- ✅ **Enable Hide Twitch's Native Stream Uptime** - Required for FFZ uptime display

**What gets styled with FFZ**:
- **FFZ uptime** - Clock icon removed, clean time display
- **FFZ player stats** - Gauge icon removed, shows only latency value
- **Centered metadata tray** - All stats aligned and centered

### ✅ What Stays Functional
- **Chat messages** and chat input
- **Video player** and controls
- **Stream information** and titles (except "About [Username]" headers)
- **Viewer count and uptime** (styled for cleaner appearance)
- **Navigation** to channels and categories
- **Search functionality** (just the icon and borders are hidden)
- **All core Twitch features**

## 🛠️ Customization

### Optional Features

The CSS includes some features that are commented out by default:

#### Tag Limiting
To hide extra tags beyond the first 3, uncomment this section in the CSS:

```css
/* Hide extra tags beyond first 3 - Uncomment block below to enable */
.InjectLayout-sc-1i43xsx-0.dwGPiE .InjectLayout-sc-1i43xsx-0.gGAvuV:nth-child(n+5),
.InjectLayout-sc-1i43xsx-0.dwGPiE .InjectLayout-sc-1i43xsx-0.hCqJdc:nth-child(n+5) {
    display: none !important;
}
```

This will:
- Show only the first 3 tags on channel pages
- Permanently hide any additional tags
- Clean up cluttered tag displays on popular streamers' channels


#### Gift a Sub Button
To hide the "Gift a Sub" button, uncomment this section in the CSS:

```css
/* Hide Gift a Sub button */
button[data-a-target="gift-button"] {
    display: none !important;
}
```

This will:
- Hide sub gifting buttons in the channel header and channel goals.

*Note: This does not affect the sub gifting buttons that may appear directly in chat. This functionality is also configurable in FFZ.*


#### Leaderboard Hiding
To hide leaderboard sections (sub gift rankings), uncomment this section in the CSS:

```css
/* Hide leaderboard section (uncomment to enable) */
.Layout-sc-1xcs6mc-0.eOHCrm:has(.channel-leaderboard-header-rotating__users) {
    display: none !important;
}

.channel-leaderboard-header-rotating__users {
    display: none !important;
}

button[aria-label="Previous leaderboard set"],
button[aria-label="Next leaderboard set"] {
    display: none !important;
}

.channel-leaderboard-header-first-entry,
.channel-leaderboard-header-runner-up-entry {
    display: none !important;
}
```

### Keeping Specific Elements

Want to keep some elements? Simply comment out or remove the corresponding CSS rules:

```css
/* To keep Gift a Sub buttons, comment out this rule: */
/*
button[data-a-target="gift-button"],
button[data-test-selector="channel-goals-gift-a-sub-button"] {
    display: none !important;
}
*/

/* To keep share buttons, comment out this rule: */
/*
button[data-a-target="share-button"] {
    display: none !important;
}
*/
```

## 🖥️ Browser Compatibility

- ✅ **Chrome/Chromium** - Full support
- ✅ **Firefox** - Full support
- ✅ **Edge** - Full support
- ✅ **Safari** - Full support
- ✅ **Mobile browsers** - Partial support (some elements may not apply)

## 🎨 Recommended Enhancements

Want to further enhance your Twitch experience? Here are some recommended additions that pair well with this CSS:

### 🌙 Theming
- **[Catppuccin for Twitch](https://github.com/catppuccin/userstyles/tree/main/styles/twitch)** - Beautiful, soothing pastel theme that works great with this clutter removal CSS
- **[Twitch Title Truncator](https://github.com/ODRise/STwitchT)** - A lightweight userscript that automatically truncates long Twitch stream titles and displays the full title on hover.

### 🔧 Browser Extensions
- **[FrankerFaceZ](https://github.com/FrankerFaceZ/FrankerFaceZ)** - Comprehensive Twitch enhancement extension with extensive customization options

#### Recommended FrankerFaceZ Add-ons
Once you have FrankerFaceZ installed, consider these useful add-ons:

- **7TV Emotes** - Access 7TV emotes without installing separate extension
- **BetterTTV Emotes** - Access BTTV emotes without installing separate extension  
- **Smokey's Utilities** - Additional utilities and quality-of-life improvements
- **The FrankerFaceZ Add-On Pack - Core** - Essential add-on pack with core features
- **Trubbel's Utilities** - More utilities for enhanced Twitch functionality

*Note: These enhancements are independent of this CSS and can be used together or separately based on your preferences.*

## 📋 Changelog

### Latest Updates (2025)
- ✅ **Added**: Hide sub gifting buttons in the channel header and channel goals.
  - New rule hides the "Gift a Sub" button in the main channel header and within the channel goals panel.
  - Note: This does not affect the sub gifting buttons that may appear directly in chat. This functionality is also configurable in FFZ.
- ✅ **Added**: Hide recap banners
  - New rule removes recap banners and promotional content links
  - Targets article elements containing recap links for cleaner content browsing
- ❌ **Removed**: Promotion (Sub Discount)
  
* ✅ **Added/Fixed**: Improved the optional rule for hiding the Turbo/Ad-Free button with a more reliable selector targeting its specific icon.
* ✅ **Added**: New optional feature to hide the collaboration/squad stream viewer sorting bubble.
* ✅ **Added**: Hide "Sort by" label on browse pages.
    * New rule removes the label for the sort dropdown, creating a cleaner look.
- ✅ **Fixed**: Chat collapse button hiding in Theater mode
  - Updated selector to use `data-a-target="right-column__toggle-collapse-btn"`
  - Now properly hides the collapse button in both regular and Theater mode layouts
  - Added backup `aria-label` selector for additional compatibility
- ✅ **Added**: "About [Username]" header hiding
  - Hides "About [Username]" section headers on channel pages
  - Includes both main container and alternative title selectors
  - Keeps about section content visible while removing headers
- ✅ **Added**: Follow/unfollow button hiding
  - Removes follow and unfollow buttons from channel pages
  - Cleans up social interaction elements for distraction-free viewing

<details>
<summary>Previous Changelog</summary>

### Previous Updates
- ✅ **Added**: Hide "Open Stories" button and container in sidebar
- ❌ **Removed**: Chat top banner/header hiding
- ❌ **Removed**: Banner for sub & TC events hiding (`.fSpCrC` rule)
- **Streamlined**: Goals hiding to use more specific selector (`.Layout-sc-1xcs6mc-0.iSXDpX`)
- **Enhanced**: About section panel transparency with specific selector (`.Layout-sc-1xcs6mc-0.cVPBKX.about-section__panel--content`)
- ✅ **Added**: Leaderboard hiding (commented out by default for optional use)
- **Improved**: Code organization and cleanup for better maintainability

### Earlier Updates
- ✅ **Added**: Hide "Following" title header with multiple selectors
- ✅ **Added**: Hide Stories sections in main area and sidebar  
- ✅ **Added**: About section panel background transparency
- ✅ **Added**: Viewer count customization (enabled by default)
  - Centers viewer count and uptime display
  - Hides viewer count SVG icon (Stream Together) and clock icon from FFZ
  - Standardizes font sizes for consistency
- **Enhanced**: Monetization button selectors for better stability
- ✅ **Added**: Search bar border removal for cleaner appearance

### Initial Features
- ✅ **Added**: Hide One-Tap Combos modal button
- ✅ **Added**: Hide share button on channel pages
- ✅ **Fixed**: Improved "Upcoming Streams" targeting to prevent hiding legitimate channel listings
- **Enhanced**: More comprehensive "Upcoming Streams" header removal with multiple selectors
- Hide Stories sections and navigation elements
- Remove monetization buttons
- Clean up directory and profile elements
- Minimize chat distractions
- Hide "show more" separators
- Make info boxes transparent
</details>


## 🤝 Contributing

Found an element that should be hidden? CSS stopped working after a Twitch update?

1. **Create an Issue** with:
   - Screenshot of the unwanted element
   - Browser and version
   - Steps to reproduce

2. **Submit a Pull Request** with:
   - New CSS rules for additional elements
   - Fixes for updated Twitch class names
   - Clear description of changes

## ⚠️ Disclaimer

This CSS modifies the visual appearance of Twitch.tv. It:
- ✅ Only hides elements (doesn't break functionality)
- ✅ Doesn't interfere with streaming or chat
- ✅ Doesn't collect or modify data
- ⚠️ May need updates when Twitch changes their interface

Use at your own discretion. Not affiliated with Twitch Interactive, Inc.
