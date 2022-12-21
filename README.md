# SAMMI Stream Deck Buttons
Just what it says on the tin. this is a collection of buttons and automations for [SAMMI](https://github.com/SAMMISolutions/SAMMI-Official/releases). Most buttons are geared towards Twitch specifically, though some buttons can be adapted to YouTube via SAMMI's trigger system. Several others are buttons that are activated manually.

## Importing Buttons and Decks into SAMMI
**All buttons are in JSON and exported / imported directly from / into SAMMI as plain text files.**
To import a button:
1.) Copy the raw text from one of the "Button" files above.
2.) Open a deck in SAMMI Core, then right click on an open space in the deck (must have available space for the button itself).
3.) Select "Import from JSON".

To import a deck:
1.) Copy the raw text from one of the "Deck" files above.
2.) In SAMMI Core, click on the "+" button.
3.) Select "Paste Deck".

## Example Deck
A deck including a handful of buttons that are more or less ready to go. This includes Twitch commands (via the Twitch API and those handled via SAMMI), various effects, follower alerts, and automations. 

## Twitch Buttons (API / SAMMI)
[Due to a change to how Twitch will handle slash commands via IRC starting in February 2023](https://discuss.dev.twitch.tv/t/deprecation-of-chat-commands-through-irc/40486), commands that previously used a slash (like /emoteonly) will need to use Twitch's API to ensure they continue to work past that date. While SAMMI has covered most API implimentations via built-in commands (such as the **Twitch: Send Announcement** command), I've included API versions in case they're needed.

## Follower / Subscriber Alerts
While these examples were built with Twitch in mind and in turn use Twitch commands and triggers, they can be converted to YouTube alerts by changing the trigger type in SAMMI. You can also use them as inspiration for other types of alerts - just because they're described as follower alerts doesn't mean you have to use them that way! Alerts and other notifications are fun ways to kit out your stream regardless of what platform you stream to.

These largely require that you provide your own Scene and Source in OBS, and are meant more to be a jumping-off point rather than an "out of the box" solution.
