Logic feature suggestions
===============
2020-07-22 -> 2020-08-23






As I'm using Logic pro daily now, I'm starting to see little things that can be improved, 
which would make working with logic faster, I believe.


There is a [form to post "feature requests"](https://www.apple.com/feedback/logic-pro.html), but it has a char limitation
which is pretty low, and so I prefer to put my ideas here in a separate file, where I can organize them, edit them, making them clearer for a potential reader.



Here are the ideas you will find in this document:




- General 
    - [The instant capture audio button](#the-instant-capture-audio-button) (if nothing else, this is the best feature to me)
    - [Loop icon should be available to the left side of the regions too](#loop-icon-should-be-available-to-the-left-side-of-the-regions-too)
- Piano roll    
    - [The :2 x2 buttons](#the-2-x2-buttons)
    - [Select every other note](#select-every-other-note)
- Channel strip
    - [Favorite plugins list](#favorite-plugins-list)
    - [The search plugin/instrument box](#the-search-plugininstrument-box)
- Arrangement window
    - [Arrangement markers: free mode](#arrangement-markers-free-mode)
    - [Select vertical slice by region](#select-vertical-slice-by-region)
    - [Snap automation mode always visible at the top of the arrange window](#snap-automation-mode-always-visible-at-the-top-of-the-arrange-window)
    - [Snap automation toggling via cmd modifier](#snap-automation-toggling-via-cmd-modifier)
- Audio region
    - [Extend audio region length like midi region](#extend-audio-region-length-like-midi-region)
    - [Slice at transient markers should be first class citizen](#slice-at-transient-markers-should-be-first-class-citizen)
- Automation
    - [The rectangular tool](#the-rectangular-tool)
    - [Rectangular selection in automation mode](#rectangular-selection-in-automation-mode)
    - [Merge snap automation values and regular snap values altogether](#merge-snap-automation-values-and-regular-snap-values-altogether)
    - [Entering automation value manually with an input box](#entering-automation-value-manually-with-an-input-box)
    - [Automation grid](#automation-grid)
    - [Automation shape tools](#automation-shape-tools)
    - [Pointer tool and automation](#pointer-tool-and-automation)
    - [Duplicate automation should snap to grid](#duplicate-automation-should-snap-to-grid)
- Drum machine designer
    - [duplicate dmd cells](#duplicate-dmd-cells)
- Mixer
    - [Being able to arrange the order of channel strips](#being-able-to-arrange-the-order-of-channel-strips)
    - [Creating mixing groups](#creating-mixing-groups)



And some bugs I found:


- [Drum machine designer bugs](#drum-machine-designer-bugs)


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




Rectangular selection in automation mode
--------------
2020-07-28


So let's say I have this saw-like automation:

![rectangular-selection-automation-mode](https://lingtalfi.com/img/logicpro-feature-request-screenshots/rectangular-selection-automation-mode.png)


Now I want to select only the top four points, to make them higher.


It's hard in the current version of logic, because both the pointer tool, and the marquee tool both select a vertical slice, so with those two tools, I can't just
draw a quick rectangle and get away with it; instead I need to shift-select them one by one.
 
In the above example I only had four points, but what if I have 100+ points, are you allowing that there is no tool in logic to select those points, apart from shift-clicking them?

(well if that's the case that's terrible, it should be fixed)


The intuitive way to select those top four points would be to simply draw a rectangular selection around them, and that's what the **pointer** tool should be able to do (since logic should feel intuitive, right?).  

At least in automation mode, where precise editing becomes critical.






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
2020-07-22 -> 2020-07-29


I've never seen myself consciously wanting a snap automation value that's different from the snap value.

I understand that other users might find this useful, but for me it's two decisions to make where only one was necessary.

Therefore, I suggest that we should have the option (in the preferences) to decide whether those two types of snap values are linked or not.


Another reason why this might be a good idea is that it's hard in logic to find keyboard shortcuts that aren't used, because there are so many of them.
So it was hard, but I managed to set my shortcuts for switching the snap value between bar, beat and division (since I switch constantly between them), and also shortcuts for switching
between snap to absolute/relative value, since I also use them a all the time. But now if I had to set new shortcuts for the automation snap value,
first of all it would eat even more shortcuts (which is expensive since there are so few left), and then it would be harder to remember all those shortcuts.

So merging the snap automation values with the snap values would really be beneficial for my case.  







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


However, I see the potential in them: as I always need to move vertical sections around (about 99.5% of the time), that's how useful "free" mode in **arrangement markers** would be for me.

I really hope this feature is implemented, as it would probably multiply by 10 the editing power of most logic users.

And if you do implement this, please remove the popup that occurs when you swap **arrangement markers**, which ask: 

![arrangement-marker-popup](https://lingtalfi.com/img/logicpro-feature-request-screenshots/arrangement-marker-popup2.png)


This is a waste of time, as this is a very common action to move vertical sections.

Instead, the user should have the option to set it once for all in the preferences, something like:
- ask always
- ask never


 
 
Select vertical slice by region
------------
2020-07-28


When the user right clicks a midi/audio region, in the Select submenu, we should have an item that says:

- select vertical slice with the selected region length 


Well, this label has too many chars, but you get the idea: the user should be able to select a whole vertical section rapidly.

Currently, to do so, I use the marquee ruler, but I sometimes struggle to nail the marquee selection with the mouse.

If we had an option in the select menu, I would use it all the time to avoid the mouse selection struggle.


To put it differently, if we look in the shortcuts, we currently have these options:

- Cut Section Between Locators
- Copy Section Between Locators
- Repeat Section Between Locators


Well, I just miss this one:

- Select Section Between Locators

because I just want to move it.

"Cut Section Between Locators" is very close, but the content disappears, and then I need to place the playhead, 
whereas for this particular case when all the regions are selected, I prefer to drag them where I want.






Extend audio region length like midi region
-------------
2020-08-05


One of the feature I like in logic is the ability to drag the top right corner of a midi region to make it loop.
Very convenient.

Before we can loop a midi region though, we sometimes need to resize the midi region.
It's easy to do so, just drag the bottom right or bottom left of the midi region to extend it to where you want.

Once it has the desired length (often a perfect bar), then drag-loop it, cool.

I wish the workflow with audio regions would be exactly the same, unfortunately it's not in logic 10.5.1.

Instead, when an audio region is short, because the sample it contains is short, we can't easily extend the region's length
to our likings.
That sucks, because then we cannot easily loop it.

I would love to be able to just drag the bottom corner of an audio region to extend it, just as a midi region behaves.
And of course, the extended space where there is no concrete audio content should be fill with silence.

Simple idea, but yet to organize the patterns in a song, it makes it much more consistent, intuitive, and therefore 
efficient to work with.








Automation shape tools
-----------
2020-08-05


So let's say I want to create a sine form automation pattern.

Of course you could say, why not use a midiFX Modulator, but the problem with that approach is that we cannot do exceptions:
for instance what if I want to have a sine wave shape for the first 3 beats, but then a custom shape for the 4th beat.

So having the automation written down, you have the full control over the sound, so I prefer the automation approach.


So to create a sine wave form, here is a quick try with current logic 10.5.1: I start with making the automation line appear:

![automation-shape-tool-a](https://lingtalfi.com/img/logicpro-feature-request-screenshots/automation-shape-tool-a.png)


Then I will draw a basic saw tooth form:

![automation-shape-tool-b](https://lingtalfi.com/img/logicpro-feature-request-screenshots/automation-shape-tool-b.png)


Then with the automation curve tool, I try to bend the lines to make it look like a sine wave:

![automation-shape-tool-c](https://lingtalfi.com/img/logicpro-feature-request-screenshots/automation-shape-tool-c.png)


We can see how hard it is for a human to make a perfect sine wave, and even if it probably doesn't matter too much, 
my sine wave is far from perfect in the above example.

Therefore, it leads me to this suggestion: we should have automation shape tools for the basic shapes.

We already have lines and we create dots anywhere, and we can bend the lines, that's cool.

But it would be even better if we had:

- a step shape (see my [rectangular tool idea](the-rectangular-tool))
- a sine wave shape
- a saw tooth wave shape
- a square wave shape

The idea with the three latter shapes is that with the mouse you drag a horizontal line, and the tool automatically contains an arbitrary number of shapes.

Like in adobe illustrator when you create a spiral, while we are holding the mouse (dragging the horizontal line), we can increase/decrease the number of shape repetitions
by tapping the up and down arrow keys. Note that those shortcuts only work while you are dragging with the mouse.

The height and lenght of the overall pattern is defined by the imaginary rectangle selection made by the mouse (where the height of that rectangle is the amplitude
of the shape, and the length is the total length of the container containing the x repetitions of that shape). 
 
 
 
Then I also believe a flatterner tool would be welcome, as an alternative to the eraser.

- flattener tool

With the flattener tool, when we start dragging, anything inside the dragged zone (left and right boundaries of the imaginary rectangle selection made by the mouse) is at level 0.

This means that probably at the left and right boundaries, a straight vertical cut is made (i.e. points are created if necessary)

This flattener tool would help inserting custom shapes in the middle of other shapes, such as the shapes described above


 


Pointer tool and automation
-----------
2020-08-06


When working in automation mode in the arrangement window, I find the current pointer tool a little clumsy to work with.

Because the rules that defines its behaviour seem a little illogical, hence not very intuitive.

For instance, with the pointer tool, if I click shortly on a line, it creates a new point on the line, but if click and hold (more than
let's say 100ms) on the line, then it just selects the segment. That's not consistent.

Then to remove a point, I need to double-click, and double-clicking feels always clumsy, especially for precision work like that.

Therefore I suggest the following:

- the pointer tool by default should only be used to select things (it doesn't create or remove point)
- the double-click behaviour of the pointer tool might be removed (although some users might like it)
- the pencil tool shall be used rather to create points
- with the pointer tool and the alt modifier, we can create points anywhere (i.e. on the line or not on the line, like the pencil tool)
- with the pointer tool and the alt modifier, if the point we are about to create will be on the line, the user should be aware of it (maybe a color change of the line, or of the cursor, to indicate that the point will be added on the line)
- with the pointer tool and the alt modifier, the vertical line should appear, to help positioning the automation point
- with the pointer tool and the alt modifier, and the shift modifier, the vertical line should snap to the current snap automation value
- with the pointer tool and the alt modifier, and the shift modifier, the up/down arrow keys should set the snap automation value to the prev/next value in the snap automation list (which by the way should be visible at the top of the arrangement window)

So to sum up, I believe that having the alt modifier to make creation of points via the pointer tool will ultimately feel less clumsy than the double-clicking behaviour, 
and more consistent, as it will be harder to create an automation point by accident with that behaviour.
 

 


Duplicate automation should snap to grid
------------
2020-08-08


When in automation mode in the arrangement window, I've created an automation pattern that I would like to duplicate and
snap to a certain beat in my region (this automation pattern needs to be applied at a very specific moment in time).

So I select my pattern with the selection tool, and alt click to duplicate, then drag the mouse to move the duplicated pattern
where I want. Unfortunately, the pattern doesn't seem to snap to any snap grid defined. So this is imprecise, and clumsy, as I can never
have the precision I want with a free mouse drag. 

So I suggest that the when duplicating an automation pattern with the alt modifier and the mouse, the pattern should snap to the defined snap value.


Note: a workaround I found around this is to set my snap value to bar, then marquee select the whole automation pattern, and cmd+R (repeat) it,
that's fine, but still I believe that the duplicate via alt-click should stick to the current snap value (because I don't see why not).
 
 



Slice at transient markers should be first class citizen
-----------
2020-08-08


When doing sound design, a very useful feature to have it to be able to slice an audio region into slices, each slice starting at a transient marker.

Fortunately, logic 10.5.1 has this feature available, but unfortunately, it's quite deep: you have to turn on flex, then make your track flex, then only do you have the 
contextual menu that gives the "Slice at transient markers" option.

In sound design, it's always good to be very efficient at doing things, as the mind is in a "creative mode" and doesn't need to be distracted with unnecessary mouse clicks and gui design problems.

That's why I suggest that this handy feature should be available for every audio region, regardless of whether flex is active.

Of course, under the hood, logic would still use the "flex engine" with default values (which is generally good enough), but that would be transparent to the user,
and so with that feature the user can slice instantly his audio regions, and keep his workflow, keeping the focus on sound design.





Duplicate dmd cells
-----------
2020-08-11


I'm following this tutorial where the tutor in ableton just duplicates the cells of the drum rack (which is the equivalent
of drum machine designer but in ableton).

The reason he does that is to create quick envelope variations on the copies, thus giving him more nuances for a given sample.

That's a pretty good reason to be able to duplicate cells, as it's musically useful.

Unfortunately in logic 10.5.1, when I alt-click a cell with the intent of duplicating it to another (empty) one, it does not duplicate the cell.


I suggest that alt-click should allow us to duplicate dmd cells, rather than having to go back to the finder and reload that same sample from there (which takes much longer).





Being able to arrange the order of channel strips
------------
2020-08-12

 
As we add tracks on a song, it's important to keep things organized.
One way to do this is assigning colors to tracks.

Another is bus grouping (re-assigning the output of some tracks to a bus, thus grouping them).

Since logic already has this color feature, it makes no sense to me that logic doesn't let the user re-arrange
the channel strip order.

Since we are able to create those bus groups, we should be able to place them where we want in the mixer.
I personally like my groups to be on the right, but in an order I decide.
For instance, sometimes I like to create a "premaster" bus, which basically takes the input of all my tracks.
Then later if I decide to group my drums into a "drum bus", logic will put it on the right of my "premaster" bus, which doesn't make sense, visually.

Same reason why the "Stereo Out" channel strip is always on the far right, I want my "premaster" bus to be on the far right, on the very left of the "Stereo Out",
but logic 10.5.1 won't let me do that. Instead, it will put my lastly created bus on the right of all the bus I created, as if I could predict the future (which I can't obviously).

So this is a real pain and limitation to not even have the ability to re-arrange the strip channels order.

Logic is not flexible in that regard, and therefore I suggest this feature, where we can simply drag (with the mouse) channel strip
wherever we want, in the mixer window only (it shouldn't impact the environment view at all).


Note: I believe this one has been a thorn in the side of Logic for a long time, and should be fixed asap.  


 
Loop icon should be available to the left side of the regions too
-----------------
2020-08-12


It's very convenient to have this loop icon on the right of the regions to make a loop quickly.
However, sometimes I find myself needing to extend the loop to the left of the region rather than to the right, 
but logic doesn't allow that yet, so I need to drag the region to the left, and then re-cut the loop where I want it to end (since moving the region
to the left will generally move the end point with it).

It would be faster to just be able to extend the loop to the left side, so that's my feature suggestion. 




Creating mixing groups
-------------
2020-08-15


I've just seen this feature in fruity loop, video "Setup" from this tutorial: https://www.sonicacademy.com/courses/uplifting-trance-2019-with-james-dymond,

where the tutor just goes into the mixer, select 4 channel strips, right click and select the "dock to the right" item, and it creates this nice separation between
the channel strips in the mixer.

![fruity-mixer-dock](https://lingtalfi.com/img/logicpro-feature-request-screenshots/fruity-mixer-dock-right.png)


So this made me think about custom mixer organization in general. 

I believe organization in the mixer is something the user should be able to do (same as re-arranging the tracks order in the arrange window).

I suggest this feature where the user is able to create mixer groups by selecting a number of channel strips (in the mixer window), and right click "create mixer group".

The group shall be visually delimited by some obvious boundaries, so that the user can easily see a group as such.
We should also be able to change the background color of the group, to make that visual separation even more obvious.
Also, we shall be able to drag and reposition the group horizontally to change its position in the mixer window, just like we should be able to do
for any channel strips (see my ["Being able to arrange the order of channel strips" idea](#being-able-to-arrange-the-order-of-channel-strips) for more details on that).





Select every other note
-----------
2020-08-23




So I have this bassoon pattern:

![bassoon pattern](https://lingtalfi.com/img/logicpro-feature-request-screenshots/select-every-other-note.png)


I want to put every other note on the lower octave, but I don't know how to select every other note at once.
I tried the default setting of the "select by sub-position" command, but it selects only one note every bar, not what I want.


So, I feel this is the kind of command that comes very handy in moment like that, and I miss it.
So I suggest that logic implements this command. 







Bugs
==========
2020-08-12



Drum machine designer bugs
---------
2020-08-12


### Bug1: cannot set the dmd on a track inside a folder stack
2020-08-12 
 
Let's say I have a folder stack with a few tracks in it.
Now if I create a new software instrument track and put it inside this folder, the "drum machine designer" instrument is disabled.

I believe that's a bug, because if I move this track out of the folder stack, not only the "drum machine designer" instrument is now enabled,
but now I can move it back into the folder stack.

So in the end, I still have my dmd instrument track inside the folder stack, so why not just allow its creation directly when the track is inside
a folder stack? (it sounds like a bug to me).



### Bug2: cannot change instrument when a dmd is set
2020-08-12 


Not sure if that's a bug, but it looks like it:
when I set a dmd instrument on a track, then I cannot change to another instrument, because in the (channel strip?) inspector the blue rectangle holding
the dmd name doesn't have the disclosure triangle next to it.

If it's not a bug, then I suggest that the user should be able to switch instrument no matter what instrument is set in the track/channel strip.








Log
===========


- 1.0.14: 2020-08-23: add "Select every other note" idea
- 1.0.13: 2020-08-15: add "Creating mixing groups" idea
- 1.0.12: 2020-08-12: add "Loop icon should be available to the left side of the regions too" idea
- 1.0.12: 2020-08-12: add "Drum machine designer bugs" bug
- 1.0.12: 2020-08-12: add "Being able to arrange the order of channel strips" idea
- 1.0.11: 2020-08-11: add "Duplicate dmd cells" idea
- 1.0.10: 2020-08-09: add "Slice at transient markers should be first class citizen" idea
- 1.0.9: 2020-08-09: add "Duplicate automation should snap to grid" idea
- 1.0.8: 2020-08-09: add "Pointer tool and automation" idea
- 1.0.7: 2020-08-05: add "Automation shape tools" idea
- 1.0.6: 2020-08-05: add "Extend audio region length like midi region" idea
- 1.0.5: 2020-07-29: update "Merge snap automation values and regular snap values altogether" section
- 1.0.4: 2020-07-28: added "Rectangular selection in automation mode" section
- 1.0.3: 2020-07-28: added "Select vertical slice by region" section
- 1.0.2: 2020-07-28: moved "Better arrangement track" to "Arrangement markers: free mode"
- 1.0.1: 2020-07-28: moved "Pattern copy track instead of arrangement track" to "Better arrangement track"
- 1.0.0: 2020-07-22: initial commit