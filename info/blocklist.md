*[Return to index](https://github.com/HomeCord/homecord-docs/blob/main/README.md)*

# How does HomeCord's Block List system work?

This page will cover each part of HomeCord's Block List system, which can be used by Server Managers to prevent items from being featured or highlighted to their Server's Home Channel.

> [!IMPORTANT]
> By "Server Managers", we mean those with at minimum the "`Manage Server`" Permission.
> 
> This is also the default Permission requirement needed to be able to use the `/block`, `/unblock`, and `/blocklist` Commands mentioned on this page.

> [!NOTE]
> If you have any Server App logging Channels in your Server, and want to help HomeCord, you can revoke the "`View Channel`" Permission from the HomeCord Server App in your logging Channels.
> 
> This won't stop your Moderators & Admins from manually featuring those logs, but it *does* help massively reduce the amount of Message API events HomeCord receives!

---

## Block List Commands: How to use them

To allow bulk-adding or bulk-removing items to a Server's Block List, the `/block` and `/unblock` Commands *don't* have fields in their initial Command objects for adding items.

Instead, you have to run the Command first as is, then HomeCord will previde you a Select Menu for selecting multiple items at once.

For example: You run `/block channel` in a Channel, and HomeCord will show you a Channel Select Menu for selecting up to 25 Channels to bulk-add at once.

---

## Block List: Channels

Starting with Channels, Server Managers can use the `/block channel` Command to add up to 25 individual Channels to their Server's Block List in HomeCord.

Adding a Channel to HomeCord's Block List means that the following items *from that specific Channel* are prevented from being featured & highlighted to the Home Channel:
- Messages sent in the Channel, and/or in the Channel's Threads
- Threads within the Channel (including Forum Posts and Media Posts for those respective Channel types)

---

## Block List: Categories

If Server Managers want to block a whole Category of Channels instead of just individual Channels; they can use HomeCord's `/block category` Command. This will allow adding up to 25 Categories to HomeCord's Block List.

Categories added to the Block List will have the following blocked from being highlightable/featureable:
- Messages sent in *any* Channels within that Category
- Messages sent in *any* Threads within any Channels within that Category
- Threads within *any* Channel within that Category

---

## Block List: Roles

The final part of the Block List system: Roles. If Servers want to, they can add up to 25 Roles to HomeCord's Block List via use of the `/block role` Command.

If a User has a blocked Role, their Messages will *not* be featureable, nor highlightable, to the Server's Home Channel.

This can be useful for punishment Roles, or if you have Members who you don't want to highlight their Messages for (in a non-negative way, such as if you want to protect certain Members).
