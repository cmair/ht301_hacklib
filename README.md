# ht301_hacklib
ht-301 thermal camera opencv python lib.

This fork is a hack to support InfiRay T2S+!
Note: measuring higher temperatures than +116°C does not work!

**Important note:
upstream now got a lot of improvements including a proper version of my hacks to support T2S+.**

**Please use https://github.com/stawel/ht301_hacklib instead of this old fork!**

---


Supported thermal cameras:
- Hti HT-301
- Xtherm T3S, thanks to Angel-1024!

It's a very simple hacked together lib, might be useful for somebody,  
uses `matplotlib` which is a little bit on the slow side,  
or pure `opencv` - much faster but without most features

Tested on ubuntu 20.04:

```
$ ./pyplot.py
keys:
    'h'      - help
    'q'      - quit
    ' '      - pause, resume
    'd'      - set diff
    'x','c'  - enable/disable diff, enable/disable annotation diff
    'f'      - full screen
    'u'      - calibrate
    't'      - draw min, max, center temperature
    'e'      - remove user temperature annotations
    'w'      - save to file date.png
    'r'      - save raw data to file date.npy
    ',', '.' - change color map
    'a', 'z' - auto exposure on/off, auto exposure type
    left, right, up, down - set exposure limits

mouse:
    left  button - add Region Of Interest (ROI)
    right button - add user temperature annotation
```
![pyplot output](docs/pyplot-output1.png)
![pyplot output](docs/pyplot-output2.png)

View saved ('r' key) raw data file:
```
$ ./pyplot.py 2022-09-11_18:49:07.npy
```

Opencv version:
```
$ ./opencv.py
```
![opencv output](docs/opencv-output.png)
