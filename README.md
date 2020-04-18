# linux-opl3-tuning-patch
This patch "tunes" the OPL3 Midi synth inside the linux kernel driver to the standard "A4 = 440Hz" concert tuning on the newer YMF289 based chips.

## Background

These Chips must be fed with the correct frequency for each note, calculated with a formula. See
http://nerdlypleasures.blogspot.com/2018/01/opl23-frequency-1hz-ish-difference.html for details.

Because of the difference between older (YMF262) and newer (YMF289, XMF7xx a.k.a. OPL3-SAx) chips, there are two sets of frequencies.
This patch here is for the newer ones.

Here's a table: https://docs.google.com/spreadsheets/d/1VDaP6zOl_oepKeAWV198P_BJIU5EZP9SCAXf9TXKmHc/edit?usp=sharing

Interestingly, the original values in the kernel code match neither. Maybe the original author's hardware clock was off?
