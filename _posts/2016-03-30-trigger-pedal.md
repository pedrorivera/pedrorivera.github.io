---
title:        "Step up your captures with a scope trigger pedal"
# jekyll-seo-tag
description:  "A short description of the page's content"
image:        "/images/scope_pedal_diagram.png"
author:       "pedror"
---

<p class="lead">How many times do you find yourself probing two or more signals, and due to limb deficit, having to call your peers to push on the oscilloscope buttons?</p>How many of you have thought of training your cat to do the job? I did (not kitting), but giving it a second thought realized I could get into trouble. So instead I decided to build a trigger pedal that I could step on to start a capture.

First thing I think when a too simple to be true idea comes to my head is "There must be something out there already". You know, Google is there to break our hearts, always. But I was impressed by how hard it was to find something like the scope pedal, compared to how easily the tool would be made. Therefore I went ahead and built it. These are the only parts needed, I expect you to know what is going to happen by just looking at the list:

- Piano keyboard sustain pedal
- 3V coin cell battery 
- BNC female connector

![The tool](/images/scope_pedal.jpg)
Total cost: $15

## How it works
The sustain pedal is nothing but a switch with a long wire that plugs into the instrument. When the player steps on it, the switch closes a circuit and the instrument knows it has been activated. 

Our non-musical instrument, the scope, is triggered by the voltage level of a signal; so we have to make the pedal output a signal. The trick is to sneak a 3V coin cell battery into the pedal enclosure and break one of the two wires that go to the switch to connect the battery in series. This way when the user closes the circuit the oscilloscope will see a 0 to 3V step. Could it be *simpler* than that?

![How it works](/images/scope_pedal_diagram.png)

## How to setup the trigger
Besides having to dedicate one channel to the pedal there is another small catch. Unless you're not looking for a particular edge in the signal of interest, your scope needs to have A-B triggering or an equivalent feature. You're looking for a feature that would let you trigger on the rising edge of the pedal channel and wait for a trigger on the channel that you're interested in to start capturing. I believe most mid-sized scopes have some variation of this feature and some even have an AUX channel that is perfect for this scenario.

## Other alternatives
Like I mentioned before, I'm truly impressed that there aren't many other alternatives to satisfy the need. Maybe I'm missing on an obvious trick? (E.g. based on capture persistence). 

A recent [Hackaday article](http://hackaday.com/2016/03/29/you-speak-your-scope-obeys/) features a project that adds speech recognition to a scope to control it; however, I find it overly complicated and unreliable like everything that's ever had speech recognition built in. Instead of asking people to push the button you'll be asking them to keep silence, which is arguably more annoying.

Investing this little time on building the amazingly simple tool has saved me lots of time (and cats) and there is no longer a reason to call for help. If your work involves an oscilloscope I strongly suggest you your hands on building a pedal trigger.

