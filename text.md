---
layout: default
---

[Cybernetic Architecture](index)

For this presentation, I would like to talk about cybernetic architecture. I
will explain later what I mean by these terms.

[Automated Experimental Rig](robot-feeding)

In my last presentation, I talked about an experimental rig that automatically
feeds food pellets to a mouse.

I used the image of Rosie the Robot to represent this automated experimental rig
because it contains sensors, actuators, and a little bit of intelligence, just
as you would find in any robotic system. The implementation details do not
particularly matter for this discussion. We created one version of this rig that
uses a rotating disk to present the pellets to the mouse. Jon is creating a new
version using a motorized X-Y-Z linear stage.

[Communication Transmitter](teensy-transmitter)

Then I talked about selecting a transmitter that would allow both humans and
Rosie to communicate with a mouse. The human and Rosie trigger the transmitter
to play tones that the mouse ear hears and sends the received messages to its
brain.

[Transmitter Options](audio-controller)

There are many possible choices of transmitter we could use. Say the researcher
gave you the specific problem of playing a 5000 Hz tone for 200 milliseconds.
You could solve this problem with a purely mechanical solution, such as a bell,
or whistle, or cuckoo clock. You could combine mechanics and electronics to play
tones using a speaker and control circuitry. You could combine mechanics,
electronics, and software with a general purpose computer programmed to play a
tone with a speaker. One approach to selecting a transmitter might be to
minimize the number of parts. A bell or tuning fork could be a simple and
elegant solution.

Whenever someone asks you to work on a project like this, however, you should
never just solve the exact problem you are given. You should always solve a set
of problems that contains the solution to the exact problem you are given. For
no matter what they say, the requirements of the project will probably change
over time as they use and test your solution. If your project has severe
constraints, such as limited cost, or time, or size, or power requirements, the
size of the solution set may have to be small, but the larger the solution set,
the more adaptable it will be to future changes.

The researcher may swear up and down that he will only ever need a 5000 Hz tone,
but then find out later after testing that the mouse confuses the 5000 Hz tone
with another sound in the environment and needs to shift that tone to 7000 Hz.
If you solved the problem with tuning fork that only plays one frequency, then
you will have to physically swap out the fork to play a new frequency. You could
blame the researcher and tell him it is his fault for picking the wrong
frequency and he will have to wait a week for you to order a new tuning fork. A
better response, though, is to be able to say, sure 7000 Hz is easy, let me
change this one line of code in my software.

This type of adaptability may push you towards selecting a more complex solution
containing more parts. The solution with more parts may turn out to be less
expensive and time consuming to manufacture than the simple solution, so solving
a larger set of problems may not always add to the cost.

[Solution Set Limitations](hearing-range)

You need to be careful, however, because sometimes increasing the size of the
solution set does add to the cost, so you have to make tradeoffs and anticipate
possible requirement changes and risks.

For example, mice can hear much higher frequency than humans. You might imagine
lots of experiments that could take advantage of that, so could be tempted to
make your audio transmitter work in the full mouse hearing frequency range.
