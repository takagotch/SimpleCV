### simplecv
---
http://simplecv.org/

https://github.com/sightmachine/SimpleCV

```py
from SimpleCV import Camera

cam = Camera()

while True:

  img = cam.getImage()
  
  img = img.binarize()
  
  img.drawText("Hello")
  
  img.show()
```

```
```

```
```


