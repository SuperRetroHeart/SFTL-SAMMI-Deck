# Superfuture Technolabs SAMMI Decks and Buttons
This is a collection of buttons and automations for [SAMMI](https://github.com/SAMMISolutions/SAMMI-Official/releases), arranged into a single deck and named (loosely) after the theming of my livestreams. Most buttons are geared towards Twitch specifically, though many of them can be adapted to work with YouTube via adjusting the triggers in SAMMI. Several others are buttons that are activated manually, or are for automation.

NOTE: A *lot* has changed since I started putting together the initial deck, including how API calls are handled (nearly all of them are now handled via SAMMI commands rather than HTTP requests) and various updates to SAMMI itself, which means a lot of this is outdated. I don't want to take it all down in case someone finds use for what I have so far, so I'm going to rework and update things as I go along. The decks and buttons outlined below still work just fine, but there are typically better ways to handle what they do at this point.

## Importing the Deck into SAMMI
To import a deck:

1.) Copy the raw text from the "SFTLDeck.txt" file above.

2.) In SAMMI Core, click on the "+" button.

3.) Select "Paste Deck".

## The Example Deck
A deck including a handful of buttons that are mostly ready to go. This includes Twitch commands (via the Twitch API and SAMMI commands), various effects, follower alerts, and automations. Instructions and additional details are included in each button, and buttons can be copied from the Example Deck to any other deck in SAMMI. This lets you pick and choose what buttons you want to incoprorate into your own setup, or just pull inspiration from to make your own.

### Twitch Buttons (API / SAMMI)
[Due to a change to how Twitch will handle slash commands via IRC starting in February 2023](https://discuss.dev.twitch.tv/t/deprecation-of-chat-commands-through-irc/40486), commands that previously used a slash (like /emoteonly) will need to use Twitch's API to ensure they continue to work past that date. While SAMMI has covered most API implimentations via built-in commands (such as the **Twitch: Send Announcement** command), I've included API versions in case they're needed, and because sometimes API calls offer more flexibility than the built-in SAMMI commands.

### Alerts
While these examples were built with Twitch in mind and in turn use Twitch commands and triggers, they can be converted to YouTube alerts by changing the trigger type in SAMMI. Alerts and other notifications are fun ways to kit out your stream regardless of what platform you stream to. Keep in mind that these are primarily meant to be inspiration for you to make your own alerts, not "out of the box" solutions. You can drop your own sources in to get a feel for how they work, but things will likely not look great until you've gone in and adjusted things yourself. It's to help you see how the cookies are made, not the cookies themselves, basically, though... if you're looking at this for alerts, hopefully that's why you're here, yeah?
Now, did I ever tell you about how I started making my own alerts because all the info I could find in SAMMI about displaying a random image was about twerking Thanos GIFs? wait come back where are you going

### Automations
Just what it says on the tin. *The triggers are ON by default* as an example of how they work.
I recommend setting the triggers for these based on your needs; "out of the box" the triggers are set for when you start and end streams in OBS, but those triggers can be deleted or you can disable the entire board until you're ready to go (triggers also copy when you copy a button, so keep that in mind).

### The Kitchen Sink
Various stuff that doesn't fit anywhere else, like making a sound board, having a random image pop up, buttons that can keep track of an increasing value, and the like. All of these run locally via SAMMI and OBS, and are not tied to any specific platform (unless otherwise stated). These are more jumping off points to make your own effects, since you'll still need to point them to the sound effects, images, etc. you want to display.

### Button Variables
There's a single button that will set variables for various buttons when SAMMI starts up via a trigger so that the buttons work correctly the first time you press them. I'd recommend not touching it unless you're sure of what you're doing.
Buttons can have an initial variable set by right clicking on them and going to "Edit Init Variables", but I find it easier to manage them all in one button that functions as a container, rather than on a per-button basis. (That's something I wish I had known - and done - early on. You do you though.)

## Extra Notes
### "Bot" accounts and "Join chat under this name" in SAMMI
Most of the Twitch API buttons include mention of a "bot" account. There are a couple of different ways bots can work on Twitch; in SAMMI's case, this can be an actual bot using a separate that you've programmed to "live" on your channel, or a separate account that you've previously set up and connected to SAMMI that you're sending instructons to. I **strongly recommend** that you run API commands via your own account unless you already have an account set up for this purpose.

The SAMMI buttons, in turn, will send messages and announcements based on which account is set as "Join chat under this name" in Twitch Connections, selectable at the bottom of the SAMMI Core window. These should be fine for the majority of folks who need automations That Just Work without too much fuss.

## Examples
### Announcement
![SAMMI_Twitch_Announcement](https://user-images.githubusercontent.com/112423124/209442719-0e3ae688-194f-48e4-af90-03e32fc7ba51.png)

### Dynamic Subscriber Alert
![SubscriptionCombo-768x602](https://user-images.githubusercontent.com/112423124/209442757-f0a9e03a-7ec1-4225-bd4f-13d4dfb7226d.png)


### Basic Follow Alerts
**Fade**

https://user-images.githubusercontent.com/112423124/209442687-02a10d73-92dd-4b6f-872c-fb200397de2f.mp4

**Motion**

https://user-images.githubusercontent.com/112423124/209442699-55039c3b-4046-4ac6-a54a-3d1635b73caf.mp4

### Advanced Follow Alert

https://user-images.githubusercontent.com/112423124/209442865-11d4081b-dc3d-4a03-876a-faaae8fc7332.mp4

