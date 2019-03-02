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


from SimpleCV import Image, Color, Display

def halfsies(left,right):
  
  result = left
  
  crop = right.crop(right.width/2.0,0,right.width/2.0,right.height)

  result = result.blit(crop,(left.width/2,0))
  
  return result
  
img = Image('http://i.imgur.com/lfAeZ4n.png')

output = img.binarize(90).invert()

result = halfsies(img,output)

result.show()

result.save('juniperbinary.png')


import SimpleCV
camera = SimpleCV.Camera()
image = camera.getImage()
image.show()


from SimpleCV import *
disp = Display(displaytype='notebook')
img = Image('simplecv')
img.save(disp)
```

```
docker pull sightmachine/simplecv
docker run -p 54717:8888 -t -i sightmachine/simplecv
curl http://localhost:54717
curl http://192.168.103:54717
```

```
```


