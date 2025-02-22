---
title: "I'm Using Tilt Controls! And You Should Too."
categories: 
    - games
---

# What is Gyro Control 

"Tilt controls" or "gyro controls" are a motion input method that promises [mouse-like precision without aim assist](https://www.youtube.com/watch?v=krQ_ggZcN1Q) while using a controller. It does this by using very small movements of the controller as input, almost always as an alternative to aiming with the right analog stick. While these are motion controls, the motion being detected is extremely small, rather than Wii sports style full body motion. Having a controller-based alternative that can work for any game is great for me, because I've found that I never want to play games at my desk using the mouse and keyboard when I've already been sitting at my desk using mouse and keyboard all day.

Also, it's fun and intuitive. People already jerk their controller around while playing games, why not make that an input? The best part is, if you own a modern controller, you can (probably) try it without buying anything.

# How Do I Use Gyro Control?

Using Gyro controls requires two things. First, any controller with a gyro sensor. Switch Pro controllers, Dualshock 4s, and DualSense controllers all have gyro, many third party controllers like 8BitDo Pro models do too. Notably, Xbox controllers do not.

Next, you need *some kind* of gyro controller support. Modern consoles (not the Xbox) have pretty good gyro support. Counterstrike 2, Fortnite, and Apex Legends, all support gyro. If you play primarily on a console, the rest of the post won't be relevant to you, stop reading and just go try it out. 

Unfortunately, native gyro support mostly sucks. Games will support one modern controller, like the DualSense, and completely break with another, like the Switch Pro. Even when it doesn't suck, the implementation of gyro support isn't standardized. Availability of customization options is extremely inconsistent. Some games only support one type of camera movement, some don't have flick stick (we'll get to this later). None of this matters because by using Steam Input, we can make any that game supports mouse and keyboard support gyro. Non-Steam games can be added to your Steam library, allowing you to use Steam Input. Outside of Steam you can use [JoyShockMapper](https://github.com/Electronicks/JoyShockMapper) (free, more work) or [reWASD](https://www.rewasd.com/releases/release-5.3.0), which is a subscription service, but supposedly the most convenient and feature complete.

# Hybrid Gamepad + Gyro vs Using Mouse and Keyboard Binds

There is a hybrid approach where the game still behaves like you have a gamepad oustide of letting you use gyro aim. At time of writing, this doesn't work well for me. I get weird little bugs, gyro doesn't work, the game gets very confused about whether you're using gamepad or mouse, instability. This is especially bad if the gamepad implementation was a bit half baked, which it often is in older games. So I just map everything in the controller to the equivalent default keyboard mapping for the game. The downside of just emulating mouse and keyboard is you lose button glyphs, so you'll see "hit E" instead of "press A". I don't care about this, some people do.

## An Example

In Helldivers 2, gyro did not work when Steam Input was off. With Steam Input on, the native support fought Steam Input's configs and weird buggy behavior was constant. Mostly this meant my character staring into the sun while being eaten by bugs / turned into a picnic table by chainsaw-wielding robots while I fumbled with configs. So I instead mapped everything on the controller to mouse and keyboard inputs and it worked perfectly. By convincing the game you're just using the default mouse and keyboard, you get the best supported control scheme and you can reuse your tuned personal gyro settings across games without having to petition the devs for better support and / or feature parity with whatever your favorite implementation of gyro is. Mouse and keyboard provides us with a perfect interface already, why bother with native support?

I hear some people are good at making hybrid setups work, so I think it might be worth trying the couple most popular Steam Community layouts. I may update this later, but I haven't tried a hybrid layout yet that "just worked".

# I Don't Have a Controller, Which One Should I Buy?

I would caution against buying a third party controller unless you want to do *even more* config finagling than you normally have to with gyro. With an unusual controller, you might not get recommended layouts for Steam, your OS might not read gyro inputs correctly, etc. If you're on Linux, you might have to deal with 💀 Linux driver issues 💀. Stick with first party hardware. If you're crazy you could spend $200 on a DualSense Edge. If you have an old DualShock 4 lying around, that could work too. Outside of those, your options are the DualSense and the Switch Pro.

Reddit generally likes the DualSense. [Youtuber "Nerrell" found that the Switch Pro was a little more accurate](https://youtu.be/CenJLOTGxLc?si=jUzV9cW4qZuQj_7o&t=946), I've seen a couple other people compare the modern options and find that the Switch Pro is a *little* better. I own a Switch, so I bought the Pro, and let me tell you, it does not have enough buttons. The DualSense has the whole pad there to map gesture controls, and I get the impression it generally gets better support. The Pro controller has no inputs beyond what you would expect from a 360 controller. That being said, Steam Input gives us the ability to deal with the lack of buttons. Creating mode switches (or layers? or I think they made a third thing?) in order to access more binds is good enough. Steam also lets you do things like map clicking a button once to one key, twice to another, and holding the button to a third, which is pretty useful for making one button deal with, for example, diving for cover (single tap), going prone (double tap), and crouch (hold).

Anyway, I bought the controller from Pink Gorilla, a local shop that I'm always surprised is still chugging along, so I don't want to return it.

If you want a little more convenience and some more features, buy a DualSense. If you want marginally more accuracy, get a Switch Pro Controller. If you already own a Switch (which is more likely than owning a PS5 if you consider their sales figures, [etc](https://www.youtube.com/watch?v=UtG11pmBe3U)), you might as well get the controller compatible with it.

# Configuration

You could just settle for native support or Steam Community suggested layouts (if any are present for your game), but you'll probably have to configure some stuff yourself. There are a [lot](https://www.reddit.com/r/GyroGaming/comments/198wq0y/new_to_gyro_gaming_start_here_gyro_beginners_guide/) of [guides](https://www.youtube.com/watch?v=D0uSfda_-Rc) out there that go into great detail, so I'm going to trust those to be better up-to-date comprehensive sources. Here I'm just going to hit a couple very common changes you might make, or situations you might find yourself in.

## Flick Stick

This is probably the most important setting. Once you've freed up your right stick, you can use it to make very large movements (like fully turning around) instantly rather than having to whip the controller around.

## Gyro Ratcheting

Ratcheting refers to the ability to disable the gyro briefly so you can move the controller back to a neutral position without moving the game's camera. I often map this to my mode switch button.

For some reason, in Steam Input you don't set a gyro disable button,you set a gyro enable button (even if gyro is always on) and set the behavior of the enable button to be disabling the gyro. Intuitive! [Credit](https://www.reddit.com/r/GyroGaming/comments/ug54tk/comment/i6xgli4/?utm_source=share&utm_medium=web3x&utm_name=web3xcss&utm_term=1&utm_content=share_button)

## Sensitivity

You're probably going to start with the sensitivity too low while you're getting used to it. This is fine. Eventually you'll probably get tired of making big movements and turn it up.

## 3D to 2D

For some reason Steam Input defaults to just using "Yaw", reading input from how the controller is turned or tipped. You probably also want to use "Roll", which reads how the controller is "twisted" as well. If it makes sense to you that you should be able to turn the controller so the top faces left when you want to turn left, use "Roll" as well. Try out the settings, reading about them is very abstract, when you actually try the different options you will immediately understand how they work, and if you're anything like me, one setting will seem obviously right and the rest obviously wrong. If you want to read about it anyway, [here you go](http://gyrowiki.jibbsmart.com/blog:player-space-gyro-and-alternatives-explained).

# Tangent About TF2
[This video](https://youtu.be/PJIqEX93vL8?si=sOfHWUPpjs1eLp4c) prompted me to look into gyro controls, naturally I tried to make them work in TF2 first. The config shown in the video is available and extremely popular, but it didn't work for me immediately. The inventory would open and then instantly close as if it was getting two inputs. Disabling the gamepad in settings seemed to did nothing, console commands either did nothing or broke it further, what worked was finding the Xbox 360 controller config text file and commenting everything out (deleting the contents would also work). 

For anyone else running into this, the file lives at:

`SteamLibrary\steamapps\common\TeamFortress2\tf\cfg\360controller.cfg`

So, if you want to play old, exceptionally buggy games with half-baked features in a way that they were never meant to be played, you may have to do this sort of thing.

# In Conclusion,

If this guide convinced you to try Gyro controls, send me a message on Github telling me how long you spent futzing with configurations and I'll chuckle knowingly while shaking my head.