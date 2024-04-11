*[Return to index](https://github.com/HomeCord/homecord-docs/blob/main/README.md)*

> [!IMPORTANT]
> For clarification:
> - "Highlight"/"Highlighting" refers to HomeCord *automatically* showcasing that aspect to its Home Channels.
> - "Feature"/"Featuring" refers to a Server Mod or Admin *manually* showcasing that aspect to HomeCord's Home Channel, through use of Commands.

---

# Information on HomeCord's "Home" Channels

"Home" Channels is a single Channel in a Server, setup using this HomeCord Bot, that can highlight, feature, and/or showcase various aspects of a Server.

These aspects can include popular Messages, active Threads & Forum Posts, upcoming Scheduled Events, and important Channels (and in future version, active Voice Channels & live Stages too!).

Not all Home Channels made with HomeCord are the same. Some Servers may choose to disable automatic highlighting of various aspects - such as disabling the ability to highlight Threads & Forum Posts - in addition to changing what the set minimum "Activity Threshold" is for being able to highlight each aspect.

This page will break down each part of HomeCord's Home Channels, what is included in said part, and how each aspect is automatically highlighted (if enabled).

> [!NOTE]
> Disabling the ability to automatically highlight a specific aspect does **NOT** disable the ability to *manually* feature said aspect via Commands.

---

## Home Channel: The Header & Important Channels

Starting at the top of HomeCord's Home Channels, we have the Home Channel's Header & Important Channels.

The Header is simply just the Server's Name and, if set via `Server Settings > Community > Overview` (in Discord itself), the Server's description.
Directly below the Header, we start getting into the toggleable aspects of the Home Channel.

Server Admins (by default, those with at minimum the "`Manage Channels`" Permission) can use HomeCord's `/feature channel` Command to 'pin' Important Channels to the top of the Home Channel. You can also include an optional, custom, description for that Important Channel when using the Command.

Important Channels can be manually removed from the Home Channel via use of the `/unfeature channel` Command.

The Important Channels aspect of a Home Channel is the *only* part of the Home Channel that is fully manual. HomeCord does *not*, and will *not*, automatically 'pin' Channels as Important Channels to the top of your Home Channel.

---

## Home Channel: Scheduled Events

Moving down the Home Channel, the first highlightable aspect of the Home Channel are Scheduled Events. (ie: the ones you can make in an Event Tab at the top of a Server's Channel List in Discord)

If automatic highlighting is enabled for Events, HomeCord can showcase upcoming Scheduled Events based off the number of Server Members that have registered their interest for that Event via clicking that Event's "Interested" button in Discord.

> [!WARNING]
> Automatic highlighting of Scheduled Events has yet to be implemented to HomeCord. This notice will be removed once it has been implemented!
> 
> You can still manually feature Scheduled Events via use of HomeCord's `/feature event` Command, as described below too.

Server Admins (by default, those with at minimum the "`Manage Channels`" Permission) can also use HomeCord's `/feature event` Command to manually showcase an upcoming Scheduled Event to the Home Channel. This Command also lets Server Admins choose how long to feature that Event too - from 12 hours up to 1 week (7 days).

Scheduled Events, regardless of being highlighted or featured, can be manually removed from the Home Channel via use of the `/unfeature event` Command.

> [!NOTE]
> If the Command's list of Scheduled Events isn't updating to reflect or showing your Server's current Scheduled Events, just run the Command once while picking any option displayed. This will make HomeCord's cache update to your Server's current Scheduled Events.

---

## Home Channel: Threads, Forum Posts, and Media Posts

Next up, are Threads, Forum Channel Posts, and Media Channel Posts. For the sake of simplifying things, all three shall be referred to together as just "threads". (Since Forum Posts and Media Posts *are* Threads behind-the-scenes)

If automatic highlighting is enabled for Threads, HomeCord can highlight Public Threads (not Private ones) based off the number of *recent* Messages sent in that Thread. This can massively increase discoverability of Threads, even more so for Threads in standard Text Channels.

Much like Events, Server Admins can also manually feature Threads via use of HomeCord's `/feature thread` Command - also including how long to feature that Thread for, from 12 hours up to 1 week. By default, only those with at minimum the "`Manage Channels`" Permission can use that Command.

Threads, regardless of being highlighted or featured, can be manually removed from the Home Channel via use of the `/unfeature thread` Command.

---

## Home Channel: Messages

Now for what could be considered the most dynamic part of HomeCord's Home Channels - Messages themselves!

If automatic highlighting is enabled for Messages, HomeCord can highlight *recently sent* Messages based off the number of Emoji Reactions added to it (doesn't matter if Super or regular Reaction), **and/or** the number of [direct Replies](https://support.discord.com/hc/en-us/articles/360057382374) to said Message.

Server Moderators and Admins (by default, those with at minimum the "`Manage Messages`" Permission) can use the "`Feature Message`" *Context* Command to manually feature Messages to the Home Channel, for between 12 hours - 1 week.

Messages, regardless of being highlighted or featured, can be manually removed from the Home Channel by EITHER:
- Using the "`Unfeature Message`" Context Command on the Message inside the Home Channel itself
  - *(Requires the User using the Command to have "`Send Messages`" Permission in the Home Channel itself, due to Discord limitations that are outside of HomeCord's control)*
- OR by using the "`Unfeature Message`" Context Command on the original Message in its original Channel

When featured or highlighted, the following parts of a Message are reposted to the Home Channel, if they exist in the original Message:
- The Message's content
- The Message's file attachments
- The Message's Author (display name & profile picture)

> [!NOTE]
> Any `@mentions` (be it `@user`, `@role`, or `@everyone`/`@here`) inside the Message are completely **suppressed** when being reposted to the Home Channel. This will ensure those mentions are **NOT** pinged again when reposted!

> [!NOTE]
> Please note that HomeCord will NOT highlight or feature non-standard Messages, and not Messages sent by non-Users. In other words: Messages sent by Bots, Webhooks, Discord's System Messages (such as Server Boost notifications or "This message has been pinned" notifications), and Messages with Polls in them, are all examples of what Messages are **NOT** featurable or highlightable to Home Channels.

> [!NOTE]
> Due to limitations imposed by Discord's public Bot API, Bots & Webhooks cannot send regular Messages with more than 2k (2000) characters in them. As such, if a Message is too long, it will not be featureable by HomeCord to Home Channels. However, those long Messages can still be automatically highlighted, though they will have some content cut off with a trailing "..." - this is to experiment with both ways of handling long Messages during HomeCord's Beta.
