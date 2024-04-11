# HomeCord Beta Changelog

> [!NOTE]
> *This changelog is ordered by newest to oldest.*

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

## Beta Build 1
> *Released 11th March 2024*

- Initial Private Beta Release
- Added the following Commands:
  - `/setup`, `/settings`, `/preferences`, `/block`, `/blocklist`, `/unblock`, `/feature`, `/unfeature`, `Feature Message`, `Unfeature Message`
- Added ability to manually feature Messages, Events, Threads/Posts, and Channels
- Added ability to automatically highlight Messages
  - *(Based off the amount of Emoji Reactions and/or direct Replies they receive in the past 3 days)*
- ...and other stuff 😅
