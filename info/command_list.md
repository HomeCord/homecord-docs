*[Return to index](https://github.com/HomeCord/homecord-docs/blob/main/README.md)*

# HomeCord's Command List

Below is a list of Commands HomeCord has, what type of Command they are, and their default Permission requirements to *use* the Command (if any).

| Command | Type | Default Permission Requirement | Description |
|---------|------|--------------------------------|-------------|
| `/block` | Slash | Manage Server | Used to add Channels, Categories, or Roles to your Server's Home Block List |
| `/blocklist` | Slash | Manage Server | Shows your Server's Home Block List |
| `/feature` | Slash | Manage Channels | Manually feature a Channel, Scheduled Event, or Thread to your Home Channel |
| `/invite` | Slash | - | Shows the invite link which can be used to add HomeCord to your own Servers |
| `/preferences` | Slash | - | Toggle if you want to disallow your own Messages from being featured or highlighted by HomeCord |
| `/refresh` | Slash | Manage Server | Force-refresh your Server's Home Channel. ⚠ Has a very long cooldown of 7 days |
| `/settings` | Slash | Manage Server | View or edit your Server's Home Channel Settings |
| `/setup` | Slash | Manage Server | Begin the setup process for creating a Home Channel in your Server with HomeCord |
| `/subscribe` | Slash | Manage Webhooks | Subscribe any Text Channel in your Server to HomeCord's updates & announcements feed |
| `/support` | Slash | - | Shows a link to HomeCord's Support Server, and to this Documentation |
| `/unblock` | Slash | Manage Server | Used to remove Channels, Categories, or Roles from your Server's Home Block List |
| `/unfeature` | Slash | Manage Channels | Manually remove a featured or highlighted Channel, Scheduled Event, or Thread, from your Home Channel |
| "`Feature Message`" | Message Context | Manage Messages | Manually feature a Message to your Home Channel |
| "`Unfeature Message`" | Message Context | Manage Messages | Manually remove a featured or highlighted Message from your Home Channel |

---

## Commands: Permission Requirements

If you want to override the default Permission requirements for HomeCord's Commands, you can do so by going to **Server Settings > Integrations > HomeCord** in your Server, and editing the Command Permission requirements there.

> [!NOTE]
> Sadly, you can only edit Bot Command Permissions on Desktop & Web versions of Discord, not Mobile versions.
