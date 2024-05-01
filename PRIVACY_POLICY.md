*[Return to index](https://github.com/HomeCord/homecord-docs/blob/main/README.md)*

# HomeCord - Privacy Policy
Last Updated: 1st May 2024

Effective: 1st May 2024

---

## Introduction
**HomeCord** (henseforth "**HomeCord**") does __not__, and will __never__, collect & store Messages, User Data, or Server Data without explicit notice & consent.
Additionally, **HomeCord** will __never__ sell or give away the Data that it does store.

The developers of **HomeCord** firmly believes in a "we don't want your data keep it away from us" process - thus, **HomeCord** will be developed as "stateless" as possible (i.e: without needing to store any information or data at all). If features and functions are not possible to develop "stateless", we will explicitly include them in this **Privacy Policy**, covering exactly what is needed to be stored, for what purpose, and how that data can be removed from **HomeCord** on request.

**HomeCord**'s source code is viewable in **HomeCord**'s GitHub Repo ( https://github.com/HomeCord/homecord ).

---

## Data Collection & Purposes
Below will be a list of what **HomeCord** *does* store.

As a reminder: User IDs, Server IDs, Channel IDs, Message IDs, Role IDs, and Custom Emoji IDs are all publicly accessible from Discord's public API and official Clients/Apps.

### For Home Channel Settings
- Server ID
  - *So **HomeCord** knows which Server these Settings belong to.*
- Channel ID
  - *So **HomeCord** knows which Text Channel the Server has assigned as the "Home Channel".*
- Webhook ID
  - *So **HomeCord** can send/edit/delete its own Messages inside of the assigned "Home Channel", and only inside of the "Home Channel", to highlight aspects of the Server.*
- Message IDs (inside of the "Home Channel")
  - *So **HomeCord** can know which of its own Messages inside of the "Home Channel" should be edited to highlight respective aspects of the Server.*

### For User Preferences
- User ID
  - *So **HomeCord** knows which User these Preferences belong to.*

### Home Block List
- Server ID
  - *So **HomeCord** knows which Server these blocked items are for.*
- Channel ID / Category ID / Role ID
  - *So **HomeCord** knows which Channel, Category, and/or Role was added to the Server's Block List, and thus prevent aspects from being highlighted from those spaces or Members.*

### Important/Featured Channels
- Server ID
  - *So **HomeCord** knows which Server this Featured Channel belongs to, and thus place it in the correct "Home Channel".*
- Channel ID
  - *So **HomeCord** knows which Channel the Server assigned as a Featured Channel.*
- User-inputted custom string [Optional]
  - *An optional bit of text the Server can assign as a description for the Featured Channel's listing in the "Home Channel".*

### Featured/Highlighted Messages, Scheduled Events, and Threads
- Server ID
  - *So **HomeCord** knows which Server this featured aspect belongs to, and thus place it in the correct "Home Channel".*
- Message ID / Scheduled Event ID / Thread ID
  - *So **HomeCord** knows which Message, Event, and/or Thread was featured or highlighted.*
  - *In the case of Featured/Highlighted Messages, both the ID for the original Message, and the ID for the reposted version of that Message inside the "Home Channel", are stored.*
  - *The content of these are NEVER stored, only their IDs.*

---

## Use of Locale Data
**HomeCord** also makes use of the publicly available locale data (i.e: what language Users and Servers have set) Discord sends to all Bots using Discord's public API for "Interactions" (e.g: Slash Commands, Context Commands, Select Menus, Buttons, Modals). This locale data is only used for knowing which language **HomeCord** should send its responses in, and is __NOT__ stored or tracked in any way.

You can see the public API Documentation regarding what the locale data includes on these official Discord API Documentation Pages:
- [API Locale Reference](https://discord.com/developers/docs/reference#locales)
- [Locale field in Interaction Objects](https://discord.com/developers/docs/interactions/receiving-and-responding#interaction-object)

---

## Final Notes
If you decide to stop using **HomeCord**, then **HomeCord** will automatically remove all data connected to a Server when it is removed or kicked from the Server in question.

Additionally, deleting from Discord a Channel, Message, Event, or Thread, whose ID has been stored as a featured/highlighted aspect, or as a core part of the "Home Channels", will cause HomeCord to also delete the respective IDs from itself too. You can also manually remove featured/highlighted aspect's IDs via use of the Unfeature Commands.

The Developer of **HomeCord**, TwilightZebby, is contactable for matters regarding **HomeCord** via GitHub, preferrably via opening an Issue Ticket or Discussion on **HomeCord**'s [GitHub Repo](https://github.com/HomeCord/homecord). You can also contact TwilightZebby via **HomeCord**'s [Support Server](https://discord.gg/4bFgUyWUMY) on Discord.

Please also see [Discord's own Privacy Policy](https://discord.com/privacy).

*This Privacy Policy is subject to change at any time.*
