*********************
Overview
*********************

It is well known that even after a light has been turned off, human eye keeps
"seeing" it for a fraction of second. This is known as Persistence of Vision, or
POV, and it allows one to "paint" pictures by quickly moving a strip of LEDs,
drawing one line of an image at a time in quick succession. If you search online
(e.g. on Etsy), you can find quite a few toys based on this idea: pois, staffs,
and more.

However, these are expensive: typical prices for a POV staff of decent
resolution start at $500, and they use proprietary software, so there is no easy
way to modify their behavior or add extra functionality. Thus, when looking for
a birthday gift for a friend who enjoys painting with light, I decided to create
my own open source version using readily available components.

My project builds upon the outstanding `work of Phillip Burgess and Erin St
Blaine <https://learn.adafruit.com/pov-dotstar-double-staff>`__ from Adafruit;
however, I made a few changes, upgrading the electronics.
Below are key features of this project:

* It is a two-sided staff, of total length 141 cm (55in); it is not collapsible.
  Each side of the staff has two 50cm/72 pixels LED strips, for the total of 288
  LEDs. Thus, you can use it to show images with 72-px resolution.

* Staff is powered by two 18650 Li-Ion batteries, which should be enough for at
  least 1 hr show, possibly as much as 2 hours, depending on intensity of your
  images. The batteries can be recharged via micro-USB connector; full charge
  time is about 5 hrs.

* Images (in bitmap format) can be easily uploaded to the
  staff by connecting the staff to a computer, where it appears as a USB
  storage device. It has enough memory for about 50 images. The order in which
  images are shown is described in a separate plain text file, where you can
  put a list of images and durations. An image can be listed there several
  times, or none at all.

* The staff contains an Inertial Motion Unit (IMU) which can be used to
  detect when the staff is in motion. The software uses it to adjust update
  frequency for images, so the images will not appear stretched or compressed
  regardless of how fast you are rotating it. You can also use it for
  controlling your show: e.g. stopping the staff horizontally is used as a
  signal to move to the next image in the slideshow. The software is based on
  Arduino IDE. It is available under an open source license and is easy to
  modify to suit your needs.

This project is open source; all code and schematics are available in my github
repository under MIT license.


For those who want to create your own staff, you can buy a kit of parts, which
includes most of the parts needed (except for LED strips and tube), from my
`Tindie store <https://www.tindie.com/stores/irobotics/>`__. Of course, you
can also build your own by sourcing all components independently -- see
building instructions for details.
