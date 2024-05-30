*[Return to index](https://github.com/HomeCord/homecord-docs/blob/main/README.md)*

> [!NOTE]
> *This page is intended for Owners, Admins, and Moderators ("Mods") of Servers that are using HomeCord.*

---

# Getting Started with HomeCord (for Server Admins/Mods)

Let's skip all the introduction fluff and just jump right into it, eh? :)


## 1. Adding HomeCord to your Server

The first thing you'll want to do to setup HomeCord in your Server is to invite it. After all, HomeCord won't even know your Server *exists* unless you add it!

You can invite it to your Server by using [this Server App Invite Link here](https://discord.com/oauth2/authorize?client_id=1156152328290840606&permissions=537250896&scope=applications.commands+bot).

> [!IMPORTANT]
> You will need to have either "**Manage Server**" Permission, "**Admin**" Permission, or be the owner of, the Server you want to add HomeCord too. This requirement is enforced by Discord for any and *all* Server Apps you want to add to Servers.

---


## 2. Setting up HomeCord's Block List

> [!NOTE]
> Steps 2 and 3 can both be done in any order, or you can skip Step 2 completely.

While you can skip right into setting up HomeCord's "Home Channel", it's advised that you configure HomeCord's Block List in your Server first *(just so you don't end up with things being highlighted onto Home while you're setting up!)*.

To do that, you can run any of the three `/block` Subcommands. These allow you to block whole Categories, individual Channels, and/or Roles from being featured on your Server's Home Channel.

You do not need to add anything to the `/block` Command itself to add to the Block Lists, just send the Command in chat and you'll be given a Select Menu to search for & pick items to add to your Server's Block List, as exampled below:

![](https://zebby.is-from.space/r/o3q4UCyvOx.mp4)

If you make a mistake, you can use the `/unblock` Subcommands to remove items from your Server's Block List; and to view your Server's current Block List, run the `/blocklist` Command.

**More information about HomeCord's Block List System can be found [on this page here]().**

---


## 3. Setting up HomeCord's "Home Channel"

> [!NOTE]
> Steps 2 and 3 can both be done in any order.

*Now it's the moment you've been waiting for[!](https://www.youtube.com/watch?v=Y6PR4WvQngM)*

### 3a. Configuring your Home's initial settings

To begin setting up HomeCord's Home Channel for your Server, run the `/setup` Command in chat. This will begin the process of creating your Home Channel.

You will be initially given the default settings for your Home Channel. Below is a more detailed description of what each setting and option on `/setup`'s first page entails:

| Setting | Description |
|---------|-------------|
| Channel to Use | Set if you would like HomeCord to create the Home Channel for you, or if you want to use an existing Text Channel as your Home Channel. |
| Message Activity | Set the minimum activity threshold for highlighting Messages to your Home Channel. |
| Scheduled Events Activity | Set the minimum activity threshold for highlighting [Scheduled Events](https://support.discord.com/hc/en-us/articles/4409494125719). |
| Threads/Posts Activity | Set the minimum activity threshold for highlighting [Public Threads](https://support.discord.com/hc/en-us/articles/4403205878423), [Forum Posts](https://support.discord.com/hc/en-us/articles/6208479917079-Forum-Channels-FAQ), and [Media Posts](https://creator-support.discord.com/hc/en-us/articles/14346342766743). |
| Save & Proceed | Save the above settings, and move on to the next step |
| Cancel | Cancel setting up your Home Channel |

You can also outright disable HomeCord from automatically highlighting Messages/Events/Threads in their respective settings too.

Once you are happy with your initial settings, select the "Save & Proceed" option to move on to the next step.

### 3b. Setup Validation

This is just a sanity check, but this step of the setup process will validate if HomeCord has the correct Server Permissions to setup your new Home Channel. These will be described below, along with if each check is a requirement or not:

**FOR IF YOU SELECTED "Create Channel for Me":**

| Validation Check | Required? | Description |
|------------------|-----------|-------------|
| HomeCord has "Manage Channel" Permission (Server-level) | ✅ | Needed for HomeCord to be able to create a Home Channel outside of any Categories. |
| HomeCord has "Manage Webhooks" Permission (Server-level) | ✅ | Needed for HomeCord to create its Webhook in its Home Channel. |

**FOR IF YOU SELECTED TO USE AN EXISTING CHANNEL:**

| Validation Check | Required? | Description |
|------------------|-----------|-------------|
| HomeCord has "Manage Webhooks" Permission (Channel-level) | ✅ | Needed for HomeCord to create its Webhook in its Home Channel. |
| Home Channel has revoked "Send Messages" Permission for `@everyone` | ✅ | Required to prevent people sending messages in your Home Channel. |
| HomeCord has "Embed Links" Permission | ❌ | For HomeCord to be able to embed links for highlighted/featured Messages. |
| HomeCord has "Attach Files" Permission | ❌ | For HomeCord to be able to cross-post attachments as part of highlighted/featured Messages, if the original Message also had an Attachment. |
| `@everyone` has "Use External Emojis" Permission (Channel-level) | ❌ | For HomeCord to use its own custom Emojis as part of its Home Channels. |

If you update Server Permissions for HomeCord, you can re-run the Validation Checks with the provided Select Menu.


After you pass, at minimum the required, checks - then you can use the provided Select Menu to complete Setup and have HomeCord finish making a Home Channel for you!
