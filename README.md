# An Experimental MIDI Feature Visualization
## Project Focus
Developed a proof-of-concept animation patch in Max/MSP to explore real-time visualization of abstract MIDI data (pitch, velocity, note duration, and track identity).  The challenges encountered in managing MIDI streams during this project led directly to the development of the JS script in another Max project [MIDI_parsing_thru_JS_in_Max](https://github.com/tellmeayu/MIDI_parsing_thru_JS_in_Max).

## Intro
The patch is a general tool for midi visulisation which can read midi file, record notes' timing information (as prepared data) for drawing. The painting section read out the stored timing data, mapping them to the corresponding x/y coordinates in lcd canvas and draw some colorful patterns.

Providing these processing methods, the patch could be used for any midi file, but the current project is specifically for Trout Quintet (the 4th movement of Schubert's Piano Quintet in A major, D.667), the two-minute music piece embeded in the project is a short excerpt of the Trout theme.

The initial idea is quite simple --- get each midi note's pitch, velocity and duration, mapping to certain pattern's attribute, then draw it. However, as a visulisation for music, one big chanllenge is TIME. As every Max user knows, there's no timeline ready for you in Max environment. The build-in midi processing objects, like [midiparse], [midiinfo], [midiformat] and the sequencer [seq] can only give you individual midievent like pitch, velocity, ect. How to solve the timing problem became the core of this project. 

For more details: https://www.sylviastudio.cn/midi-visulisation-max-project-for-schuberts-trout-quintet/

 A demo video: https://www.youtube.com/watch?v=9X_WIT-fNKw

![](https://www.sylviastudio.cn/wp-content/uploads/2024/04/Screenshot-2024-04-19-at-19.54.52.png)
