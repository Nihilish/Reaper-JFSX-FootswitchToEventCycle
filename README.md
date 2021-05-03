# Reaper-JFSX-FootswitchToEventCycle
Short script to use a single event footswitch to toggle between two states.

I recently got a series of Neural DSP plugins, and I wanted to be able to switch between two presets when jamming along to some tracks, without having to stop playing or use automation. I had an old sustain pedal from one of my older keyboard laying around so I figured there would be a way to use it for that purpose. I opened the MIDI mapping section of Neural DSP to find that sadly there wasn't an option that would allow to 'cycle' between 2 different presets from a single MIDI event.

![image](https://user-images.githubusercontent.com/36556896/116931778-6ef62e80-ac2f-11eb-9247-33910cafbdb0.png)

Oh no! It seemed my idea wasn't going to work after all. I decided to message Neural DSP asking them if they had somekind of workaround but alas, there wasn't. They were super cool about it though, they suggested some alternatives, but nothing that would allow me to pick 2 specific presets. The only option I had would be to keep my foot on the pedal when playing with preset #1 and then release it when going back to preset #2. Which isn't really intuitive.

So I wrote a short JSFX script that would allow me to take the CC#64 input from my sustain pedal and remap it in an alterning pattern to two separate events, which could then easily be processed by Neural DSP.

![image](https://user-images.githubusercontent.com/36556896/116932227-fa6fbf80-ac2f-11eb-8bc0-8e2cb9f04a25.png)

The first slider is the number of the CC event you wish to remap. The 2nd and 3rd sliders are, respectively, the first and the second CC events you want to generate from the input. Then all I had to do was create a track that took MIDI input from the Channel 1 and send the MIDI to an Audio track with the Neural DSP FX. And it works really well!

Let me know if you have any questions on how to use it, and feel free to modify the script to your liking.
