---
title:  “[matplotlib] How to use plot_surface”
last_modified_at:   2020-08-30
author: dsaint31
categories: 
  - Python
use_math: false
tags: 
  - plot_surface
---

# [Matplotlib] How to use plot_surface

`view_init`
* 단위는 degree임. 
* 시점을 결정.

```python
from scipy import misc
import cv2
import numpy as np
import matplotlib.pyplot as plt

img = misc.face()
img_gray = cv2.cvtColor(img, cv2.COLOR_RGB2GRAY)
h,w = img_gray.shape
x,y =np.mgrid[0:h,0:w]

ax = plt.figure().gca(projection=‘3d’)
surf = ax.plot_surface(x,y,img_gray,cmap=plt.cm.gray)
ax.set_zticks([]);ax.set_yticks([]);ax.set_xticks([])
ax.view_init(89,20)
plt.gcf().colorbar(surf,shrink=1,aspect=10)
```