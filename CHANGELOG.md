# HomeCord Beta Changelog

> [!NOTE]
> *This changelog is ordered by newest to oldest.*

---

## Development Update - HomeCord now in Maintenance Mode
> *10th June 2024*

On 6th June 2024, Discord announced some new [Developer Policies](https://support-dev.discord.com/hc/en-us/articles/8563934450327-Discord-Developer-Policy), which includes new requirements for ~~Bots~~ Apps looking to monetize and/or have paywalled features.
These new Policies were collectively met by the Discord ~~Bot~~ App Developer community with massive distain - due to the *extremely* greedy nature of the Policies and how they treat us ~~Bot~~ App Developers like dirt.

As a result, I have decided to fully scrap any and all plans I had for my HomeCord and [HeccBot](https://github.com/HeccBot/HeccBot) Discord Server Apps.

Both of them are now in "Maintenance Mode". Meaning, I will continue doing bug-fix updates for them if need be, and only add new stuff *if I feel like it*.
I no longer feel the joy I once had with developing Discord Server Apps, due to the fact Discord keeps treating App Developers like dirt with half-baked API features, constant unannounced breaking changes, sliently scrapped announcements (API v6 & v7 never did shut down like they announced years ago), and now the greed of the new Monetization Requirements in the new Developer Policy.

Both HomeCord and HeccBot will still remain online & running, since both me and my friends do still use them frequently (esp. HeccBot).

I would say I'm sorry for stopping development of my Server Apps, but if you want someone to blame: blame Discord's higher-ups, CTO, and CEO.

I'll now be moving into learning either Web-dev or Game-dev. So I'll still be around, just now focusing my passion of programming in non-Discord areas. :)

- TwilightZebby, developer of HomeCord (and HeccBot).

---

## Beta Build 11
> *Released 30th May 2024*

- Changed how featured/highlighted Messages link to their source
  - Instead of using masked links, Link Buttons are used
- Due to the above change, HomeCord can now make full use of the 2k character limit.
  - Thus, HomeCord can now include the first 1990 characters of the featured/highlighted message, instead of just 1800 characters (if it has that many characters in the original Message!)
- Attempting to manually feature Messages with content longer than 1800 characters no longer gives an error. You can now feature long Messages!

---

## Beta Build 10
> *Released 8th May 2024*

- Added full support for featuring/highlighting Messages that contains Discord's Polls feature.

---

## Beta Build 9
> *Released 1st May 2024*

- Added a new setting to `/settings` - which can be used to enable or disable HomeCord from counting the default ⭐ Star Emoji Reactions for automatically highlighting Messages
  - *This is disabled by default as to not conflict with, nor be flooded by, existing Starboard Server Apps/Bots.*

---

## Beta Build 8
> *Released 26th April 2024*

- Scheduled Events can now be automatically highlighted to your Home Channel by HomeCord! (If you've enabled that of course)

- Added `/subscribe` Command for subscribing to HomeCord's Announcement Channel feed when you're not in HomeCord's Support Server
  - *`/subscribe`, by default, can only be used by those with the "Manage Webhooks" Permission*
- Added `/invite` Command for quickly grabbing HomeCord's Invite Link
- Added `/refresh` Command for force-refreshing a Server's Home Channel
  - ***This Command intentionally has a VERY LONG COOLDOWN of 7 days!***
  - *`/refresh`, by default, can only be used by those with the "Manage Server" Permission*

- The `Very Low` Activity Threshold for Threads was lowered a tiny bit
- The `Low`, `Medium`, and `High` Activity Thresholds for Messages, Events, and Threads was lowered too

---

## Beta Build 7
> *Released 18th April 2024*

- When setting up Home Channels **and** using the "Create Channel for me" option - HomeCord now revokes the new `SEND_POLLS` ("Create Polls") Permission for atEveryone by default
- Tweaked the default Webhook Icon used in the Home Channel that gets set when setting up Home Channels (to match the new HomeCord icon, in other words: zoomed it out a little)

- Highlighted & Featured Scheduled Events no longer include a direct Event Link; due to a bug in Discord itself preventing Event Links from having their embed suppressed

- Patched issue that caused HomeCord to, when highlighting a Message due to direct Replies, include the attachments of the *replying* Message instead of the original *replied to* Message. Whoops!

---

## Beta Build 6
> *Released 13th April 2024*

- Lowered cooldown for `/setup`, from 600 seconds down to 60 seconds.
- `/setup` now checks the HomeCord's Permissions if you try to select the "Create for Me" option in the initial Setup Page.
- Updated HomeCord's Invite Link to ask for `MANAGE_CHANNELS` and `MANAGE_WEBHOOKS` Permissions by default. These are just for easing the setup process.
  - *Thanks to the peeps in [Discord Admins](https://dis.gd/dac-faq) Server for suggesting the above three!*
- The length of time HomeCord will keep automatically highlighted items on Home Channels is now dependant on the respective Activity Thresholds
  - In other words: lower thresholds will mean highlighted items stay on Home longer. Higher thresholds mean shorter durations for highlighted items.

---

## Open Beta Release
> *12th April 2024*

- HomeCord is now in a state ready for its public beta phase! 👀

---

## Beta Build 5
> *Released 11th April 2024*

- Finally figured out how to block Polls from being featured onto Home via the "`Feature Message`" Context Command

---

## Beta Build 4
> *Released 10th April 2024*

- Refactored the database values for setting the Activity Threshold & if things can be highlighted or not.
- Each thing (Message, Events, Threads, etc) now has its own Activity Threshold
  - Can still fully disable highlighting or featuring of said thing by setting their Threshold to "disabled".
- Updated both the `/setup` and `/settings` Commands to reflect the above changes to Activity Thresholds.

---

## Beta Build 3
> *Released 3rd April 2024*

- Highlighted & Featured Events now include a direct Event Link to said Event
- "`Unfeature Message`" Context Command now supports being used on the original version of the Featured/Highlighted Message *(in addition to its cross-posted version in Home Channel)*

- Patched Bot spamming errors at TwilightZebby when failing to check a Message Author's Roles against the Server's Home Block List
  - *In other words, now handles uncached members better*
- Patched error that prevented more than 1 Thread per Server from being featured/highlighted at a time

---

## Beta Build 2
> *Released 27th March 2024*

- Added `/support` Command (links to HomeCord's Support Server)
- HomeCord can now automatically highlight Threads, Forum Channel Posts, and Media Channel Posts - based off the amount of Messages sent in them within the last 3 days

- When creating a Channel during `/setup`, HomeCord now revokes the following Permissions for `@everyone`
  - `CREATE_PUBLIC_THREADS`, `CREATE_PRIVATE_THREADS`, `ADD_REACTIONS`, `USE_EMBEDDED_ACTIVITIES`
- Patched errors when attempting to cross-post Messages to Home Channel when said Message contains multiple Attachments
- Increased Very Low Activity Threshold for Message Highlighting by 1
- Attempted to patch errors/spam-crossposting caused by Messages bulk-receiving Reactions in a manner of seconds

- HomeCord now prevents highlighting/featuring of Messages that are too old, or are of invalid Message types.
  - *For example: HomeCord will ignore Messages sent by Discord's AutoMod, those System Messages such as "User has boosted the Server", etc.*
- Added a temp-patch so that HomeCord will ignore any Messages containing Discord's native [Polls feature](https://support.discord.com/hc/en-us/articles/22163184112407)

---

## Beta Build 1 (Closed Beta Release)
> *Released 11th March 2024*

- Initial Private Beta Release
- Added the following Commands:
  - `/setup`, `/settings`, `/preferences`, `/block`, `/blocklist`, `/unblock`, `/feature`, `/unfeature`, `Feature Message`, `Unfeature Message`
- Added ability to manually feature Messages, Events, Threads/Posts, and Channels
- Added ability to automatically highlight Messages
  - *(Based off the amount of Emoji Reactions and/or direct Replies they receive in the past 3 days)*
- ...and other stuff 😅
