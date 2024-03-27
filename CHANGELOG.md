# HomeCord Beta Changelog

> [!NOTE]
> *This changelog is ordered by newest to oldest.*

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

- Initial Beta Release
- Added the following Commands:
  - `/setup`, `/settings`, `/preferences`, `/block`, `/blocklist`, `/unblock`, `/feature`, `/unfeature`, `Feature Message`, `Unfeature Message`
- Added ability to manually feature Messages, Events, Threads/Posts, and Channels
- Added ability to automatically highlight Messages
  - *(Based off the amount of Emoji Reactions and/or direct Replies they receive in the past 3 days)*
- ...and other stuff 😅
