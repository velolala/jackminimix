[![Build Status](https://travis-ci.org/njh/jackminimix.svg?branch=master)](https://travis-ci.org/njh/jackminimix)

JackMiniMix
===========

JackMiniMix is a simple mixer for the  Jack Audio Connection Kit with an OSC 
based control interface. It is released under the  GPL licence.

For the latest version of JackMiniMix, please see:
http://www.aelius.com/njh/jackminimix/


OSC Interface
-------------

Channels numbers range from 1 to the total number of channels. Gains are in floating point decibels in the range -90 to 90 dB, where -90 dB is treated as infinite.

    /mixer/get_channel_count        - Get the number of channels
     replies with:
    /mixer/channel_count (i)

    /mixer/channel/set_gain (if)    - Set the gain of channel i to f dB
     replies with:
    /mixer/channel/gain (if)

    /mixer/channel/set_label (is)   - Set the label of channel i to s
     replies with:
    /mixer/channel/label (is)
 
    /mixer/channel/get_gain (i)     - Get gain of channel i
     replies with:
    /mixer/channel/gain (if)

    /mixer/channel/get_label (i)    - Get the label of channel i
     replies with:
    /mixer/channel/label (is)
  
    /ping                           - Check mixer is still there
     replies with:
    /pong

Replies are send back to the port/socket that they were sent from.

