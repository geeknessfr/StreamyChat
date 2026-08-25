# Changes

One line per change, most recent version on top.

**Every line starts with a bold title.** Reading only the titles must be enough to know what was
added, fixed or changed. What follows a title is optional: one or two lines at most, and nothing
at all when the title says it.

This file is **written for a user**: it says what changes on screen or in use, not how it is
written. Technical detail lives in `docs/PHASE-N.md`, decisions in `ARCHITECTURE.md`.

**English is the source here**, like the interface and the README. The French version is
`CHANGELOG.fr.md`, and the two are written together.

**Anything that belongs to StreamyChat xD goes in its own section**, at the end of each version.
Everyone sees it, including people on the free edition: what a paid edition brings is worth
knowing before deciding whether to try it.

It feeds a panel in the settings window: hence the regular structure: a `## <version> - <date>`
heading, then sections, then short lines.

**One version number = one distributed build** (CLAUDE.md, rule 13). Between two releases,
changes pile up under "Unreleased" and the number does not move.

At release time: the **minor** goes up if the version brings features (that is what a delivered
phase does), the **patch** if it only fixes defects. The major stays at `0` until real use has
proved itself.

---

## Unreleased

### Fixed

- **"Add a language" now opens the folder for you**, and creates it if it is not there. The
  folder does not exist until something makes it, so the instructions sent people to a path
  Windows called missing.

---

## 0.9.0 - 25 August 2026

**StreamyChat speaks English, and your channel says what happens on it.**

⚠️ **Sign in to Twitch again on first launch**: six more permissions, without which your channel
will not report anything.

### Added

- **A nickname menu.** Profile picture, name colour, and how long ago the person last spoke.
  Type `@` and it opens on its own.
- **It filters while you type.** You open it on "ge", you carry on with "ek", the list narrows
  and your text does not move.
- **A nickname is found by its middle too.** "geek" also offers "LeGeeK".
- **Commands that take a nickname open that menu.** `/ban`, `/timeout`, `/warn`, `/vip`, `/mod`
  and the others, the way `/raid` opens the channel one.
- **Your channel says what happens on it.** Channel point redemptions, polls, predictions, hype
  trains, goals and ad breaks land in the chat.
- **Shoutouts show up.** The ones you send, the ones you get, and the ones from other mods.
  Twitch puts none of them in the chat: without this, they existed nowhere.
- **New follows too.** On your channel, and on the ones you moderate.
- **StreamyChat speaks English.** The language is picked under "Advanced"; by default it follows
  your PC.
- **You can add your own language.** Drop a `.po` file into the `lang` folder of your data, then
  restart. An unfinished translation falls back to English.
- **StreamyChat updates itself.** It checks on launch, downloads in the background, and installs
  the next time you restart it.
- **An "About" section**, with your version, the update button and what each version brought.
- **A "Report a bug" button.** It opens the form on GitHub already filled in with your version,
  and drops the report file in a folder next to it, ready to drag in.

### Fixed

- **The emote picker could stay empty for a whole session**, on every tab. The emotes were
  loaded: the screen did not know it.
- **Nicknames with no colour were all white.** They now take one of Twitch's colours, derived
  from the name: the same one from one evening to the next, as on the site.
- **The channel's own emotes went missing every other time** from the "This channel" section.

### Changed

- **Moderation wording uses Twitch's words.** A "timeout", a "ban", a "warn", like the commands,
  which were already called that.
- **The six built-in themes keep their English names.** A theme name travels inside the file you
  export: it stays the same whatever the language. Your current theme is untouched.
- **More text follows the chosen language.** An account's age, the moderation lines, the room
  modes, the connection messages, the sign-in screen.
- **Amounts are written the way your language writes them.** "0,003 $" in French, "$0.003" in
  English.
- **The number of open channels goes from 33 down to 10.** The old figure was wrong: past the
  11th, Twitch stopped reporting raids and nothing said so. Your tabs are all reopened.
- **Global emotes are grouped by provider** (Twitch, 7TV, BTTV, FFZ) instead of one single
  heading.
- **Packaged versions now show as "Beta", not "Alpha".** The app said one thing and the
  download page said another.

### StreamyChat xD

- **Five settings sections instead of six.** "Clean up messages" moved to the bottom of "Voice",
  with its OpenRouter key and its test field.
- **The model and the cleanup prompt are no longer adjustable.** StreamyChat answers for the
  quality of the cleanup, so it sets the details.
- **The spending counters moved to "Advanced"**, next to the bug report.

---

