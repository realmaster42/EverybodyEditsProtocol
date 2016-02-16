# Everybody Edits Messages Protocol
The description of the Everybody Edits game protocol.

## Table of contents
- [Game Information](#game-information)
- [Room Types](#room-types)
- [Receive Messages](#receive-messages)
  - [access](#rm-access)
  - [add](#rm-add)
  - [addedToCrew](#rm-addedToCrew)
  - [admin](#rm-admin)
  - [allowSpectating](#rm-allowSpectating)
  - [aura](#rm-aura)
  - [autotext](#rm-autotext)
  - [b](#rm-b)
  - [backgroundColor](#rm-backgroundColor)
  - [badgeChange](#rm-badgeChange)
  - [banned](#rm-banned)
  - [bc](#rm-bc)
  - [br](#rm-br)
  - [bs](#rm-bs)
  - [c](#rm-c)
  - [campaignRewards](#rm-campaignRewards)
  - [clear](#rm-clear)
  - [completedLevel](#rm-completedLevel)
  - [crewAddRequest](#rm-crewAddRequest)
  - [crewAddRequestFailed](#rm-crewAddRequestFailed)
  - [editRights](#rm-editRights)
  - [effect](#rm-effect)
  - [effectlimits](#rm-effectlimits)
  - [face](#rm-face)
  - [favorited](#rm-favorited)
  - [givemagicbrickpackage](#rm-givemagicbrickpackage)
  - [givemagicsmiley](#rm-givemagicsmiley)
  - [god](#rm-god)
  - [hide](#rm-hide)
  - [hideLobby](#rm-hideLobby)
  - [info](#rm-info)
  - [info2](#rm-info2)
  - [init](#rm-init)
  - [init2](#rm-init2)
  - [joinCampaign](#rm-joinCampaign)
  - [k](#rm-k)
  - [kill](#rm-kill)
  - [ks](#rm-ks)
  - [lb](#rm-lb)
  - [left](#rm-left)
  - [liked](#rm-liked)
  - [lobbyPreviewEnabled](#rm-lobbyPreviewEnabled)
  - [lostaccess](#rm-lostaccess)
  - [m](#rm-m)
  - [magic](#rm-magic)
  - [minimapEnabled](#rm-minimapEnabled)
  - [mod](#rm-mod)
  - [muted](#rm-muted)
  - [ps](#rm-ps)
  - [psi](#rm-psi)
  - [pt](#rm-pt)
  - [reset](#rm-reset)
  - [restoreProgress](#rm-restoreProgress)
  - [roomDescription](#rm-roomDescription)
  - [roomVisible](#rm-roomVisible)
  - [saved](#rm-saved)
  - [say](#rm-say)
  - [say_old](#rm-say_old)
  - [show](#rm-show)
  - [smileyGoldBorder](#rm-smileyGoldBorder)
  - [team](#rm-team)
  - [tele](#rm-tele)
  - [teleport](#rm-teleport)
  - [time](#rm-time)
  - [toggleGod](#rm-toggleGod)
  - [ts](#rm-ts)
  - [unfavorited](#rm-unfavorited)
  - [unliked](#rm-unliked)
  - [updatemeta](#rm-updatemeta)
  - [upgrade](#rm-upgrade)
  - [worldReleased](#rm-worldReleased)
  - [wp](#rm-wp)
  - [write](#rm-write)
- [Send Messages](#send-messages)
  - [access](#sm-access)
  - [addToCrew](#sm-addToCrew)
  - [admin](#sm-admin)
  - [aura](#sm-aura)
  - [autosay](#sm-autosay)
  - [b](#sm-b)
  - [c](#sm-c)
  - [crown](#sm-crown)
  - [caketouch](#sm-caketouch)
  - [checkpoint](#sm-checkpoint)
  - [changeBadge](#sm-changeBadge)
  - [clear](#sm-clear)
  - [death](#sm-death)
  - [diamondtouch](#sm-diamondtouch)
  - [effect](#sm-effect)
  - [favorite](#sm-favorite)
  - [god](#sm-god)
  - [hologramtouch](#sm-hologramtouch)
  - [init](#sm-init)
  - [init2](#sm-init2)
  - [key](#sm-key)
  - [kill](#sm-kill)
  - [levelcomplete](#sm-levelcomplete)
  - [like](#sm-like)
  - [m](#sm-m)
  - [mod](#sm-mod)
  - [name](#sm-name)
  - [pressKey](#sm-pressKey)
  - [ps](#sm-ps)
  - [rejectAddToCrew](#sm-rejectAddToCrew)
  - [requestAddToCrew](#sm-requestAddToCrew)
  - [reset](#sm-reset)
  - [save](#sm-save)
  - [say](#sm-say)
  - [setAllowSpectating](#sm-setAllowSpectating)
  - [setCurseLimit](#sm-setCurseLimit)
  - [setHideLobby](#sm-setHideLobby)
  - [setLobbyPreviewEnabled](#sm-setLobbyPreviewEnabled)
  - [setMinimapEnabled](#sm-setMinimapEnabled)
  - [setRoomDescription](#sm-setRoomDescription)
  - [setRoomVisible](#sm-setRoomVisible)
  - [setStatus](#sm-setStatus)
  - [setZombieLimit](#sm-setZombieLimit)
  - [smiley](#sm-smiley)
  - [smileyGoldBorder](#sm-smileyGoldBorder)
  - [team](#sm-team)
  - [time](#sm-time)
  - [touch](#sm-touch)
  - [unfavorite](#sm-unfavorite)
  - [unlike](#sm-unlike)
- [Models](#models)
  - [Auto Text](#model-auto-text)
  - [Badges](#model-badges)
  - [Campaign Status](#model-campaign-status)
  - [Crew World Status](#model-crew-status)
  - [Effects](#model-effects)
  - [Keys](#model-keys)
  - [Teams](#model-teams)

___

# <a id="game-information">Game Information</a>
```
GameID = everybody-edits-su9rn58o40itdbnw69plyw
Version = 206
```

# <a id="room-types">Room Types</a>
```
Normal      = EverybodyeditsXXX
Beta        = BetaXXX
Lobby       = LobbyXXX
Crew Lobby  = CrewLobbyXXX
Guest Lobby = GuestLobbyXXX

(Replace XXX with the current version)
```
___

# <a id="receive-messages">Receive messages</a>

### <a id="rm-access">"access"</a>
Occurs when you are given edit rights in the world.

### <a id="rm-add">"add"</a>
Occurs when someone joins the world.

`[0] Integer` Id
> The player's identifier.

`[1] String` Username
> The player's username.

`[2] String` ConnectUserId
> The player's unique user identifier.

`[3] Integer` Smiley
> The player's smiley identifier.

`[4] Double` X
> The x coordinate of the player's position.

`[5] Double` Y
> The y coordinate of the player's position.

`[6] Boolean` God Mode
> Value indicating whether the player is in god mode.

`[7] Boolean` Admin Mode
> Value indicating whether the player is in administrator mode.

`[8] Boolean` Can Chat
> Value indicating whether the player is allowed to chat.

`[9] Integer` Gold Coins
> The amount of player's gold coins.

`[10] Integer` Blue Coins
> The amount of player's blue coins.

`[11] Integer` Deaths
> The amount of player's deaths.

`[12] Boolean` Is Friend
> Value indicating whether the player is a friend.

`[13] Boolean` Gold Membership
> Value indicating whether the player has gold membership.

`[14] Boolean` Gold Smiley Border
> Value indicating whether the player is wearing gold smiley border.

`[15] Boolean` Moderator Mode
> Value indicating whether the player is in moderator mode.

`[16] Integer` Team
> The player's team identifier.
> *See [Teams](#model-teams).*

`[17] Integer` Aura Shape
> The player's aura shape identifier.

`[18] Integer` Aura Color
> The player's aura color identifier.

`[19] Integer` Chat Color
> The player's chat color.

`[20] String` Badge
> The player's badge identifier.
> *See [Badges](#model-badges).*

`[21] Boolean` Crew Member
> Value indicating whether the player is a member of the crew to which belongs this world.

`[22] Boolean` Can Edit
> Value indicating whether the player can edit in this world.  
> **NOTE:** This is received only by the world owner.

### <a id="rm-addedToCrew">"addedToCrew"</a>
Occurs when world was successfully added to a crew.

`[0] String` Crew Id
> The identifier of the crew to which the world was added.

`[1] String` Crew Name
> The name of the crew to which the world was added.

### <a id="rm-admin">"admin"</a>
Occurs when a player toggles administrator mode.

`[0] Integer` Player Id
> The player's identifier.

`[1] Boolean` Is In Administrator Mode
> Value indicating whether the player is now in administrator mode.

### <a id="rm-allowSpectating">"allowSpectating"</a>
Occurs when spectating in the world setting is changed.

`[0] Boolean` Allowed
> Value indicating whether spectating is allowed.

### <a id="rm-aura">"aura"</a>
Occurs when a player changed their aura shape or color.

`[0] Integer` Player Id
> The player's identifier.

`[2] Integer` Aura Shape
> The aura shape identifier.

`[2] Integer` Aura Color
> The aura color identifier.

### <a id="rm-autotext">"autotext"</a>
Occurs when a player uses auto-text.

`[0] Integer` Payer Id
> The player's identifier.

`[1] String` Auto-Text
> The automatic text value.
> *See [Auto Text](#model-auto-text).*

___

### <a id="rm-b">"b"</a>
Occurs when a block is placed in the world.

`[0] Integer` Layer
> The layer identifier.

`[1] UInt` X
> The x coordinate of the block's position.

`[2] UInt` Y
> The y coordinate of the block's position.

`[3] UInt` Block Id
> The block identifier.

`[4] UInt` Player Id
> The identifier of the player which placed this block.

### <a id="rm-backgroundColor">"backgroundColor"</a>
Occurs when the background color of the world is changed.

`[0] UInt` Color
> The color of the background.
> **NOTE:** Transparent color means that the custom background color is disabled.

### <a id="rm-badgeChange">"badgeChange"</a>
Occurs when a player changes badge.

`[0] Integer` Player Id
> The player's identifier.

`[1] String` Badge
> The badge identifier.
> *See [Badges](#model-badges).*

### <a id="rm-banned">"banned"</a>
Occurs when trying to join a world with a banned account.

### <a id="rm-bc">"bc"</a>
Occurs when a block with number value is placed in the world.

`[0] UInt` X
> The x coordinate of the block's position.

`[1] UInt` Y
> The y coordinate of the block's position.

`[2] UInt` Block Id
> The block's identifier.

`[3] UInt` Number Value
> The number value.

`[4] UInt` Player Id
> The identifier of the player which placed this block.

### <a id="rm-br">"br"</a>
Occurs when a morphable block is placed in the world.

`[0] UInt` X
> The x coordinate of the block's position.

`[2] UInt` Y
> The y coordinate of the block's position.

`[3] UInt` Morph
> The morph identifier.

`[4] Integer` Layer
> The layer identifier.

`[5] UInt` Player Id
> The identifier of the player which placed this block.

### <a id="rm-bs">"bs"</a>
Occurs when a sound block is placed in the world.

`[0] UInt` X
> The x coordinate of the block's position.

`[1] UInt` Y
> The y coordinate of the block's position.

`[2] UInt` Block Id
> The block identifier.

`[3] Integer` Sound Id
> The sound identifier.

`[4] UInt` Player Id
> The identifier of the player which placed this block.

___

### <a id="rm-c">"c"</a>
Occurs when a player's gold or blue coin count changes.

`[0] Integer` Player Id
> The player's identifier.

`[1] Integer` Gold Coins
> The amount of collected gold coins.

`[2] Integer` Blue Coins
> The amount of collected blue coins.

`[3] UInt` X
> The x coordinate of the coin's position.

`[4] UInt` Y
> The y coordinate of the coin's position.

### <a id="rm-campaignRewards">"campaignRewards"</a>
Occurs when received rewards for completing a campaign world.

`[0] Boolean` Received Badge
> Value indicating whether received a badge.

This message has 2 possible outcomes:

1. If the player received a badge:

`[1] String` Badge Title
> The title of the badge.

`[2] String` Badge Description
> The description of the badge.

`[3] String` Badge URL
> The image URL of the badge.

2. If the player didn't receive a badge:

`[1] String` World URL
> The image URL of the next world in the campaign.

Both of these outcomes are followed with list of rewards described as follows:

`[...] String` Id
> The identifier of the reward.

`[...] UInt` Quantity
> The quantity of the reward.

### <a id="rm-clear">"clear"</a>
Occurs when the world is cleared.

`[0] Integer` Width
> The width of the world.

`[1] Integer` Height
> The height of the world.

`[2] UInt` Border Block Id
> The identifier of the block used as a world border.

`[3] UInt` Fill Block Id
> The identifier of the block used to fill the world.

### <a id="rm-completedLevel">"completedLevel"</a>
Occurs when completing a world by touching win trophy.  
**NOTE:** If player received campaign rewards, ["campaignRewards"](#rm-campaignRewards) message is received instead.

### <a id="rm-crewAddRequest">"crewAddRequest"</a>
Occurs when a player requests to add the world to their crew.

`[0] String` Username
> The username of the player which requested the add the world to their crew.

`[1] String` Crew Name
> The name of the crew to which they want to add the world.

### <a id="rm-crewAddRequestFailed">"crewAddRequestFailed"</a>
Occurs when an attempt to request adding of the world to a crew didn't succeed.
(For example when the world owner wasn't online in the world or rejected the request.)

`[0] String` Reason
> The reason of the failure.

___

### <a id="rm-editRights">"editRights"</a>
Occurs when a player receives or loses edit rights.
**NOTE:** You receive this even only if you are the owner of the world.

`[0] Integer` Player Id
> The player's identifier.

`[1] Boolean` Can Edit
> Value indicating whether the player is now allowed to edit in the world.

### <a id="rm-effect">"effect"</a>
Occurs when a player gains or looses an effect.

`[0] Integer` Player Id
> The player's identifier.

`[1] Integer` Effect
> The effect's identifier.
> *See [Effects](#model-effects).*

`[2] Boolean` Enabled
> Value indicating whether the effect is enabled.

Conditional parameters:

`[3] Double` Argument
> The optional argument of the effect. (time left, number of jumps, etc.)

`[4] Integer` Duration
> The duration of the effect.

### <a id="rm-effectlimits">"effectlimits"</a>
Occurs when effect limits are changed.

`[0] Integer` Curse Limit
> The curse limit.

`[1] Integer` Zombie Limit
> The zombie limit.

___

### <a id="rm-face">"face"</a>
Occurs when someone changes their smiley.

`[0] Integer` Player Id
> The player's identifier.

`[1] Integer` Smiley
> The smiley identifier.

### <a id="rm-favorited">"favorited"</a>
Occurs when you successfully favorited the world.

___

### <a id="rm-givemagicbrickpackage">"givemagicbrickpackage"</a>
Occurs when you are given a magic brick package.

`[0] String` Package
> The identifier of the magic brick package.

### <a id="rm-givemagicsmiley">"givemagicsmiley"</a>
Occurs when you are given magic smiley.

`[0] String` Smiley
> The identifier of the magic smiley.

### <a id="rm-god">"god"</a>
Occurs when a player toggles god mode.

`[0] Integer` Player Id
> The player's identifier.

`[1] Boolean` Is In God Mode
> Value indicating whether this player is now in god mode.

___

### <a id="rm-hide">"hide"</a>
Occurs when a player touches a key or timed doors change their state.

`[0] Integer` Player Id
> The player's identifier.

`[1] String` Key
> The name of the key (or timed door).
> *See [Keys](#model-keys).*

### <a id="rm-hideLobby">"hideLobby"</a>
Occurs when world hidden in the lobby setting is changed.

`[0] Boolean` Hidden
> Value indicating whether the world is now hidden from the lobby and profile.

___

### <a id="rm-info">"info"</a>
Occurs when the server sends information pertaining to low-level functions like (a) you were kicked or (b) the room is full or (c) rate limit exceeded.

`[0] String` Title
> The title of the message.

`[1] String` Text
> The text of the message.

### <a id="rm-info2">"info2"</a>
Occurs when the server sends low priority information that can be displayed in non-invasive pop-up.

`[0] String` Title
> The title of the message.

`[1] String` Text
> The text of the message.

### <a id="rm-init">"init"</a>
Occurs when the player initially joins the room.
Contains world information such as world name and the world content.

`[0] String` Owner Username
> The username of the world owner.

`[1] String` World Name
> The name of the world.

`[2] Integer` Plays
> The amount of plays.

`[3] Integer` Favorites
> The amount of favorites.

`[4] Integer` Likes
> The amount of likes.

`[5] Integer` Player Id
> The player's identifier.

`[6] Integer` Smiley
> The player's smiley identifier.

`[7] Integer` Aura Shape
> The player's aura shape identifier.

`[8] Integer` Aura Color
> The player's aura color identifier.

`[9] Boolean` Gold Smiley Border
> Value indicating whether the player is wearing gold smiley border.

`[10] Double` X
> The x coordinate of the player's spawn position.

`[11] Double` Y
> The y coordinate of the player's spawn position.

`[12] UInt` Chat Color
> The player's chat color.

`[13] String` Username
> The player's username.

`[14] Boolean` Can Edit
> Value indicating whether the player can edit.

`[15] Boolean` Is Owner
> Value indicating whether the player is world owner.

`[16] Boolean` Favorited
> Value indicating whether the player has favorited this world.

`[17] Boolean` Liked
> Value indicating whether the player has liked this world.

`[18] Integer` World Width
> The width of the world.

`[19] Integer` World Height
> The height of the world.

`[20] Double` World Gravity Multiplier
> The world's gravity multiplier.

`[21] UInt` Background Color
> The color of the background.
> **NOTE:** Transparent color means that the custom background color is disabled.

`[22] Boolean` Accessible
> Value indicating whether this world is accessible by other players.

`[23] Boolean` Hidden From Lobby
> Value indicating whether this world is hidden from the lobby and profile.

`[24] Boolean` Spectating Allowed
> Value indicating whether spectating in this world is allowed.

`[25] String` Description
> The description of the world.

`[26] Integer` Curse Limit
> The curse limit.

`[27] Integer` Zombie Limit
> The zombie limit.

`[28] Boolean` Belongs To Campaign
> Value indicating whether this world is part of a campaign.

`[29] String` Crew Id
> The identifier of the crew to which belongs this world.

`[30] String` Crew Name
> The name of the crew to which belongs this world.

`[31] Boolean` Can Change World Options
> Value indicating whether the player can change world options.

`[32] Integer` Crew Status
> The crew status of the world.
> *See [Crew World Status](#model-crew-status).*

`[33] String` Badge
> The player's badge identifier.
> *See [Badges](#model-badges).*

`[34] Boolean` Is Crew Member
> Value indicating whether the player is a member of the crew to which belongs this world.

`[35] Boolean` Minimap Enabled
> Value indicating whether the minimap is enabled in this world.

`[36] Boolean` Lobby Preview Enabled
> Value indicating whether the lobby preview is enabled in this world.

`[37] String` ws
> Indicates the start of the world data.

`[...]`
> The serialized world data.

`[...] <String>` we
> Indicates the end of the world data.

### <a id="rm-init2">"init2"</a>
Occurs when joining world is completed.

___

### <a id="rm-joinCampaign">"joinCampaign"</a>
Occurs when player joins a campaign world.
Contains information about campaign data of the world.

`[0] String` Title
> The title of the campaign.

`[1] Integer` Status
> The campaign status.
> *See [Campaign Status](#model-campaign-status).*

Additional parameters received when this campaign world is unlocked:

`[2] Integer` Difficulty
> The campaign difficulty.

`[3] Integer` Tier
> The campaign tier of this world.

`[4] Integer` Tiers
> The amount of tiers in the campaign.

___

### <a id="rm-k">"k"</a>
Occurs when a player collects gold crown.

`[0] Integer` Player Id
> The player's identifier.  
> **NOTE:** Set to `-1` if there is no player with a crown.

### <a id="rm-kill">"kill"</a>
Occurs when a player is killed due to expired effect or /kill, /killall commands.

`[0] Integer` Player Id
> The player's identifier.

### <a id="rm-ks">"ks"</a>
Occurs when someone receives a silver crown.

`[0] Integer` Player Id
> The player's identifier.

___

### <a id="rm-lb">"lb"</a>
Occurs when someone places a label block.

`[0] UInt` X
> The x coordinate of the block's position.

`[1] UInt` Y
> The y coordinate of the block's position.

`[2] Integer` Block Id
> The identifier of the block.

`[3] String` Text
> The text.

`[4] String` Text Color
> The color of the text.

`[5] UInt` Player Id
> The identifier of the player which placed this block.

### <a id="rm-left">"left"</a>
Occurs when someone leaves the world.

`[0] Integer` Player Id
> The player's identifier.

### <a id="rm-liked">"liked"</a>
Occurs when you successfully liked the world.

### <a id="rm-lobbyPreviewEnabled">"lobbyPreviewEnabled"</a>
Occurs when lobby preview is enabled or disabled.

`[0] Boolean` Enabled
> Value indicating whether the lobby preview is now enabled.

### <a id="rm-lostaccess">"lostaccess"</a>
Occurs when you lose edit rights.

___

### <a id="rm-m">"m"</a>
Occurs when someone moves.

`[0] Integer` Player Id
> The player's identifier.

`[1] Double` X
> The x coordinate of the player's position.

`[2] Double` Y
> The y coordinate of the player's position.

`[3] Double` Horizontal Speed
> The horizontal speed.

`[4] Double` Vertical Speed
> The vertical speed.

`[5] Double` Horizontal Modifier
> The horizontal movement modifier.

`[6] Double` Vertical Modifier
> The vertical movement modifier.

`[7] Integer` Horizontal Movement
> Value indicating horizontal movement direction.  
> `-1` means left, `1` means right and `0` means that player is not moving horizontally.

`[8] Integer` Vertical Movement
> Value indicating vertical movement direction.  
> `-1` means up, `1` means down and `0` means that player is not moving vertically.

`[9] Boolean` Space Pressed
> Value indicating whether the player is holding down space-bar.

`[10] Boolean` Space Just Pressed
> Value indicating whether the player has just pressed down space-bar.

### <a id="rm-magic">"magic"</a>
Occurs when you are given magic reward.

### <a id="rm-minimapEnabled">"minimapEnabled"</a>
Occurs when the minimap is enabled or disabled.

`[0] Boolean` Minimap Enabled
> Value indicating whether the minimap is now enabled.

### <a id="rm-mod">"mod"</a>
Occurs when a player toggles moderator mode.

`[0] Integer` Player Id
> The player's identifier.

`[1] Boolean` Is In Moderator Mode
> Value indicating whether the player is now in moderator mode.

### <a id="rm-muted">"muted"</a>
Occurs when you successfully muted or un-umted someone.

`[0] Integer` Player Id
> The player's identifier.

`[1] Boolean` Muted
> Value indicating whether the player is now muted.

___

### <a id="rm-ps">"ps"</a>
Occurs when someone touches purple switch.

`[0] Integer` Player Id
> The player's identifier.

`[1] Integer` Switch Id
> The switch identifier.

`[2] Integer` Enabled
> Value indicating the state of the switch.  
> `1` means pressed and `0` not.

### <a id="rm-psi">"psi"</a>
Occurs after join. Contains information about initial switch states.

`[0] Integer` Player Id
> The player's identifier.

`[1] ByteArray` Switch States
> The byte array describing switch states.

### <a id="rm-pt">"pt"</a>
Occurs when a portal is placed in the world.

`[0] UInt` X
> The x coordinate of the block's position.

`[1] UInt` Y
> The y coordinate of the block's position.

`[2] UInt` Block Id
> The block identifier.

`[3] UInt` Portal Rotation
> The portal rotation.

`[4] UInt` Portal Id
> The portal identifier.

`[5] UInt` Portal Target
> The portal target identifier.

`[6] Integer` Player Id
> The identifier of the player which placed this block.

___

### <a id="rm-reset">"reset"</a>
Occurs when world is reverted to the last save using /loadlevel command.

`[0] String` ws
> Indicates the start of the world data.

`[...]`
> The serialized world data.

`[...]` we
> Indicates the end of the world data.

### <a id="rm-restoreProgress">"restoreProgress"</a>
Occurs when your campaign progress is restored.

`[0] Integer` Player Id
> The player's identifier.

`[1] Double` X
> The x coordinate of the player's position.

`[2] Double` Y
> The y coordinate of the player's position.

`[3] Integer` Gold Coins
> The amount of collected gold coins.

`[4] Integer` Blue Coins
> The amount of collected blue coins.

`[5] ByteArray` Gold Coin X
> The x coordinates array of the gold coins positions.

`[6] ByteArray` Gold Coin Y
> The y coordinates array of the gold coins positions.

`[7] ByteArray` Blue Coin X
> The x coordinates array of the blue coins positions.

`[8] ByteArray` Blue Coin Y
> The y coordinates array of the blue coins positions.

`[9] Integer` Deaths
> The amount of deaths.

`[10] UInt` Spawn X
> The x coordinate of the player's checkpoint position.

`[11] UInt` Spawn Y
> The y coordinate of the player's checkpoint position.

`[12]: ByteArray` Switch States
> The byte array describing purple switches states.

`[13] Double` Horizontal Speed
> The horizontal movement speed.

`[14] Double` Vertical Speed
> The vertical movement speed.

### <a id="rm-roomDescription">"roomDescription"</a>
Occurs when the world description is changed.

`[0] String` Description
> The world description.

### <a id="rm-roomVisible">"roomVisible"</a>
Occurs when the world accessibility is changed.

`[0] Boolean` Accessible
> Value indicating whether the world is now accessible by other players.

___

### <a id="rm-saved">"saved"</a>
Occurs when you successfully saved world.

### <a id="rm-say">"say"</a>
Occurs when a player sends a chat message.

`[0 Integer` Player Id
> The player's identifier.

`[1] String` Text
> The chat message text.

### <a id="rm-say_old">"say_old"</a>
Occurs shortly after join.
Contains information about chat message from before you joined the world.

`[0] String` Username
> The sender's username.

`[1] String` Text
> The text of the chat message.

`[2] Boolean` Is Friend
> Value indicating whether the player is a friend.

`[3] UInt` Chat Color
> The chat color of the sender.

### <a id="rm-show">"show"</a>
Occurs when key deactivates or timed doors change their state.

`[0] String` Key
> The name of the key (or timed door).
> *See [Keys](#model-keys).*

### <a id="rm-smileyGoldBorder">"smileyGoldBorder"</a>
Occurs when someone enables or disables gold smiley border.

`[0] Integer` Player Id
> The player's identifier.

`[1] Boolean` Gold Smiley Border
> Value indicating whether the player is wearing gold smiley border.

___

### <a id="rm-team">"team"</a>
Occurs when someone changes their team.

`[0] Integer` Player Id
> The player's identifier.

`[1] Integer` Team
> The team identifier.
> *See [Teams](#model-teams).*

### <a id="rm-tele">"tele"</a>
Occurs when multiple players are teleported. This event gets raised for respawns of any kind, including death.

`[0] Boolean` Reset
> Value indicating whether the player's properties were reset.

Repeated for each teleported player:

`[...] Integer` Player Id
> The player's identifier.

`[...] Double` X
> The x coordinate of the player's respawn position.

`[...] Double` Y
> The y coordinate of the player's respawn position.

`[...] Integer` Deaths
> The amount of player's deaths.

### <a id="rm-teleport">"teleport"</a>
Occurs when a player is teleported to another location.

`[0] Integer` Player Id
> The player's identifier.

`[1] Integer` X
> The x coordinate of the player's position.

`[2] Integer` Y
> The y coordinate of the player's position.

### <a id="rm-time">"time"</a>
Occurs as a response to the ["time"](#sm-time) send message.

`[0] Double` Data
> The previously sent data.

`[1] Double` Time
> The current server time.

### <a id="rm-toggleGod">"toggleGod"</a>
Occurs when a player received or lost ability to toggle god mode.

`[0] Integer` Player Id
> The player's identifier.

`[1] Boolean` Can Toggle God
> Value indicating whether the player can now toggle god mode.

### <a id="rm-ts">"ts"</a>
Occurs when a sign block is placed in the world.

`[0] UInt` X
> The x coordinate of the block's position.

`[1] UInt` Y
> The y coordinate of the block's position.

`[2] UInt` Block Id
> The block identifier.

`[3] String` Text
> The text.

`[4] UInt` Sign Type
> The type of the sign.

`[5] UInt` Player Id
> The identifier of the player which placed this block.

___

### <a id="rm-unfavorited">"unfavorited"</a>
Occurs when you successfully un-favorite the world.

### <a id="rm-unliked">"unliked"</a>
Occurs when you successfully un-like the world.

### <a id="rm-updatemeta">"updatemeta"</a>
Occurs when world metadata is updated.

`[0] String` Owner Username
> The username of the world owner.

`[1] String` World Name
> The world name.

`[2] Integer` Plays
> The amount of plays.

`[3] Integer` Favorites
> The amount of favorites.

`[4] Integer` Likes
> The amount of likes.

### <a id="rm-upgrade">"upgrade"</a>
Occurs when the server version has increased.

___

### <a id="rm-worldReleased">"worldReleased"</a>
Occurs when crew world has been released.

### <a id="rm-wp">"wp"</a>
Occurs when a world portal is placed in the world.

`[0] UInt` X
> The x coordinate of the block's position.

`[1] UInt` Y
> The y coordinate of the block's position.

`[2] UInt` Block Id
> The block identifier.

`[3] String` Target
> The target of the world portal.

`[4] UInt` Player Id
> The identifier of the player which placed this block.

### <a id="rm-write">"write"</a>
Occurs when a non-player message is received. (System messages, etc.)

`[0] String` Title
> The title of the message.

`[1] String` Text
> The text of the message.

___

# <a id="send-messages">Send messages</a>

### <a id="sm-access">"access"</a>
Sent to attempt to get edit rights by using the edit key.

`[0] String` Edit Key
> The edit key.

### <a id="sm-addToCrew">"addToCrew"</a>
Sent to accept adding of the world to a crew request.

### <a id="sm-admin">"admin"</a>
Sent to toggle administrator mode.

### <a id="sm-aura">"aura"</a>
Sent to change aura shape and/or color.

`[0] Integer` Aura Shape
> The aura shape identifier.

`[1] Integer` Aura Color
> The aura color identifier.

### <a id="sm-autosay">"autosay"</a>
Sent to use auto-say message.

`[0] Integer` Auto-Text
> The auto-text message identifier.
> *See [Auto Text](#model-auto-text).*

___

### <a id="sm-b">"b"</a>
Sent to place a block in the world.

`[0] Integer` Layer
> The layer identifier.

`[1] Integer` X
> The x coordinate of the block's position.

`[2] Integer` Y
> The y coordinate of the block's position.

`[3] Integer` Block Id
> The block identifier.

Additional arguments:

- For sound blocks:

`[4] Integer` Sound Id
> The sound identifier.

- For admin label:

`[4] String` Text
> The text.

`[5] String` Text Color
> The text color.

- For blocks with number value:

`[4] Integer` Number Value
> The number value.

- For portal:

`[4] Integer` Portal Rotation
> The portal rotation.

`[5] Integer` Portal Id
> The portal identifier.

`[6] Integer` Portal Target
> The portal target identifier.

- For world portal:

`[4] String` Target
> The world portal target.

- For signs:

`[4] String` Text
> The text.

`[5] Integer` Sign Type
> The sign type.

___

### <a id="sm-c">"c"</a>
Sent to collect a coin.

`[0] Integer` Gold Coins
> The amount of collected gold coins.

`[1] Integer` Blue Coins
> The amount of collected blue coins.

`[2] UInt` X
> The x coordinate of the coin's position.

`[3] UInt` Y
> The y coordinate of the coin's position.

### <a id="sm-caketouch">"caketouch"</a>
Sent to touch a cake.

`[0] UInt` X
> The x coordinate of the cake's position.

`[1] UInt` Y
> The y coordinate of the cake's position.

### <a id="sm-checkpoint">"checkpoint"</a>
Sent to change checkpoint position.

`[0] UInt` X
> The x coordinate of the checkpoint's position.

`[1] UInt` Y
> The y coordinate of the checkpoint's position.

### <a id="sm-changeBadge">"changeBadge"</a>
Sent to change the badge.

`[0] String` Badge
> The badge identifier.
> *See [Badges](#model-badges).*

### <a id="sm-clear">"clear"</a>
Sent to clear the world.

### <a id="sm-crown">"crown"</a>
Sent to collect the gold crown.

`[0] UInt` X
> The x coordinate of the crown's position.

`[1] UInt` Y
> The y coordinate of the crown's position.

___

### <a id="sm-death">"death"</a>
Sent to die.

### <a id="sm-diamondtouch">"diamondtouch"</a>
Sent to touch a diamond.

`[0] UInt` X
> The x coordinate of the diamond's position.

`[1] UInt` Y
> The y coordinate of the diamond's position.

___

### <a id="sm-effect">"effect"</a>
Sent to activate or deactivate an effect.

`[0] UInt` X
> The x coordinate of the effect's position.

`[1] UInt` Y
> The y coordinate of the effect's position.

`[2] Integer` Effect
> The effect identifier.
> *See [Effects](#model-effects).*

___

### <a id="sm-favorite">"favorite"</a>
Sent to favorite the world.

___

### <a id="sm-god">"god"</a>
Sent to change the god mode state.

`[0] Boolean` God Mode
> Value indicating whether the god mode should be enabled.

___

### <a id="sm-hologramtouch">"hologramtouch"</a>
Sent to touch a hologram.

`[0] UInt` X
> The x coordinate of the hologram's position.

`[1] UInt` Y
> The y coordinate of the hologram's position.

___

### <a id="sm-init">"init"</a>
Sent to request initialization message.

### <a id="sm-init2">"init2"</a>
Sent to request initialization messages such as add, k, etc.

___

### <a id="sm-key">"key"</a>
Sent to change the edit key.

`[0] String` Edit Key
> The edit key.

### <a id="sm-kill">"kill"</a>
Sent to kill the world.

___

### <a id="sm-levelcomplete">"levelcomplete"</a>
Sent to complete the world.

`[0] UInt` X
> The x coordinate of the trophy's position.

`[1] UInt` Y
> The y coordinate of the trophy's position.

### <a id="sm-like">"like"</a>
Sent to like the world.

___

### <a id="sm-m">"m"</a>
Sent to move.

`[0] Double` X
> The x coordinate of the player's position.

`[1] Double` Y
> The y coordinate of the player's position.

`[2] Double` Horizontal Speed
> The horizontal movement speed.

`[3] Double` Vertical Speed
> The vertical movement speed.

`[4] Double` Horizontal Movement
> The horizontal movement modifier.

`[5] Double` Vertical Movement
> The vertical movement modifier.

`[6] Integer` Horizontal Direction
> The horizontal direction indicator.
> `-1` means left, `1` means right and `0` means that player is not moving horizontally.

`[7] Integer` Vertical Direction
> The vertical direction indicator.  
> `-1` means up, `1` means down and `0` means that player is not moving vertically.

`[8] Double` Gravity Multiplier
> The gravity multiplier.

`[9] Boolean` Space Pressed
> Value indicating whether the player holds down space-bar.

`[10] Boolean` Space Just Pressed
> Value indicating whether the player has just pressed down space-bar.

`[11] Integer` Tick Id
> The player's current tick identifier.

### <a id="sm-mod">"mod"</a>
Sent to toggle moderator mode.

___

### <a id="sm-name">"name"</a>
Sent to change the world name.

`[0] String` World Name
> The world name.

___

### <a id="sm-pressKey">"pressKey"</a>
Sent to activate a key.

`[0] Integer` X
> The x coordinate of the key's position.

`[1] Integer` Y
> The y coordinate of the key's position.

`[2] String` Key
> The name of the key.
> *See [Keys](#model-keys).*

### <a id="sm-ps">"ps"</a>
Sent to change the purple switch state.

`[0] UInt` Switch Id
> The switch identifier.

`[1] Integer` Enabled
> Value indicating the state of the switch. 1 = active, 0 = disabled.

___

### <a id="sm-rejectAddToCrew">"rejectAddToCrew"</a>
Sent to reject add to crew request.

### <a id="sm-requestAddToCrew">"requestAddToCrew"</a>
Sent to request adding of the world to a crew.

`[0] String` Crew Id
> The crew identifier.

### <a id="sm-reset">"reset"</a>
Sent to reset progress.

`[0] UInt` X
> The x coordinate of the reset block's position.

`[1] UInt` Y
> The y coordinate of the reset block's position.

___

### <a id="sm-save">"save"</a>
Sent to save the world.

### <a id="sm-say">"say"</a>
Sent to say a chat message.

`[0] String` Text
> The chat message.

### <a id="sm-setAllowSpectating">"setAllowSpectating"</a>
Sent to allow or disallow spectating in the world.

`[0] Boolean` Allowed
> Value indicating whether the spectating should be allowed.

### <a id="sm-setCurseLimit">"setCurseLimit"</a>
Sent to change the curse limit.

`[0] Integer` Curse Limit
> The curse limit.

### <a id="sm-setHideLobby">"setHideLobby"</a>
Sent to change the world visibility in lobby and profile.

`[0] Boolean` Hidden
> Value indicating whether the world should be hidden from the lobby and profile.

### <a id="sm-setLobbyPreviewEnabled">"setLobbyPreviewEnabled"</a>
Sent to enable or disable the lobby preview.

`[0] Boolean` Enabled
> Value indicating whether the lobby preview should be enabled.

### <a id="sm-setMinimapEnabled">"setMinimapEnabled"</a>
Sent to enable or disable the minimap.

`[0] Boolean` Enabled
> Value indicating whether the minimap should be enabled.

### <a id="sm-setRoomDescription">"setRoomDescription"</a>
Sent to change the world description.

`[0] String` Description
> The world description.

### <a id="sm-setRoomVisible">"setRoomVisible"</a>
Sent to change the world accessibility.

`[0] Boolean` Accessible
> Value indicating whether other players are allowed to join the world.

### <a id="sm-setStatus">"setStatus"</a>
Sent to change the crew world status.

`[0] Integer` Crew Status
> The crew world status.
> *See [Crew World Status](#model-crew-status).*

### <a id="sm-setZombieLimit">"setZombieLimit"</a>
Sent to change the zombie limit.

`[0] Integer` Zombie Limit
> The zombie limit.

### <a id="sm-smiley">"smiley"</a>
Sent to change smiley.

`[0] Integer` Smiley
> The smiley identifier.

### <a id="sm-smileyGoldBorder">"smileyGoldBorder"</a>
Sent to enable or disable gold smiley border.

`[0] Boolean` Gold Smiley Border
> Value indicating whether the gold smiley border should be enabled.

___

### <a id="sm-team">"team"</a>
Sent to change team.

`[0] UInt` X
> The x coordinate of the team block's position.

`[1] UInt` Y
> The y coordinate of the team block's position.

### <a id="sm-time">"time"</a>
Sent to request ["time"](#rm-time) message response.

`[0] Double` Data
> The data to be returned.

### <a id="sm-touch">"touch"</a>
Sent to touch other player transferring effects.

`[0] Integer` Player Id
> The touched player's identifier.

`[1] Integer` Effect
> The effect identifier.

___

### <a id="sm-unfavorite">"unfavorite"</a>
Sent to un-favorite the world.

### <a id="sm-unlike">"unlike"</a>
Sent to un-like the world.

___

# <a id="models">Models</a>

### <a id="model-auto-text">Auto Text</a>
```
0   = Left.
1   = Hi.
2   = Goodbye.
3   = Help me!
4   = Thank you.
5   = Follow me.
6   = Stop!
7   = Yes.
8   = No.
9   = Right.
```

### <a id="model-badges">Badges</a>
```
adv = Adventure League
clr = Colorful
end = Endurance
ffs = Fractured Fingers
hlw = Halloween
pp1 = Puzzle Pack 1
rns = Ancient Ruins
tnr = Tunnel Rats
ttr = Tutorials
wtr = Winter
```

### <a id="model-campaign-status">Campaign Status</a>
```
-1  = Locked
0   = Unlocked
1   = Completed
```

### <a id="model-crew-status">Crew World Status</a>
```
0   = Work in Progress
1   = Open
2   = Released
```

### <a id="model-effects">Effects</a>
```
0   = Jump
1   = Fly
2   = Speed
3   = Protection
4   = Curse
5   = Zombie
6   = Team
7   = Low Gravity
8   = Fire
9   = Mutli Jump
```

### <a id="model-keys">Key names</a>
```
red
green
blue
cyan
magenta
yellow
timedoor
```

### <a id="model-teams">Teams</a>
```
0   = None
1   = Red
2   = Blue
3   = Green
4   = Cyan
5   = Magenta
6   = Yellow
```

___

# <a id="shop">Shop Information</a>

### <a id="shop-blocks">Blocks</a>
```
Basic Package  				=
Beta Access					= pro
Brick Blocks				=
Metal Blocks 				=
Grass Blocks 				=
Generic Blocks 				=
Factory Package				= brickfactorypack
Secret Bricks				= bricksecret
Glass bricks 				= brickglass
Minerals					= brickminiral
Christmas 2011 bricks		= brickxmas2011
Gravity Modifying Arrows	=
Key Blocks					=
Gate Blocks 				=
Door Blocks					= 
Coin Blocks					= brickcoindoor
Tool Blocks					= brickcomplete, brickresetpoint
Boost Arrows				= brickboost
Climbable Blocks			= brickmedieval, brickninja, brickjungle, brickjungle, brickcowboy
Purple Switches	(+10)		= brickswitchpurple
Death Doors/Gates (+10)		= brickdeathdoor
Zombie Blocks 				= brickeffectzombie
Team effect (+10)			= brickeffectteam
Timed Doors (+10) 			= bricktimeddoor
Music Blocks				= bricknode, brickdrums
Hazard Blocks				= brickspike, brickfire
Liquid Blocks 				= brickwater, bricklava, brickswamp
Portal Blocks				= brickinvisibleportal, brickportal, brickworldportal
Diamond (+1) 				= brickdiamond
Cake						= brickcake
Hologram					= brickhologram
Christmas 2010 Blocks 		= brickchristmas2010
New Year 2010				= mixednewyear2010
Spring package 2011			= brickspring2011
Your Prices					= brickhwtrophy
Easter  decorations 2012	= brickeaster2012
CandyLand					= brickcandy
Summer package 2011			= bricksummer2011
Halloween pack				= brickhw2011
XMAS  decorations			= brickxmas2011
Sci-Fi Package				= brickscifi
Prison						= brickprison
Colored Windows				=
Pirate Pack					= brickpirate
Stone Pack					= brickstone
Dojo Pack					= brickninja
Wild West Pack				= brickcowboy
Plastic Pack				= brickplastic
Water pack					= brickwater
Sand Pack					= bricksand
Summer pack 2012			= bricksummer2012
Cloud Pack					= brickcloud
Industrial Package			= brickindustrial
Clay Backgrounds			= brickclay
Medieval					= brickmedieval
Pipes						= brickpipe
Outer Space					= brickrocket
Desert Pack					= brickdesert
Fog							= brickfog
Halloween 2012				= brickhw2012
Checker Blocks				=
Jungle						= brickjungle
Christmas 2012				= brickxmas2012
Lava						= bricklava
Swamp 						= brickswamp
Sparta						= bricksparta
Admin Blocks				= "" (Admin Only!)
Signs (+1)					= bricksign
Farm						= brickfarm
Autumn 2014					= brickautumn2014
Christmas 2014				= brickchristmas2014
Basic Background Blocks 	= brickoneway
Valentines 2015				= brickvalentines2015
Magic Blocks				= brickmagic, brickmagic2, brickmagic3, brickmagic4, brickmagic5
Effect Blocks				= brickeffectjump, brickeffectfly, brickeffectspeed, brickeffectlowgravity, brickeffectprotection, brickeffectcurse, brickeffectmultijump
Gold Membership Blocks		= goldmember
Cave Backgrounds			= brickcave
Summer 2015					= bricksummer2015
Environment					= brickenvironment
Domestic					= brickdomestic
Halloween 2015				= brickhalloween2015
Arctic						= brickarctic
New Year 2015				= bricknewyear2015
Ice							= brickice2
Brick Background Blocks		=
Checker Backgrounds			=
Solid Dark Backgrounds		= brickbgdark
Solid backrounds			=
Pretty Pastel Backgrounds	= brickbgpastel
Canvas Backgrounds			= brickbgcanvas
Carnival backgrounds		= brickbgcarnival
Neon Backgrounds			= brickneon
Monster 					= brickmonster

### <a id="shop-blocks">Blocks</a>
```
Artist				= smileyartist
Dark Wizard 		= smileydarkwizard
Light Wizard		= smileylightwizard
Red Ninja		 	= smileyninjared
Purple Ghost 		= smileypurpleghost
Witch 				= smileywitch
Blue Wizard 		= smileywizard
Red Wizard 			= smileywizard2
Bird 				= smileybird
Bunny 				= smileybunni
Fan Boy 			= smileyfanboy
Pumpkin 	 		= smileypumpkin1
Lit Pumpkin			= smileypumpkin2
Superman 			= smileysuper
Grinch				= smileyxmasgrinch
Fan Boy II 			= smileyfanboy2
Big Spender 		= smileybigspender
Bat 				= smileybat
Diver 				= smileydiver
Santa 				= smileysanta
Skeleton 			= smileyskeleton
Archaeologist 		= smileyarchaeologist
Astronaut 			= smileyastronaut
Cat 				= smileycat
Elf 				= smileyelf
Hooded 				= smileyhooded
Dog 				= smileylaika
Nightvision 		= smileynightvision
Ninja				= smileyninja
Postman 			= smileypostman
Summer Girl 		= smileysummergirl
Terminator 			= smileyterminator
Viking 				= smileyviking
Winter Hat 			= smileywinter
Bully 				= smileybully
Clown 				= smileyclown
Commando 			= smileycommando
Gas Mask 			= smileygasmask
Spartan 			= smileyspartan
Caroler 			= smileycaroler
Cowboy 				= smileycowboy
Ghoul 				= smileyghoul
Gingerbread 		= smileygingerbread
Hard Hat			= smileyhardhat
Frankenstein 		= smileyhw2011frankenstein
Ghost				= smileyhw2011ghost
Vampire 			= smileyhw2011vampire
Mad Scientist 		= smileymadscientist
Monster 			= smileymonster
Mummy 				= smileymummy
New Year 2013 		= smileynewyear2012
Nutcracker 			= smileynutcracker
Police 				= smileypolice
Guard 				= smileysoldier
Sombrero 			= smileysombrero
Sunburned 			= smileysunburned
Tanned 				= smileytanned
Templar 			= smileytemplar
Indian 				= smileytg2011indian
Pilgrim				= smileytg2011pilgrim
Tourist 			= smileytourist
Unit				= smileyunit
Kissing				= smileyvalentines2011
Reindeer 			= smileyxmasreindeer
Snowman 			= smileyxmassnowman
Bruce 				= smileyzombieslayer
Earmuffs 			= smileyearmuffs
Alien				= smileyalien
Bishop 				= smileybishop
Chef 				= smileychef
Cow 				= smileycow
Fox 				= smileyfox
Graduate		 	= smileygraduate
Lady				= smileyhelen
Karate 				= smileykarate
Nurse 				= smileynurse
Peasant 			= smileypeasant
Pirate 				= smileypirate
Robber 				= smileyrobber
Robot 				= smileyrobot
Safari 				= smileysafari
Daredevil 			= smileycannon
Fire Demon 			= smileyfiredeamon
Headhunter 			= smileyheadhunter
Princess 			= smileyprincess
3D Glasses 			= smiley3dglasses
Angel 				= smileyangel
Blacksmith 			= smileyblacksmith
Girl 				= smileygirl
Kung Fu Master 		= smileykungfumaster
Propeller Hat 		= smileypropeller
Scarecrow			= smileyscarecrow
Worker 				= smileyworker
Extra Grin 			= smileyxd
Extra Tongue 		= smileyxdp
Coy 				= smileycoy
LOL 				= smileylaughing
Sigh 				= smileysigh
Surprise 			= smileysupprice
Eyeball	 			= smileyeyeball
Penguin 			= smileypenguin
Gold Smiley			= goldmember
Gold Ninja			= goldmember
Gold Robot			= goldmember
Gold Top Hat		= goldmember

### <a id="shop-auracolor">Aura Color</a>
```
Red		= aurared
Blue	= aurablue
Yellow	= aurayellow
Green	= auragreen
Purple	= aurapurple
Orange	= auraorange
Cyan	= auracyan
Pink 	= aurapink
Gold 	= goldmember

### <a id="shop-aurashape">Aura Shapre</a>
```

Default		=
Pinwheel	= aurashapepinwheel
Torus		= aurashapetorus
Ornate		= goldmember











