# Protected Reaction Emoji

## What is it?

Runs when reactions are added, checks the reaction emoji used and the roles of the folks they're used by to keep specific emoji limited to staff reactions only. If someone uses an emoji they aren't supposed to, YAG instantaneously removes that reaction.

## How do I set it up?

Requires the [YAGPDB Discord bot](https://yagpdb.xyz).

Add the contents of the included file as a Custom Command in YAGPDB's dashboard. The file provides guidance on the type of command to set up.

Make modifications to the values in the `$settings` map based on your needs:

- **allowedRoles** lists the IDs of the roles who are permitted to use the restricted emojis for reactions
- **protectedEmoji** lists the names and IDs of the emoji that are restricted. See instructions in the file for acquiring the proper identifiers
- **showWarning**, boolean, determines whether the restricted emoji reactions will be removed silently or if a self-deleting warning will be shown

## How do I use it?

Runs automatically against all reactions used in the channels for which it's configured.
