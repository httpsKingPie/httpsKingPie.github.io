# Welcome to TDL2

Truly Dynamic Lighting 2 (or TDL2) is the more advanced iteration and successor to my original module, Truly Dynamic Lighting (or TDL).  This version aims to be more lightweight , more customizable, and easier to use than the original TDL, all while retaining the same original features.

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
- [Day/Night Script Auto Sync & Auto Calculated Tween Starts](https://github.com/httpsKingPie/httpsKingPie.github.io/blob/master/README.md#daynight-script-auto-sync-and-auto-calculated-tween-starts)
- [Utilizes a Scalable Class Based Approach](https://github.com/httpsKingPie/httpsKingPie.github.io/blob/master/README.md#utilizes-a-scalable-class-based-approach)
- [Integration with Weather Scripts](https://github.com/httpsKingPie/httpsKingPie.github.io/blob/master/README.md#integration-with-weather-scripts)

and many more...

Check out [Full Feature List](https://github.com/httpsKingPie/httpsKingPie.github.io/blob/master/README.md#full-feature-list) for a full list

You can use the [editor on GitHub](https://github.com/httpsKingPie/httpsKingPie.github.io/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

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

As was mentioned before, TDL2 uses a scalable design to allow for the easy addition of any new lighting properties or classes.  TDL2 is also fully compatible with *classes not explicitly included in the settings*, meaning that if there is a class that you want to affect (ex: Sparkles) you can simply add it to the TDL2 settings page like any other class and the script will work.  Some properties that are not able to be adjusted by code (ex: LightingTechnology) or values that are difficult to include as automated changes (ex: ColorSequences) may result in errors, but the door is open for you to take the module where you want.  Ultimately, this acts as a tool for you to use how you wish.

### Day/Night Script Auto Sync and Auto Calculated Tween Starts

TDL2, like TDL, features a system that auto-calculates how fast time moves in your game (i.e. the speed of your Day/Night cycle) and will automatically adjust your Lighting Periods such that the completion of the settings changes and tweens corresponds exactly to the beginnings of your lighting period.  This is a setting that can now be disabled, too.

### Smart Set Up for Setting Management

Settings now feature a much more readable format internally that makes editing them much simpler.  Settings are also created by placing ModuleScripts into either the LightingSettings or WeatherSettings folders.  Furthermore, you can freely add Folders within those folders to organize your settings for your own benefit.  Here's an example:

![Example](https://i.vgy.me/16KOzO.png)

### Integration with Weather Scripts

### Performance Improvements

### Easy Use

### Simple API

## Settings Overivew


Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

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