## 0.8.0 - 23 August 2026

**Your tabs move with the mouse.** Grab one and drop it where you want: elsewhere in the bar to
reorder, on another window to send it there, or anywhere outside to give it its own window.

### Added

- **Tabs move with the mouse.** Reorder them, send them from one window to another, or pull one
  out onto the desktop to give it its own window.
- **A "Reset position" button** in Settings → Window. It gives your chat windows their starting
  size back and re-centres them.

### Fixed

- **The close button says what it does.** "Quit StreamyChat" on the main window, "Close this
  window" on the others. Both used to say "Close", when only one of them is final.
- **Closing the main window now really quits.** The app used to stay alive behind your other
  chat windows, with no way to bring the main one back.
- **Chat windows find their channels again after a restart**, when you quit through the main
  window's close button.
- **The window can finally get as small as its text.** At 70% interface size it goes down to
  208 px wide instead of 296.
- **The channel banner no longer opens when you hover the top of the feed.** It only reacts just
  above itself, at tab level.

---

## 0.7.0 - 23 August 2026

**Emote search finds by the middle of a name**, and Tab stops turning your words into images.

### Added

- **Emote search finally finds by the middle of a name.** Typing `:sad` offers `peepoSad` and
  `FeelsBadMan`, where you used to have to know the start.
- **Tab on an ordinary word only completes nicknames now.** It also offered emotes, and turned a
  word of your sentence into an image. For an emote, type `:`.
- **`Ctrl+E` opens the emote picker** while you are in the message field, like Discord.

### Fixed

- **A tab's close button when it slides under the mouse.** Closing a tab slides the next one
  under a cursor that has not moved; its cross only appeared after leaving and coming back.
- **The add-channel menu stayed open for a second and a half** after the click.

### Worth knowing

- **The raid banner has no countdown, and cannot have one.** Twitch only signals a raid as it
  **leaves**: the ninety seconds the site shows live in the video player, on a channel that is
  not public.

### StreamyChat xD

- **Chat messages are cleaned up before they are read out loud.** Abbreviations, missing
  accents, stretched letters. The text becomes speakable without changing what was meant.
- **A test field** in the settings, to hear the difference before turning it on.
- **A "Voice power" slider**, above the volume. Volume only turns the sound down; this one turns
  it up at the source.
- **Two counters say what it all costs**, per session, per day and in total.
- **A message already cleaned up is never paid for twice**, even after a restart.
- **Emoticons are no longer mispronounced.** An `x)` was read out as letters mid-sentence. They
  now become a short pause. `xD` stays: it reads fine.
- **The voice was far too quiet.** It now comes out about **seven times louder**.
- **Every voice comes out at the same level.** Switching voices could divide or multiply the
  volume by twenty without warning.
- **The ignored-nicknames list would not take a new line.** Enter did nothing; you had to paste
  the text.
- **Cleanup is off to begin with**, and needs an OpenRouter key. It costs money per message and
  it rewrites what people typed: that is your call.
- **Around 17 cents per thousand cleaned messages**, before the cache helps.
- **A troll trying to trick the model gets nothing.** Their message is cleaned up like any
  other, or read exactly as they wrote it.
- **If the cleanup fails, the message is read as is.** Nothing stops and nothing shows: your
  stream carries on.

---

## 0.6.0 - 22 August 2026

**Chat can be read out loud.** Everything below is off to begin with.

### StreamyChat xD

- **Chat messages can be read out loud**, by a Fish Audio voice.
- **A button on each message on hover**, and a shortcut you choose, middle click by default.
- **Pick where the sound comes out.** Send the voice to whichever audio output you want.
- **A page to choose your voice**: filter by language, search, and listen before you pick.
- **Automatic reading, optional**, with filters: subscribers, bits, length, ignored nicknames.
- **A bar of its own**: it says what is being read, and lets you skip or cut it all.
- **Emotes are not spoken**, so a message made only of emotes is not read.
- **Messages already read are not paid for twice**: they are kept on your PC for a while.

---

## 0.5.1 - 22 August 2026

**What the live trial of 0.5.0 turned up**: a session you can repair, and messages that speak
plainly.

### Added

- **A bar asks you to sign in again** while permissions are missing, and only goes once it is
  sorted.
- **"Sign out" in the settings**, bottom left, with the connected account above it.
- **Signing out also removes the permission on Twitch's side.**

### Fixed

- **Error messages no longer talk technical**: no more permission names, codes, or English.
- **No more "Timeout" or "Ban" button on your own messages**, which Twitch refuses anyway.
- **`/vip` and `/mod` go out on the channels you moderate**: Twitch decides, not the app.

