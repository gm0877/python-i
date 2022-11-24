# python-i

import PIL
from PIL import Image

#Open Image
im = Image.open(r"C:\Users\manikanta\Downloads\eiffel-tower.jpg")
im.getbands()
im.mode

im.show()
#width=im.width
#height=im.height
width,height=im.size
print(width,height)
im.info
#Image rotate & show
im.rotate(45).show()
area = (width/2, height/2, width, height)
img = im.crop(area)

#img.show()
#RESIZE
im=im.resize((int(width/2), int(height/2)))
im.save('resiz.jpg')
im1=Image.open("resiz.jpg")
im1.show()
