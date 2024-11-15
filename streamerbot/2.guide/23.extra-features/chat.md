---
title: Streamer.bot Chat
description: Built-in chat with deep Streamer.bot integration
logo: https://streamer.bot/logo-transparent.svg
---

Streamer.bot ships with a built-in chat client to provide you with direct integration between chat and your bot's actions.

## Features

### Multi Stream Support
By default, the chat window will enable a tabbed view for all broadcaster accounts you have connected.

While on the combined chat view, you can toggle which chat(s) to send to:

![Preview](assets/chat-toggle.png){.rounded-md .shadow-xl}

#### Shortcuts
Keyboard shortcuts exist to easily direct your chat messages to/from different accounts:
| Keybind | Action |
|--------:| ------ |
| :shortcut{value="Enter"} | Send to **selected** chat(s) |
| :shortcut{value="Shift+Enter"} | Send to **all** chats |
| :shortcut{value="Ctrl+Enter"} | Send to **selected** chat(s) with the **bot account** |
| :shortcut{value="Ctrl+Shift+Enter"} | Send to **all** chats with the **bot account** |

![Preview](assets/chat-multi-youtube.png){class="rounded-md shadow-xl" width="500"}

### Command Menus
Autocomplete menus exist for the following options:

| Keybind | Menu |
|--------:| ---- |
| `/`     | Slash Commands |
| `:`     | Emote Autocomplete |
| `!`     | Streamer.bot [Commands](/guide/commands) |

#### Slash Commands
::note
You can open the slash command menu with :shortcut{value="/"}
::

Slash commands contain a set of actions that are directly integrated with your Streamer.bot instance.

For example, you can type `/action` to reveal a menu with all actions in your Streamer.bot instance to directly execute.

Some commands support **Multi-Platform** execution, such as `/title` which can set the title of both Twitch and YouTube broadcasts simultaneously.

![Preview](assets/chat-slash-commands.png){class="rounded-md shadow-xl" width="500"}


#### Streamer.bot Commands
::note
You can open the command menu with the :shortcut{value="!"} prefix
::

For commands to appear in the command menu they must be configured with:
- Set `Location` to `Start`
- Start with the `!` prefix

::warning
Commands must have the`Ignore Internal Messages` option **disabled** to work in the chat window.
<br>
This setting forces those commands to ignore internal chat input, including from the built-in chat.
::

When selecting a command, :shortcut{value=Enter} will submit the command immediately to chat.

If you wish to add input for a command, use :shortcut{value=Tab} to select the command and continue typing.

![Preview](assets/chat-commands.png){class="rounded-md shadow-xl" width="500"}

#### Emote Autocomplete
::note
You can open the emote menu with :shortcut{value=":"}
::

Emote autocomplete can be triggered at any time and contains emotes from the following sources:

- Twitch
- YouTube
- 7TV (Twitch & YouTube)
- FFZ (Twitch)
- BTTV (Twitch & YouTube)

To select an emote and continue typing, you can use either :shortcut{value="Enter / Tab"}

![Preview](assets/chat-emotes.png){class="rounded-md shadow-xl" width="500"}

### Quick Actions
In settings, you can configure **Quick Actions** for 3 different sources.

Quick Actions allow you to immediately execute any of your Streamer.bot actions with custom arguments.

#### Global
Global Quick Actions are displayed in the bottom-left of the chat window and can be executed at any time.

![Preview](assets/chat-quick-actions-global.png)

#### User
User Quick Actions are displayed in the `View User` popup windows that display when you click on a username in chat.

Additional arguments are populated with the usual user args for the respective platform.

![Preview](assets/chat-quick-actions-user.png)

#### Message
Per-message quick actions appear when you hover over a specific chat message.

Additional arguments are populated with the usual message args for the respective platform.

![Preview](assets/chat-quick-actions-message.png)

### Highlights
Message and event highlights can be customized for a variety of events.

::collapsible{name="configuration options preview"}
![Preview](assets/chat-highlights.png)
::

::collapsible{name="message highlighting preview"}
![Preview](assets/chat-highlights-preview.png)
::

## OBS Browser Dock

You can dock the internal chat in `read-only` mode by enabling the Streamer.bot WebSocket Server and adding the following URLs as Custom Browser Docks in OBS:

| Name | URL |
| ---- | --- |
| Streamer.bot Chat | `https://chat.streamer.bot/feed/chat` |
| Streamer.bot Event Feed | `https://chat.streamer.bot/feed/events` |

::tip
The ability to **send messages** from the external web chat is coming in Streamer.bot v0.2.5, currently available in public beta
::