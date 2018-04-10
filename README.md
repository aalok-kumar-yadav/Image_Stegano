## Image_Stegano : Hiding an image inside another image

## Description

This Project provides facility of hidining one image into another image ,we can performe images's RGB pixels
manipulation and send over the network and another side extract the hidden image. The advantage of steganography
over cryptography is that the wanted secret message does not attract attention to itself as an
object of scrutiny.


## Installation

Install pillow on ubuntu system for python

```bash
sudo apt install python-pil
```

Install pillow on ubuntu system for python3

```bash
sudo apt install python3-pil
```


## Internal Details

So basically a digital image is made by many small units called pixel and one pixel contains three different information
about Colour i.e RGB.

Whenever we change the pixel value then image colour is changed, our hiding is based on concept of LSB(least significant bit) and MSB( most significant bit).I mean each R,G,B contains a binary bit, when we made some change in LSB then no major
effect is performed but whenever we change MSB all the image is disrupted.


First of all take an digital image that obviously contains many pixel take initial one pixel remove last four bits of RGB 
and append First four MSB bits of another digital image and make a new pixel that is combination of those two .in this 
process fisrt image's maximum feature is preserved as well as we put some information in that pixel. Iterate this process of all the pixels available in image.


At this step we sucessfully able to hide one image's MSB into another image ,now this image may be send over network and 
and we can get the hidden image when we perform just opposite of above process i.e take received image's one pixel and split into two halfs and create two new pixels from them ,iterate this for all pixel of recieved image and we get the  two images.





