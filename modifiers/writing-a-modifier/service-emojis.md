# Service: Emojis

The Emojis service allows the Modifier to install UI Emoji Packs onto your bot. This will require an **emoji.json** file, which defines which emoji the emoji files correspond to.

## Making an Emoji Pack

To create an Emoji Pack, you will first need to design a set of emojis. These may be animated (.gif) or static (.png, .jpg, etc), as long as Discord supports the file formats. To see which emojis you may make, please refer to the guide below.

## List of UI emojis

All emojis are compatible from **v2.0.1 (release 51)** unless stated otherwise.

* **back**: Used in UI buttons leading to a previous phase of an interaction.
* **prev**: Used in UI buttons leading to the previous page of a list embed.
* **next**: Used in UI buttons leading to the next page of a list embed.
* **first**: Used in UI buttons leading to the first page of a list embed.
* **last**: Used in UI buttons leading to the last page of a list embed.
* **search**: Used in search UI buttons, usually in list embeds.
* **command**: Used in list embeds to denote that the embed is displaying a list of bot commands.
* **emoji**: Used in list embeds to denote that the embed is displaying a list of global emojis.
* **rooms**: Used in list embeds to denote that the embed is displaying a list of rooms.
* **leaderboard**: Used in list embeds to denote that the embed is displaying the Unifier EXP leaderboard.
* **success**: Used for confirmation or when a task has been completed successfully.
* **warning**: Used for non-critical alerts or when there has been an issue but the task is able to function regardless.
* **error**: Used for critical alerts or when a task fails.
* **install**: Used in Modifier management embeds.
* **safety (v3.1.0, release 81)**: Used in selection UI to represent safe mode boot. May be used for other purposes in the future.
* **gear (v3.1.0, release 81)**: Used in selection UI to represent core boot. May be used for other purposes in the future.
* **info (v3.1.9, release 90)**: Used throughout all of Unifier when displaying information.
* **loading (v3.1.9, release 90)**: Used in embeds or messages when a task that needs some time to complete is running.

## Compatibility

Modifiers offering Emojis service should have a minimum Unifier release requirement of **51** or above.

If an emoji is not compatible with the version of a Unifier instance, it will install the emoji to the home server anyways, but it will not be used in any part of the bot.
