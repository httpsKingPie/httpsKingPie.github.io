# Welcome to TDL2

Truly Dynamic Lighting 2 (or TDL2) is the more advanced iteration and successor to my original module, Truly Dynamic Lighting (or TDL).  This version aims to be more lightweight , more customizable, and easier to use than the original TDL, all while retaining the same original features.

Here's an example of what this looks like visually (with some example Lighting Periods)
![Example of Lighting Features](https://i.gyazo.com/8e7d60361fb68c108a7670c00a351e17.png)

## How do I use TDL2?
TDL2 takes a different approach than the original TDL.  It comes in more of a package setting.  You can always download the most up to date version directly from the github as a .rbmx model.  Alternatively, you can check out it's toolbox page (ADD TOOLBOX PAGE HERE).

_Once in Game_

1. I recommend putting the TDL2 folder in ReplicatedStorage.  This way, you have the freedom to change it from server sided to client sided at the touch of a button.
2. Adjust the Settings module.  There should be a brief documentation within the script, but a more detailed overview can be found [here](https://github.com/httpsKingPie/httpsKingPie.github.io/blob/master/README.md#settings-overview)
3. Make a copy of the FullSettingsExample, and paste it into either LightingSettings or WeatherSettings, depending on what you are trying to adjust.
4. Adjust the settings for the LightingSettings and WeatherSettings.  Feel free to remove any settings that you do not plan to change.  The settings page can be as big or small as you like.  Make sure your lighting periods are continuous!
5. Add a Day/Night cycle in.  It doesn't matter what kind, since the script is able to auto sync the times for your lighting periods with the day/night cycle so that it activates at the correct point.
6. Require the module from a server sided script, and execute the .Run function
7. Enjoy!  Let me know if you have any questions!
(I've done my best to add useful warnings to prevent script errors and alert you for any typos, etc. with that being said, make sure to check spelling/syntax)

## Highlights

- [Server Sided or Client Sided Options](https://github.com/httpsKingPie/httpsKingPie.github.io/blob/master/README.md#server-sided-or-client-sided-options)
- [Turn on/off lights](https://github.com/httpsKingPie/httpsKingPie.github.io/blob/master/README.md#turn-onoff-lights)
- [Control and Modify the Properties of Complex Instances](https://github.com/httpsKingPie/httpsKingPie.github.io/blob/master/README.md#more-advanced-complex-instance-aka-multi-instance-capability)
- [Day/Night Script Auto Sync & Auto Calculated Tween Starts](https://github.com/httpsKingPie/httpsKingPie.github.io/blob/master/README.md#daynight-script-auto-sync-and-auto-calculated-tween-starts)
- [Utilizes a Scalable Class Based Approach](https://github.com/httpsKingPie/httpsKingPie.github.io/blob/master/README.md#utilizes-a-scalable-class-based-approach)
- [Integration with Weather Scripts](https://github.com/httpsKingPie/httpsKingPie.github.io/blob/master/README.md#integration-with-weather-scripts)

and many more...

Check out [Full Feature List](https://github.com/httpsKingPie/httpsKingPie.github.io/blob/master/README.md#full-feature-list) for a full list

## Full Feature List

### Server Sided or Client Sided Options

Lighting can be tricky, especially if your game uses more advanced features that change lighting based on region, certain actions, etc.  With that being said, TDL2 offers the ability to change lighting, based on lighting periods or weather, on either the client or server.  This can be done, simply by changing a setting - no other work is required and a lot of headache can be saved on your end.  

### Turn On/Off Lights

One of the great things about immersive environemnts is that they replicate what actually exists in the real world.  An effect that I love to see in-game is lights turning on in buildings.  TLD2 allows you to do that.  Turn on lights, change their colors, change the colors of parts, adjust particle emitters, etc. etc.  TLD2 gives you the freedom to adjust different classes and create the changes to make your lighting period perfect.

### Compataible with all Lighting Settings and Lighting Children Settings

TLD2 is compatible with all properties of the Lighting service (except ClockTime and TimeOfDay since these are used to determining lighting periods and will be automatically filtered out) and lighting classes such as Atmosphere, BloomEffect, BlurEffect, and ColorCorrectionEffect.  TLD2 also uses a scalable design to allow for the easy addition of any new lighting properties or classes with requiring an overhaul or update to the general script.  Everything is ready to go and built for the future.

### More Advanced Complex Instance (aka Multi-Instance) Capability

One cool feature of TDL was its ability to control complex instances (previously known as multi-instances).  If you're confused on what I mean, imagine a lantern model.  The lantern model might have an actual part, that looks yellow and has a neon material, as well as a particle emitter for effects, and a point light for lighting.  TDL2 and TDL allow for control of the complex instance so that you can control multiple instances within the same fundamental model with ease.  TDL2 expands upon complex instances and allows you to specify a single reference part and affect siblings, children, desecendants, and the reference part's parent with ease.

### Utilizes a Scalable Class Based Approach

As was mentioned before, TDL2 uses a scalable design to allow for the easy addition of any new lighting properties or classes.  This makes it both very easy to edit, but also fully compatible with *classes not explicitly included in the settings*, meaning that if there is a class that you want to affect (ex: Sparkles) you can simply add it to the TDL2 settings page like any other class and the script will work.  Some properties that are not able to be adjusted by code (ex: LightingTechnology) or values that are difficult to include as automated changes (ex: ColorSequences) may result in errors, but the door is open for you to take the module where you want.  Ultimately, this acts as a tool for you to use how you wish.

### Day/Night Script Auto Sync and Auto Calculated Tween Starts

TDL2, like TDL, features a system that auto-calculates how fast time moves in your game (i.e. the speed of your Day/Night cycle) and will automatically adjust your Lighting Periods such that the completion of the settings changes and tweens corresponds exactly to the beginnings of your lighting period.  This is a setting that can now be disabled, too.

If you're confused about why this is necesary, take a look at this graphic.  

![Example of issue](https://i.gyazo.com/265de5b46b7d54e2ba45542d4032e12a.png)

*The black lines are the ranges of each lighting period and when we want those settings to be applied.  The red lines are approximately where those settings are going to be applied if the tween starts at the beginning of the lighting period.  This can result in Lighting Periods behaving as the developer does not intend*

Auto Sync solves this issue and ensures that Lighting Periods exist during the ranges that you specify.

### Smart Set Up for Setting Management

Settings now feature a much more readable format internally that makes editing them much simpler.  Settings are also created by placing ModuleScripts into either the LightingSettings or WeatherSettings folders.  Furthermore, you can freely add Folders within those folders to organize your settings for your own benefit.  Here's an example:

![Example](https://i.vgy.me/16KOzO.png)

### Integration with Weather Scripts

I mentioned immersion before, and one of the best ways to employ weather is to use it in combination with awesome lighting settings.  TDL2 carries on the ability of TDL in allowing for smooth transitions to weather lighting.  This can be done, very simple, using the below function:

```lua
module.TweenWeather(WeatherName)
```

This is also the same command used in TDL, so conversion between the two should be seamless.

### Performance Improvements

If you compare the source code between TDL and TDL2, you will see a completely different shift in mentality.  TDL2 was built to be powerful and very lightweight.  Increased controls are also given to the user in Settings that can lead to performance enhancements as well, depending on the structure of your game.

### Easy Use

TDL2 is designed to be usable and understandable by all.  Setup is very quick and the entire module can be run in one line, that being:

```lua
module.Run()
```

### Simple API

TDL2 has a very simple API, that most people won't ever have to use.  As mentioned above, the entire system can be run in one line.  The API is to give developers more freedom to make manual changes if necesary.

## Settings Overivew

This is a brief overview of the various settings.

### Settings (the Main Settings module that is a sibling of Main)

**AdjustmentTime**

This is the value that determines the amount of time allocated to the script to detect how fast time passes in your day/night script, i.e. the amount of time the script has to figure out Auto Sync.  From my own experience, I've found that 5 yields the best results per time allocated, so I recommend keeping that as the default.  With that being said, if you would like to shorten or extend this, feel free.

**AlwaysCheckInstances** 

This determines whether the script should run a search through workspace to check for instance changes every time the lighting settings change or whether it should only happen once.  In other words, setting this to false will mean that the script will check to see if it has already performed a search for the instances you are trying to change, and if it has, it will cache that result.  Setting to true will mean that it will search each time, regardless of a cached result.

**AutomaticTransitions**

Setting this to true means that TDL2 will perform checks and update the lighting automatically as your time changes.  Setting this to false means that you will have to do this manually.  This isn't difficult to do manually, see the API section.

**ChangingInstanceChildrenOfWorkspace**

Long setting name, very short explanation.  Basically if all the instances (excluding those that are naturally children of Lighting) that you expect to change are children, rather than descendants, or Workspace, set this to true.  If you have instances that are descendants, rather than children, set this to false.  This yields a small performance increase for those who have instances that are simply children of Workspace.  

**CheckTime**

This is the time that the script has between its checks where it determines whether a new lighting period has been entered.  The reason the script works this way, as opposed to an event, is because many day/night scripts would fire the event multiple times a second.  Given that most lighting period changes don't need to be accurate to the thousandeth of a ClockTime, implementing independent CheckTimes boasts a massive performance increase.  It is recommended to keep CheckTime to around 1 - 3, but feel free to adjust it to your liking.  In general though, day/night scripts that move faster should have smaller CheckTimes, while day/night scripts that move slower can get away with larger CheckTimes.

**ClientSided**

This determines whether the script is run on the server or the client.  Lighting can be tricky when both the server and client are modifying the same instances, so this gives a solution for the client to take total ownership over the lighting.  Setting this to true, is also not the same thing as running the module from the client, as checks are performed on the server, to ensure all players have the same experience, and then replicated to the clients.  This is default set to false, as this is useful for games that meet the criteria above.  Many games will never encounter the issues that would make client sided TDL2 attractive.

**EnableSorting**

Sorting is a method that improves the performance of the system by having the script only check to see when the next adjacent lighting period begins.  The drawbacks are that you *can not* make changes to the ClockTime variable that are drastic, ex: when ClockTime is 12, do not randomly change it to 23 if doing so would move the game into a lighting period that is not immediately following the current lighting period.  If you only have a few lighting periods in game, you can get away with doing this while EnableSorting is set to true.  However, if you are planning on making sudden changes to the ClockTime in game (not including day/night scripts) I would not recommend using EnableSorting.  Setting to false will make it so that TDL2 checks to see what lighting period it is, regardless of sequential or adjacent position.  I.e. if you make a sudden change to ClockTime, TDL2 will follow you and start adjusting lighting settings appropriately.

**Tween**

Set it to true if you like nice tweens.  Set it to false if you want hard changes.

**TweenInformation**

Adjust the tween information if you set Tween to true.  I recommend keeping the EasingStyle as Linear in all cases.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Internal Settings

*Do not adjust Internal Settings unless you are planning on modifying TDL2 for your own purposes.  Modification without proper changes can break the script entirely or result in unexpected behavior*

## LightingSetings/WeatherSettings/FullSettingsExample

*GeneralSettings*

**StartTime** (for LightingSettings only)

This is the time your lighting period starts.  Put times in using 24 hour notation (ex: 4 in the afternoon = 16).

**EndTime** (for LightingSettings only)

This is the time your lighting period ends.  Put times in using 24 hour notation (ex: 4 in the afternoon = 16).

*Important Note: Make your lighting periods continous.  If you have four lighting periods, make them look like (0-6, 6-12, 12-18, 18-0).  Don't do (0-1, 6-7, 12-13, 18-19)*

**LightsOn** (for LightingSettings only)

This one is sort of tough to explain, so I'll describe how the script uses this value and why it's useful for immersion.  

Imagine a town where TDL2 is used to make things look realistic.  If randomization is used (covered in the ChanceOfChange setting/property below), 75% of the lights turn on when it gets dark (picture early evenign) to simulate buildings having some lights on due to the darkness.  Now, if another lighting period is called, say there's a midnight lighting period, it wouldn't make sense to make changes to the lights again, they are already on.  Same goes for if the weather changes causing the lighting to get vastly darker, unless you specifically intended to, it wouldn't make sense to change the lights *again*.

Not making sense?  Here's a more Studio relevant example.  I have a lantern model.  When the time hits nighttime and we enter my nighttime lighting period, I want the light to have a 75% chance of turning on.  Assuming it turns on, the PointLight instance within my lantern is active.  Now imagine, I actually have 200 lantern models that are affected by this, and approximately 75% (150 lanterns) of them are "on".  Now, when I hit my midnight lighting period, it might make sense to still tell the TDL2 that I want my lanterns on, particularly if you're using the unsorted setting.  Now if I turn on all my lanterns again, with 75% randomization, that means that actually approximately 188 of the 200 lanterns will be on (since the ones that are on are already on, and the remaining ones that are off with have a 75% chance of turning on again).  Ugh, now lighting periods are not behaving how I want them to, because 94% of lanterns on is not 75%.  This problem would not occur if TDL2 respected the fact that the lanterns were already on, and decided not to make any changes, which is what setting LightsOn as true does.

**AdjustOnlyLightsOn**

This one is also tough to explain, so forgive me for taking you on a rollercoaster.  Read the description for the LightsOn setting (ctrl + f if you need to), and then come back to here.  Sorry.

So continuing my exmaple, lanterns.  Of my approximately 150 lanterns that are on, I might want to make a change such as reducing the size of the light in the lanterns, to simulate the light dying down.  By setting AdjustOnlyLightsOn to true, any changes with the lighting period will only affect lights that have been toggled as on, based on the LightsOn property.  

So basically this property makes TDL2 respect lights as "already being on".  
### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/httpsKingPie/httpsKingPie.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
