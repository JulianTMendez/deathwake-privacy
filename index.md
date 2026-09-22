---
title: Deadwake Privacy Policy
---

# Deadwake — Privacy Policy

**Last updated:** 22 September 2026
**Applies to:** the Deadwake Android application (`com.monkforge.zombies`)

Deadwake is a free, independent zombie-survival game. This policy explains
exactly what the app does and does not do with information about you.

**In short:** the app has no accounts of its own, ads, analytics, or in-app
purchases. Your progress stays on your device unless you are signed in to Google
Play Games, which can keep a backup copy, your achievements and your scores in
your Play Games profile. Online play shares your network address with
other players and our matchmaking broker. Optional online leaderboards are off
by default; if you turn posting on, your match result and player name are sent
to our leaderboard service and the score is displayed publicly.

---

## 1. What stays on your device

The following is stored in the app's own private storage directory:

- **Game progress** — rank, level, prestige, XP, challenge completion, camo
  unlocks, badges, per-map best rounds, and total playtime. Match results are
  sent only if you switch on leaderboard posting. Stored locally as plain
  files (`profile_progression_a.dat` / `_b.dat`).
- **Settings** — graphics, audio, controls, touch layout, language, and key
  bindings (`user_settings.cfg` and the app's shared preferences).
- **Your player name**, as you type it in the menu. It is sent to other players
  during online play and with a match result if you opt in to leaderboard posting.
- **Imported custom maps**, if you use the map import feature.

The app sets `allowBackup="false"`, so none of this is copied to Google Drive by
Android backup. Uninstalling the app deletes all of it. The only copy that can
leave the device is the Google Play Games backup described in section 4.

The game has no account system of its own. We never ask for an email address or
a phone number. The only sign-in is Google Play Games, which is optional and
handled entirely by Google.

---

## 2. Online play

Solo play is entirely offline. If you host or join an online game:

- **Your IP address is shared with the other players in that game.** Deadwake
  connects players directly to each other (peer-to-peer). This is unavoidable
  for direct connections and is how nearly all peer-to-peer games work.
- **Your local network address is also shared** with the other players in the
  game, so that two people on the same Wi-Fi can connect to each other
  directly. Only players in your game receive it.
- **Our matchmaking broker** briefly receives your IP address, your game code,
  your player-visible server name, the current map, and the number of players,
  so that the people you invite can find you. It holds this only while your game
  is running and forgets it when you disconnect. The **matchmaking broker**
  never stores this information to disk and carries no game traffic. The
  separate leaderboard service is described below.
- **Your player name and progression rank** are visible to everyone in your
  game, and to anyone browsing the public server list if you choose to make your
  game public. Games are **private by default**.

**Online traffic is not encrypted.** Deadwake uses plain peer-to-peer
networking, so anyone able to observe your network could see chat messages and
player names in transit. Do not share anything sensitive in game chat. A lobby
password, if you set one, controls who may join — it does not encrypt anything.

The game engine does not log IP addresses to a file. (The underlying engine can
do this, but the feature is off by default and the app never turns it on.) The
separate leaderboard service stores a hash of request IP addresses as described
below.

---

## 3. Online leaderboards (optional, off by default)

You can always view the public boards. Posting is **off by default**. You can
switch it on or off in the Leaderboards section of Progression. When it is on,
the app sends a result when a match ends: your sanitized in-game name, internal
map name, highest round, kills, player count, match length, and build identifier.
It sends no device ID, advertising ID, or location. A random one-use request
code and tamper-evidence signature are also sent to protect the service from
casual replay. Scores are public and kept indefinitely unless removed.

Like any web server, the leaderboard service sees the request IP address. It
uses the address in memory to limit request rates and retains a **hash** of it
with the submission log for 30 days. The service stores the name and match
result. Names on a blocklist are displayed as `PLAYER` while their scores stay
on the board. There are **no accounts, so a name is not an identity**: two
players using the same name share one leaderboard row.

Leaderboard traffic uses plain HTTP and is **unencrypted**. Anyone able to
observe the connection may see the submitted information or public scores.
Do not use a sensitive name. To request removal of a leaderboard row or ask for
a copy of the data associated with a name, use the address in the Contact
section. Because there are no accounts, we cannot prove ownership of a name
from the name alone; we will review removal requests case by case.

---

## 4. Google Play Games (optional)

If your device has Google Play Games and you are signed in to it, Deadwake
uses it automatically; you can also sign in from the Achievements or
Leaderboards section of Progression. The game plays exactly the same without it.

When you are signed in, Google provides the game with your **Play Games player
name**, which the game shows in the menu and, if you never chose a name of your
own, uses as your in-game name. The game sends Google:

- **Achievements** you have earned, worked out from your local progress.
- **Scores** for the Play Games leaderboards: your best round on each stock map,
  your lifetime kills, and your lifetime XP. Scores are shown to other players
  according to your Play Games visibility settings.
- **A backup of your progress file** (`profile_progression_a.dat` / `_b.dat`,
  described in section 1), saved to Play Games Saved Games so your progress can
  be restored after reinstalling or on another device.

This data goes to Google, not to us: we do not receive your Google account,
email address, player ID, or backup, and none of it is sent to our leaderboard
service. Google handles it under the
[Google Privacy Policy](https://policies.google.com/privacy). You can sign out,
change who sees your Play Games profile, or delete your Play Games data for
Deadwake (including the backup) in the Google Play Games app.

---

## 5. Permissions

| Permission | Why |
| --- | --- |
| `INTERNET` | Online play, optional online leaderboards, and Google Play Games. |
| `ACCESS_WIFI_STATE`, `CHANGE_WIFI_MULTICAST_STATE` | Makes a game you host on your Wi-Fi visible to players on the same network. |
| `WAKE_LOCK` | Keeps Wi-Fi responsive while you are *hosting* a game, so the players connected to you do not see latency spikes. Only held while you host. It does not keep the game running in the background: if you leave the app while hosting, the game pauses for everyone until you come back. |
| `VIBRATE` | Haptic feedback. Can be turned off in Accessibility settings. |

The app requests **no** location permission, **no** camera or microphone access,
**no** contacts access, and **no** broad storage permission. Custom map import
uses the Android document picker, which grants access to the single file you
choose and nothing else.

---

## 6. Children

Deadwake depicts combat against zombies and is not directed at children. We do
not knowingly collect information from children under 13 (or the equivalent age
in your country). The optional leaderboard feature may hold the data described
above if posting is enabled.

---

## 7. Your rights

Uninstalling the app removes local progress and settings. Data held by Google
Play Games is managed in the Google Play Games app (see section 4). You can turn
off future leaderboard posts at any time. To request a copy or deletion of a public
score or related submission log, contact us using the address below and provide
the in-game name and map. We will handle applicable data protection requests.
We cannot identify an individual from a name alone, so we may need more detail
to find the correct record. The matchmaking broker keeps its temporary data
only in memory while your game is running.

---

## 8. Changes

If this policy changes materially, the updated version will be published at the
same URL with a new "last updated" date, and a new app release will accompany
any change to what the app collects.

---

## 9. Contact

juliantmendez2004@gmail.com

---

## 10. Attribution

Deadwake is an unofficial adaptation of *Nazi Zombies: Portable* and is not
endorsed by the NZ:P team, Activision, Treyarch, or the FTEQW project.
Licensing and source-code availability notices are included with the app.
