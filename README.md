# Obamicon
This code changes one's pictures to the colors Obama used his in campaign advertisements. Thus this project is called Obamicon

from Myro import* 
pic = makePicture("3002ac3.jpg")
show(pic) 
lst = getPixels(pic)
Obama_DarkBlue = makeColor(0,51,76)
Obama_Red = makeColor(217, 26, 33)
Obama_Blue = makeColor(112,150,158)
Obama_Yellow = makeColor(252, 227, 166)
for pix in lst:
    r = getRed(pix)
    b = getBlue(pix)
    g = getGreen(pix)
    gray = (r+b+g)/3
    if gray > 180:
        setColor(pix,Obama_Yellow)
    elif gray > 120:
        setColor(pix,Obama_Blue)
    elif gray > 60:
        setColor(pix,Obama_Red)
    else:
        setColor(pix,Obama_DarkBlue)
