## Heating things with Quiescent current

See https://github.com/karlp/zypsnips/blob/master/lm1117.replacements.for.glory.md

Demo PCB to show off how horrificall inefficient LM1117 style devices are.

5mA Iq! Do _not_ use these parts! It's the 21st century! you can do better!

## Particulars

LM1117 family parts specify "typical" Iq of 5mA.  Power losses are P=VI, with V being the Vin
So 40x5x5e-3 = ~1W of wasted power.  It's _probably_ not actually possible to pack this tight
to actually get any meaningful heat raise, but the idea is to at least demonstrate that with
a ~zero load, you still consume serious power.

Things we've shortcutted with:
* LM1117 specifes ~2mA minimum load required to ensure regulation.  hah, like we care
  about regulation anywya
* LM1117 _prefers_ to have input capacitance, but admits that the power supply caps may
  be sufficient.
* LM1117 specifies min 10uF output capacitance.  We're going to yolo that, for demo purposes.

## Thanks
Mad props to the l33t hacking crew in HASHHASHGD32, as always.

