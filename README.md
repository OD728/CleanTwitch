# Twitch.tv Clutter Removal CSS

A simple CSS stylesheet that removes distracting UI elements from Twitch.tv for a cleaner, more focused viewing experience.

## 🎯 What It Does

This CSS hides various clutter elements on Twitch.tv without breaking core functionality:

- **Stories & Navigation**: Removes Stories sections and navigation clutter
- **Monetization**: Hides Bits and Cheer buttons 
- **Social Elements**: Removes follow buttons and subscriber goals
- **Directory Clutter**: Hides category buttons (Games, IRL, Music, Creative)
- **Chat Cleanup**: Removes chat header banner and collapse button
- **Stream Discovery**: Hides "Upcoming Streams" panels and "show more" separators
- **Visual Polish**: Makes info boxes transparent for cleaner look

## 🚀 Installation

### Method 1: Browser Extension (Recommended)

1. Install a userCSS extension:
   - **Chrome/Edge**: [Stylus](https://chrome.google.com/webstore/detail/stylus/clngdbkpkpeebahjckkjfobafhncgmne)
   - **Firefox**: [Stylus](https://addons.mozilla.org/en-US/firefox/addon/styl-us/)
   - **Safari**: [Cascadea](https://apps.apple.com/us/app/cascadea/id1432182561)

2. Copy the CSS code from below
3. Create a new style in Stylus
4. Set the domain to `twitch.tv`
5. Paste the CSS code and save

### Method 2: Browser Developer Tools (Temporary)

1. Open Twitch.tv
2. Press `F12` to open Developer Tools
3. Go to **Console** tab
4. Paste this code and press Enter:

```javascript
const style = document.createElement('style');
style.textContent = `/* CSS CODE HERE */`;
document.head.appendChild(style);
```

*Note: This method only lasts until you refresh the page*

## 📋 CSS Code

<details>
<summary>Click to expand the complete CSS code</summary>

```css
/* ==========================================
   TWITCH.TV CLUTTER REMOVAL CSS
   ==========================================
   
   This CSS removes distracting UI elements from Twitch.tv
   for a cleaner, more focused viewing experience.
   
   Features:
   - Hides Stories sections and navigation
   - Removes monetization buttons (Bits, Cheer)
   - Cleans up directory and profile elements
   - Minimizes chat distractions
   - Hides upcoming streams panels and show more separators and show more separators
   - Makes info boxes transparent
   
   ========================================== */

/* ==========================================
   STORIES & NAVIGATION
   ========================================== */

/* Hide stories following/sidebar page */
.lcFJxY {
    display: none !important;
}

/* Hide stories left navigation section */
.storiesLeftNavSection--csO9S {
    display: none !important;
}

/* Hide additional story elements */
.hdoiLi {
    display: none !important;
}

/* Hide "FOLLOWING" text header on following page */
.kcPfws {
    display: none;
}

/* ==========================================
   SEARCH & INPUT ELEMENTS
   ========================================== */

/* Hide search icon button */
.tw-combo-input__button-icon--large {
    display: none !important;
}

/* ==========================================
   PROFILE & USER ELEMENTS
   ========================================== */

/* Hide story border around profile pictures */
.halo--FRPlG {
    background: transparent !important;
}

/* Hide follow/unfollow buttons */
.grllUE {
    display: none !important;
}

/* ==========================================
   STREAM & CONTENT ELEMENTS
   ========================================== */

/* Hide subscription and follower goals below stream */
.ldUFHV {
    display: none !important;
}

/* Hide banner for sub & TC events */
.fSpCrC {
    display: none !important;
}

/* Make stream info box background transparent */
.jlCrCH {
    background-color: transparent !important;
}

/* ==========================================
   DIRECTORY & DISCOVERY
   ========================================== */

/* Hide Games, IRL, Music, Creative category buttons in directory */
.vertical-selector-card__container--lg {
    display: none;
}

/* The following rules are intended to hide the "Upcoming Streams" panel 
  and the "show more" line separator specifically on the page:
  https://www.twitch.tv/directory/following
  Note: Standard CSS cannot restrict rules to a specific URL. 
  This comment serves as a guide for manual application or for use with browser extensions 
  that allow per-URL custom CSS.
*/
header[aria-label="Upcoming Streams"],
div.Layout-sc-1xcs6mc-0.iqUbUe, /* Targets title containers for "Upcoming Streams" */
div.Layout-sc-1xcs6mc-0.iHafKo,  /* Targets the content grid for "Upcoming Streams" */
.Layout-sc-1xcs6mc-0.show-more__hidden /* Targets the "show more" line separator */
{
    display: none !important;
}

/* ==========================================
   MONETIZATION ELEMENTS
   ========================================== */

/* Hide Bits button */
.kBEymU.Layout-sc-1xcs6mc-0 > .GOdqv.ScCoreButton-sc-ocjdkq-0 {
    display: none !important;
}

/* Hide Cheer button */
.gkrCJN.Layout-sc-1xcs6mc-0 > .eSFFfM.ScButtonIcon-sc-9yap0r-0.kIbAir.ScCoreButton-sc-ocjdkq-0 {
    display: none !important;
}

/* ==========================================
   CHAT ELEMENTS
   ========================================== */

/* Hide chat top banner/header */
.stream-chat-header.fiHaCw.Layout-sc-1xcs6mc-0 {
    display: none !important;
}

/* Hide chat collapse button */
.toggle-visibility__right-column--expanded {
    display: none !important;
}
```

</details>

## ✨ What Gets Hidden

### ✅ Removed Elements
- **Stories sections** in navigation and sidebar
- **"Following" text** on following page
- **Search icon** button
- **Story borders** around profile pictures
- **Follow/Unfollow buttons**
- **Subscriber and follower goals**
- **Event banners** (sub & TC notifications)
- **Category buttons** in directory (Games, IRL, Music, Creative)
- **Upcoming Streams panels** (titles and content grids) - *primarily on /directory/following page*
- **"Show more" line separators** on directory pages
- **Bits and Cheer buttons**
- **Chat header banner**
- **Chat collapse button**

### ✅ What Stays Functional
- **Chat messages** and chat input
- **Video player** and controls
- **Stream information** and titles
- **Navigation** to channels and categories
- **Search functionality** (just the icon is hidden)
- **All core Twitch features**

## 🛠️ Customization

Want to keep some elements? Simply comment out or remove the corresponding CSS rules:

```css
/* To keep follow buttons, comment out this rule: */
/*
.grllUE {
    display: none !important;
}
*/

/* To keep subscriber goals, comment out this rule: */
/*
.ldUFHV {
    display: none !important;
}
*/

/* To keep upcoming streams panels and show more separators, comment out this rule: */
/*
header[aria-label="Upcoming Streams"],
div.Layout-sc-1xcs6mc-0.iqUbUe,
div.Layout-sc-1xcs6mc-0.iHafKo,
.Layout-sc-1xcs6mc-0.show-more__hidden
{
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

## 🐛 Troubleshooting

### Elements Not Hidden
1. **Clear browser cache** and refresh Twitch
2. **Check CSS is applied** in browser dev tools (F12)
3. **Verify domain** is set to `twitch.tv` in your CSS extension
4. **Try force refresh** with Ctrl+F5 (Windows) or Cmd+Shift+R (Mac)

### Twitch Updates Breaking CSS
Twitch occasionally updates their CSS class names. If elements reappear:

1. **Check for script updates** in this repository
2. **Report the issue** with screenshots of what's no longer hidden
3. **Temporary fix**: Use browser dev tools to find new class names

### Performance Issues
This CSS is lightweight and shouldn't affect performance. If you experience issues:

1. **Disable other extensions** temporarily to test
2. **Check browser console** for errors (F12 → Console)
3. **Try disabling specific CSS sections** to isolate the problem

## 📱 Mobile Support

The CSS works on mobile browsers but with limitations:
- Some mobile-specific elements may not be targeted
- Touch interfaces may behave differently
- Consider using Twitch mobile app for better mobile experience

## 🔄 Updates

Twitch regularly updates their interface, which may break some CSS rules. 

**When this happens:**
1. Check this repository for updates
2. Report broken elements in Issues
3. Provide screenshots and browser info

**Staying updated:**
- ⭐ Star this repository to get notifications
- 👀 Watch for releases
- 🔔 Enable notifications for Issues

## 🎨 Recommended Enhancements

Want to further enhance your Twitch experience? Here are some recommended additions that pair well with this CSS:

### 🌙 Theming
- **[Catppuccin for Twitch](https://github.com/catppuccin/userstyles/tree/main/styles/twitch)** - Beautiful, soothing pastel theme that works great with this clutter removal CSS

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

## 📝 License

This CSS is provided as-is for personal use. Feel free to modify and share.

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