Logic feature suggestions
===============
2020-07-22






As I'm using Logic pro daily now, I'm starting to see little things that can be improved, 
which would make working with logic faster, I believe.


There is a [form to post "feature requests"](https://www.apple.com/feedback/logic-pro.html), but it has a char limitation
which is pretty low, and so I prefer to put my ideas here in a separate file, where I can organize them, edit them, making them clearer for a potential reader.



Here are the ideas you will find in this document:


* [The rectangular tool](#the-rectangular-tool)
* [Automation grid](#automation-grid)
* [Entering automation value manually with an input box](#entering-automation-value-manually-with-an-input-box)
* [Snap automation toggling via cmd modifier](#snap-automation-toggling-via-cmd-modifier)
* [Snap automation mode always visible at the top of the arrange window](#snap-automation-mode-always-visible-at-the-top-of-the-arrange-window)
* [Merge snap automation values and regular snap values altogether](#merge-snap-automation-values-and-regular-snap-values-altogether)
* [The instant capture audio button](#the-instant-capture-audio-button) (if nothing else, this is the best feature to me)
* [The :2 x2 buttons](#the-2-x2-buttons)
* [The search plugin/instrument box](#the-search-plugininstrument-box)
* [Favorite plugins list](#favorite-plugins-list)
* [Arrangement markers: free mode](#arrangement-markers-free-mode)




As I like to say, editing is a constraint, we, logic users, just want to be the most efficient possible at editing, 
so that implementing a musical idea is easy and intuitive, and is not a painful process.
Every second counts.

I believe implementing the ideas below in logic will greatly enhance the editing power of the users.

Cheers.






The rectangular tool
-----------
2020-07-22


So let's say we have this current automation:

![c1](https://lingtalfi.com/img/logicpro-feature-request-screenshots/c1.png)

And what we want is a drop of 40dB at a specific point, which would look like that:

![c2](https://lingtalfi.com/img/logicpro-feature-request-screenshots/c2.png)


Currently, in logic 10.5.1, the fastest way I know of doing this is a workaround that look something like this:

- 1. Creating a marquee tool selection, starting at the specific point, and ending at an arbitrary location
- 2. Then create the cut in the automation, and lower it to -40db
- 3. Then with the pointer tool, select both end points
- 4. Then delete them to obtain the desired result


Something like that:

![c6](https://lingtalfi.com/img/logicpro-feature-request-screenshots/c6.png)


Actually, with the alt behaviour of the pencil tool, we can do the first two steps in one click, but that's still three steps:

- 1. Alt-click with the pencil tool where you want to create the cut
- 2. Then with the pointer tool, select both end points
- 3. Then delete them to obtain the desired result 



So, the idea of the rectangular tool (probably a bad name) is to make this simple operation a "one step" process, as I believe it should be, since
it's such a common thing to do.

The workflow would then be:

- 1. Click where you want to make the cut (and your mouse y's coord at -40dB) with the "rectangular tool"


Basically, it's like the pencil tool in logic, but the connection with sibling points is always horizontal (creating steps if necessary because of the vertical offset with the siblings),
and not a direct straight (and often oblique) line like the pencil tool does.











Automation grid
----------
2020-07-22

Sometimes, it's visually hard to imagine the snap lines in our head, it would be great if we could have some options to show vertical and horizontal lines while in automation mode.



Entering automation value manually with an input box
---------
2020-07-22

Sometimes it's hard to be precise with the mouse, let's say I want to place an automation point at -40dB (for instance), it would be much faster if I could just double-click the point and enter -40 manually, 
rather than fiddling with the mouse, using the control modifier to augment the mouse accuracy and doing up/down mouse moves to try to nail the -40 spot. 

 




Snap automation toggling via cmd modifier
-------------- 
2020-07-22


I believe it would be quite useful, while in the middle of moving automation point, to able to snap to the automation grid or at the contrary to disable the automation snap.
This could be achieved by using the "cmd" modifier (while moving a point) for instance, since other modifiers such as alt are already used for some other things.




Snap automation mode always visible at the top of the arrange window
------------
2020-07-22


Often I wonder which automation snap mode I'm in.
While I can know at a glance which general snap mode I'm in, because it's just at the top of the arrange window, I miss the same information for the snap automation mode.

So, having the option to show the snap automation mode menu at the top of the "arrange window" would kill two birds with one stone:

- make it faster to know which mode we are on
- faster access to the snap values if we want to change them via the mouse




Merge snap automation values and regular snap values altogether
----------
2020-07-22


I've never seen myself consciously wanting a snap automation value that's different from the snap value.

I understand that other users might find this useful, but for me it's two decisions to make where only one was necessary.

Therefore, I suggest that we should have the option (in the preferences) to decide whether those two types of snap values are linked or not.







The instant capture audio button
-----------
2020-07-22 -> 2020-07-28


That's my number one feature, that would totally be awesome if implemented.

When doing "sound design", a terribly useful skill is to be able to say: "hey, I liked how this reverb tail sounded", and then grab that reverb tail, and merge it with other sounds, etc...

Currently, in logic 10.4.5, the only way (afaik) to capture exactly what we hear, which is basically what goes out of the "Stereo Out" channel, takes too long:

- create a bus
- route the signal(s) that we want to that bus (this can become cumbersome very fast, especially when the sound we want has its own routing system, then we need to make sure that routing is preserved to get that same sound we want to capture)
- then from an audio track, set the input of that audio track to the prepared bus
- record


It would be awesome if we could just be on any track, and press a button which would record the output of "stereo out" and put it into a wave file directly.
 
I believe ableton has that kind of feature.

In logic, we could for instance have an option to show that "instant audio capture" button, next to the record button for instance.


Again, I can't stress enough how this would change sound design possibilities in logic, as sometimes going through process of setting up the routing, in logic 10.5.1, which can take minute or even more sometimes,
can be a blocker in itself. If we had that button, ideas would pop a lot more, and no frustration.








The :2 x2 buttons
------------
2020-07-22


I saw that in ableton (again): basically in the piano roll, they have those handy ":2" and "x2" buttons, which divide the speed by half of the selected midi notes (or double their speed).

This is handy, and I believe logic users should have the option to display them. They would be at the top of the piano roll.

Currently, in logic 10.5.1, to achieve that, we have to open the midi transform dialog first, which is already nested in some menus, and then only reopen the menu to select the operation type, and then again
click another time to validate the operation, this is way too much time spent for such a simple/common operation. 
  




The search plugin/instrument box
--------
2020-07-22


This one I saw in cubase (for a change).
Basically the idea is to have an autocomplete box to search for plugins.

Often, I know exactly which plugin I want to insert on my channel strip, for instance the h-delay from Waves.
Still, it will invariably take me about 6 seconds just to insert it, because I have to open the plugin nested menu, scroll down to "Audio Units", then go to "Waves", being careful to not move my mouse out of the menu,
and then from the Waves gigantic list of plugins, scroll down to "h", where is "h", after "g" but before "i", ..., and then finally find the "h-delay" plugin. 

And that's when I know that Waves is the company behind the plugin, if I know the plugin name, but don't remember the vendor name, then I need to remember the vendor name first.

My point is that an autocomplete box at the top of the first menu would be much faster for me.


Favorite plugins list
---------
2020-07-22


At the top of the plugins list, I see that logic keeps the last 5 or 6 plugins I recently used.

While this helps sometimes, because I tend to use more than 5 or 6 plugins I find that this list is too short.

I would prefer to have a list of arbitrary length, which contains whichever plugin I tag as "my favorite".

I could have 2 or 50 favorites, that list should display all those favorites, and only those.

I know that in my case, that would be much more helpful than the list of recently used plugins.

 

Arrangement markers: free mode
----------------
2020-07-22 -> 2020-07-28


The **arrangement markers** in logic are a great tool to quickly edit vertical sections of your project.


The problem with the current arrangement markers is that it has only two operation modes:
 
- the default "swap" mode, where you can swap **arrangement markers** with their siblings
- suspend content connection mode, where basically **arrangement markers** are just markers/labels


I believe a third mode would be very useful: the free mode.


With the free mode, the **arrangement markers** can be placed anywhere: they don't have to be contiguous anymore.
This allows the user to do is have more power when editing the arrangement.

While the "swap" mode is great once you have all your song parts ready, I personally spend most of my time building the song parts, and often, I encounter the need to quickly/temporarily
move a section to the right, to make space to insert a new musical idea for instance.

Moving a whole section to the right is a very common action in my workflow, and currently in logic the time it takes to select a vertical section takes too long.

My current options are:

- either use the marquee tool ruler, but the problem with that is that I need to be very precise when dragging over the ruler, and then once I moved the selection, 
    I cannot recall that selection for later
- or I can use the **arrangement markers**, I can simply create an empty **arrangement marker** to the right of the **arrangement marker** I want to move, then extend it to make the space I need,
    and then either duplicate my **arrangement marker** to the right of that pivot/empty **arrangement marker**, or swap it.
    

I prefer the first one, but the problem is that I need to redo the marquee drag every time I want to move the section again (i.e. it's not stored in memory).


Hence, the need for the "free" mode, where **arrangement makers** can be not only moved anywhere, but also created from anywhere, just like midi regions.

This "free" mode would really make the **arrangement markers** useful and powerful.


Currently, I don't use the arrangement at all (maybe 0.5% of the time) because they can't be moved freely, and so from my perspective they aren't usable (I just don't use the feature).
However, I always need to move vertical sections around (about 99.5% of the time), that's how useful "free" mode in **arrangement markers** would be for me.

I see the potential in **arrangement markers**, I really hope this feature is implemented, as it would probably multiply by 10 the editing power of most logic users.




 
 
 

Log
===========


- 1.0.2: 2020-07-28: moved "Better arrangement track" to "Arrangement markers: free mode"
- 1.0.1: 2020-07-28: moved "Pattern copy track instead of arrangement track" to "Better arrangement track"
- 1.0.0: 2020-07-22: initial commit