---

## 0.5.0 - 22 August 2026

**Moderation, end to end**: sanction, lift, set the room, and know who you are dealing with
before you decide.

### Added

- **Ban, timeout, warn, delete a message, clear the chat.**
- **`/ban`, `/timeout`, `/unban`, `/untimeout`, `/warn`, `/delete`, `/clear`.**
- **Durations are written the way you say them**: `/timeout bob 10m`, `1h`, `24h`.
- **Room modes as commands**: `/slow`, `/followers`, `/subscribers`, `/emoteonly`,
  `/uniquechat`, and their opposites.
- **`/vip`, `/unvip`, `/mod`, `/unmod`** on your own channel.
- **Room modes in one click** from the banner: slow, followers, subscribers, emotes, unique.
- **A user card on their nickname**: picture, account age, follow, their messages.
- **An account created under an hour ago is flagged in red**. That is what a throwaway looks
  like.
- **The card offers to timeout, ban, and lift a running sanction.**
- **On hover over a message**: delete, timeout, ban, and a duration menu.
- **Those buttons only appear on channels where you can moderate.**
- **A mistyped command offers the right one** instead of going out into the chat.
- **A role badge StreamyChat does not know yet still shows.**
- ⚠️ **Signing in to Twitch again will be asked for**: three more permissions.

### Fixed

- **The main window keeps its name**, "StreamyChat", instead of taking the active tab's.
- **A deleted message's nickname opens a card**: you can lift the sanction from the fold.

---

## 0.4.2 - 22 August 2026

**Several channels at once, in several windows**, and a merged feed that mixes them all.

### Added

- **One shared Twitch connection**: the ceiling goes from 3 channels to 33.
- **Every window has its own tab bar and its own "+".**
- **A channel moves from one window to another** through the context menu.
- **Closing a window gives its channels back to the main one**, disconnecting nothing.
- **An "All" tab from two channels on**: every message mixed in arrival order.
- **A picture and a colour edge in front of each line** to say which channel it came from.
- **A shared-chat message only appears once** in the merged feed.
- **A channel banner**: stream title, game, viewers, uptime, follow and subscription.
- **The channel's picture replaces the dot** on tabs, faded when offline.

### Fixed

- **The feed no longer scrolls by itself** when you have scrolled up and the buffer is full.
- **A new window opens next to the focused one**, not on the other screen.
- **The right-click menu no longer runs off the window.**
- **A tab tooltip no longer sits on top of the menu.**
- **Click-through pins the window**, and gives its previous pinning back when you turn it off.
- **The emote picker stays stuck to the message field.**
- **Escape on `/raid` or `/shoutout` no longer blocks the channel menu** for the session.
- **Packaged versions show as "Alpha".**

---

## 0.3.2 - 22 August 2026

### Fixed

- **Click-through pins the window on top**, and the setting sits right below it.
- **Escape on `/raid` or `/shoutout` no longer blocks the channel menu** for the session.
- **The emote picker stays stuck to the message field.**

---

## 0.3.1 - 22 August 2026

**The first numbered version.** It gathers everything that existed by then: reading chat,
writing, third-party emotes, looks and transparency.

### Added

- **Sign in to Twitch in three clicks**, with no token to paste.
- **Live chat**: emotes, badges, nickname colours, replies, links, cheermotes.
- **Automatic reconnection after a network drop**, with no duplicates.
- **Channel tabs**, with a picture, the stream title and an unread counter.
- **A channel can be pulled out into its own window.**
- **A sanctioned person's messages fold up**, and open again on click.
- **Unbans and lifted timeouts are announced.**
- **A message field with a draft and a history per channel.**
- **Replies to a message**, on hover or from the keyboard.
- **Completion for nicknames, emotes, commands and channels.**
- **A four-section emote picker**, which remembers the recent ones.
- **`/me`, `/announce`, `/shoutout`, `/raid` and `/unraid`.**
- **A subscribers-only or followers-only room closes the field and says why.**
- **7TV, BetterTTV and FrankerFaceZ**, global and per channel.
- **Overlaid (zero-width) emotes.**
- **Animated emotes can be frozen.**
- **A theme editor**: colours, fonts, density, sizes.
- **Six built-in themes**, and export/import as `.json`.
- **Interface size and text size are adjustable.**
- **Window opacity and background opacity, separately.**
- **Click-through**: clicks pass through the chat to whatever is behind it.
- **A frameless window**, an active-window edge, rounded corners.
