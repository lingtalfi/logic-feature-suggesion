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
* [The instance capture audio button](#the-instance-capture-audio-button)
* [The :2 x2 buttons](#the-2-x2-buttons)
* [The search plugin/instrument box](#the-search-plugininstrument-box)
* [Favorite plugins list](#favorite-plugins-list)
* [Pattern copy track instead of arrangement track](#pattern-copy-track-instead-of-arrangement-track)




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







The instance capture audio button
-----------
2020-07-22


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

 

Pattern copy track instead of arrangement track
----------------
2020-07-22


Although I believe logic is much more powerful than fruity loop, while watching a techno tutorial, the guest tutor, 
which was using fruity loop, was using this nice little feature of fruity loop where he could just copy paste any pattern
he had created before, thus making arranging a song a breeze.

Made me think that this would be actually more efficient than the current "Arrangement track" that we have in logic,
which is not very easy to manipulate when it comes to duplicating a section.


So below is what I suggest should be a better alternative to the "arrangement track" in logic.


At the top of the arrange window, just above the marker track for instance, we should have a "Pattern" track.
There will be no "plus" button next to the label "Pattern". Instead, we can create pattern regions exactly as we create midi regions, 
the only difference is that they have their own dedicated track at the top (when you open the global controls, shortcut=g).

The benefit of this is that instead of clicking a plus button to add a section, we can create and POSITION the REGION WHERE WE WANT, so, more flexible than the arrangement sections.
Once a region is created, whenever moved, everything under is moved along with, and again with the options of keep/split/shorten, or maybe with a default of "keep" mode.

So the workflow then becomes this: I'm creating my techno song, I have 58 tracks,  and there is this section that I like, I want to duplicate it.

With logic 10.5.1, I would have to use the the marquee ruler with copy/paste which is great, but the marquee ruler is very thin and therefore hard to operate, plus I have to drag, which makes it awkard,
depending on my snap value I might not select the thing I want in the first time, and also, it's just copied in the buffer and I cannot re-use my copy for later.

Well in the new logic, I could simply create a "pattern" region, and extend it at my own pace (no loosing mouse drag pressure), and then when satisfied with the region length, I can alt+click it to duplicate it
(and all the content above will follow). 

Plus, I can name it, for instance "cool vibe". And then later if I need that cool vibe again, it's already there, no more marquee ruler, and no need (at least for me) for an arrangement track.


Also, I believe that deleting the pattern region/container shouldn't (by default) delete the attached content.
In other words, I would like to have the possibility to use those regions/container as a tool to move rapidly a delimited section of the arrangement, that's all.

Maybe the behaviour could even be that when we move that region/container, it doesn't move the content below it, unless we use the alt modifier? Just a quick idea I just had.

But the goal is nothing but being to move whole parts of the arrangement rapidly, and as a bonus in a re-usable manner.










 



 







