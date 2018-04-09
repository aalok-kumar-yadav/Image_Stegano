# Image_Stegano : Hiding an image inside another

This Project provides the hidining(merging) one image into another image one images's RGB manipulation and send over the network and another side extract the hidden image. the advantage of The advantage of steganography over cryptography is that the wanted secret message does not attract attention to itself as an object of scrutiny.

# Installation

Install pillow on ubuntu system

```bash
sudo apt-get install libjpeg-dev
```
 
# Internal Details

So basically a digital image is made by many small unit called pixel and one pixel contains three different information
Colour i.e RGB.

whenever we change the pixel value then image colour is changed, our merging(hiding) is based on concept of LSB(least significant bit) and MSB( most significant bit) i mean each R,G,B contains a binary bit .when we made some change in LSB
then no major effect is performed but whenever we change MSB all the image is disrupted.

We take fisrt image and extract their MSB and also Second image's MSB after this we concate this bit and form a new image
and the when we want those image back we perform the opposite.


