### **Changelog**

#### **[7.5]**
- Add new custom color feature: "Full BG"
- Update `@baseBg` to match ChatGPT's new dark theme background (pure black)
- Adjust `.blendVariant` color mix values
- Remove old `<ol>` spacing fix
- Update option labels
- Remove boilerplate license
- Migrate StretchGPT files to `StretchGPT/` subdirectory

#### **[7.3]**
- Fix: update/add selectors for composer submit/speech buttons
- Rename chat bubble stretch option
- Remove all fancy spacing (to address VS Code issues)
- Remove/rename some colors
- Fix messed up whitespaces
- Update option labels
- Add new `compliment` mixin for dynamic selection background color
- Fix custom color functionality

#### **[7.2]**
- Update selector vars for message bubble & composer
- Apply border-radius to message container for extra-small screens when full message background color is enabled
- Rework stretch approach to adapt to ChatGPT's new sizing implementation and CSS variables
- Rename option labels

#### **[7.0]**
- Redo "stretch" implementation by overriding new ChatGPT CSS variables
- Add custom theme color picker option
- Add 2 options for new custom color override feature
- Rework custom color "de-harshing" using smarter color blending instead of transparency
- Add 30 new color presets and update docs
- Fix inconsistent width resizing for user message container
- Improve composer colorization and colorize tertiary text
- Full message background color: make the bubble match its background
- Hide horizontal overflow for the main thread component
- Remove devmode toggle

#### **[6.6]**
- Add a master toggle for unlocking all "bonus" options
- Restructure rules and guards, and disable all bonus features by default
- Add "hide avatars" option
- Update selectors, 'hide disclaimer' styles
- Selector fix: composer

#### **[6.5]**
- Fixed everything that broke after recent ChatGPT updates and added new "full-width chat bubble" feature
- Move core functionality disable option back into "Stretch factor" dropdown
- Fix footer disclaimer selectors
- Remove "hide avatars" feature and associated styles (scrapped)

#### **[6.4]**
- Update option labels' text, formatting & menu order
- Fix: hide footer disclaimer on new chat/"composer" view
- Fix: input colorization @ xs BP
- Restore missing metadata lines
- Move changelog to own file

#### **[6.3]**
- Fix: selector var (input colorize broke)

#### **[6.2.5]**
- Fix: broken selector (chat disclaimer)

#### **[6.2.4]**
- Switch default color preset from "Aged Sage" to "Super Blue Lavender"
- Improve options menu formatting

#### **[6.2.2]**
- Tweak max-width scaling for the different stretch modes. Set to 100% fixed width <768px.
- Update/rearrange settings menu items

#### **[6.2.1]**
- Fix: broken selector (chat disclaimer)

#### **[6.2]**
- Fix: broken selector (message items)

#### **[6.1]**
- Added 4 "Stretchiness" options to the userstyle config menu, to allow users to choose how wide the chat area expands based on personal preference
- The dropdown also includes a "Disable" option for those who are only interested in using the extra features.
- Tweaked the default max chat widths (now called "Comfy") so that it maxes out at 80% for the largest breakpoints.

#### **[6.0]**
- Fixed all the broken things for both desktop and mobile VPs
- Added some more cool custom color presets
- Added some new color customization options (you can now apply the color to just your message bubble or the bubble + full chat item/row.

#### **[5.1]**
- Bugfix (ChatGPT update) - custom color no longer applying to the prompt input field
- Colorize feature now fully working and enabled for "Light" ChatGPT theme
- Added an accessible text mixin to ensure that the text is always readable against any custom background color
- Split custom color options into two separate ones (user message BG and input/textarea BG)
- Cleaned up/replaced some outdated selectors to accommodate recent changes

#### **[5.0.2]**
- Loosened up the horizontal message padding a bit
- Adjusted the BG color tint logic for improved contrast accessibility with more colors
- Removed "Mobile Layouts" + some other broken code/features

#### **[5.0.1] Post UI-update hotfixes**
- A couple new fixes to restore the basic functionality after another big structural update by OpenAI a few days ago.
- Made a few tweaks to Accent Colors - added a few extra color presets and made a small fix to accommodate some elements in the new Custom GPT builder UI.
- Temporarily removed "Sidebar Tweaks" because it's been almost 100% unfunctional since the previous major UI overhaul. I'm currently working on a total overwork of this feature and it should be back in the next update.

#### **[5.0.0] New "accent colors" feature + several fixes to accommodate the most recent major ChatGPT UI overhaul**
> *OpenAI's new UI revamp released today broke pretty much everything.. Everything should be good now though.*

I've also decided to release a new adaptive "accent colors" feature that I've been sitting on for a while. I'm flagging it as an experimental feature for now (turned off by default, of course) since I'm a huge stickler for accessibility and this isn't 100% color contrast accessible yet, given the large # of possible color options/combos, but I still think it's worth releasing to everyone in its current state, despite its imperfections.

I've had this feature permanently turned on for several months now and it's become a super essential part of my ChatGPT experience, livening everything up and making the default color palette feel so bland in comparison. It'll be getting lots of polishing and improving over the next few updates, so keep an eye out!

#### **[4.0] 4 New Optional Features: Hide Avatars, Colored Message Indicators, Mobile Layout, Stacked/Centered Layout**
> **A bunch of nifty new UI enhancements are now available in the userstyle config!**
> *The subtlest new enhancements are set to active by default, but they can be easily toggled on/off at any time.*

  **Hide avatars**
- Remove the avatars from the top left corner of every message, making the conversation window a lot more symmetrical and aesthetically pleasing, as well as freeing up a significant amount of useful of horizontal space for text on smaller viewports.

**Customizable color indicators on user messages**
- Add a colored left border to all messages sent by you.
- Makes it super easy to distinguish your's vs. ChatGPT's messages, especially when "Hide avatars" is active.
- Choose from 27 different color presets in the dropdown list.
  - A subtle 2-tone gradient is dynamically generated from the selected color, based on its lightness and saturation values.
  - An upcoming update will include more color presets + the ability to define your own custom color values.

**"Mobile layout" on all screens**
 - Stacks the action buttons below the text in ChatGPT responses.

**Stacked message layout** (mobile-only - <500px viewport)
 - Centers all avatars and displays them in a separate row above the text in each message (ignored when avatars are visible)"

#### **[3.0] Sidebar/Chat History UI enhancements**
> **Introducing an optional set of sidebar/chat history menu UI tweaks - toggleable options for these are now available in the userstyle config menu.**

- Minor size reduction of fonts, icons and action buttons.
- Slightly reduce the height of the selectable list items.
- Improve chat title readability by:
  - Eliminating title truncation/ellipses.
  - Enabling text wrapping to make all the generated chat titles fully visible (no longer cut off after just a few words).
  - A couple subtle tweaks to some font weights and background/border colors in order to improve visual distinction between the different chat history "time period" sections ("Today", "Yesterday", "Previous 7 Days", etc.).

#### **[1.0] Core functionality**
- @ 768px viewport width, the fixed max-width for conversation contents is disabled.
- @ 1536px viewport width (Tailwind CSS's default "2xl" breakpoint), some modest, responsive horizontal padding is introduced, ensuring optimal and consistent readability on all larger screens.
