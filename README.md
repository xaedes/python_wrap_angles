# python_wrap_angles
Wrap angles to equivalent angles

```python

import math
# degree to radian
d2r = math.pi / 180
# radian to degree
r2r = 180 / math.pi

def wrapTo2Pi(rad): 
    return rad % (2*math.pi)

def wrapToPi(rad):
    return wrapTo2Pi(rad + math.pi) - math.pi

def angleDiff(rad0, rad1):
    r0 = wrapToPi(rad0)
    r1 = wrapToPi(rad1)
    return wrapToPi(r1-r0)

def wrapToPiSeq(rad0, rad1):
    r0 = wrapToPi(rad0)
    r1 = wrapToPi(rad1)
    diff = wrapToPi(r1-r0)
    return rad0+diff

```
