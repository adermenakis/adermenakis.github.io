---
layout: page
title: ICC Color Profiles
permalink: /iccColorProfiles/
description: "ICC Color Profiles with Qt and C++ for Embedded Systems"
---

# ICC Color Profiles with Qt and C++ for Embedded Systems

This article provides some basic information related to color profiles as well as a link to download my thesis work which includes also source code. the source code was testing on Nokia N900 and Nokia N9 and allows performing color conversion from one color profile to another through OpenGL ES and shaders.

You will find my thesis [here](http://uu.diva-portal.org/smash/record.jsf?pid=diva2%3A683909&dswid=-6544).

The full source code that was used for deploying on meego and maemo and getting the results discussed in my thesis can be downloaded from [here](/assets/data/iccColorProfiles/color_profile_conversion.zip).

## What are color profiles?

Color profiles are functions that map numbers to color values. For example if you have a color RGB(0,255,0) it means that:

Read = 0
Green = 255 (max)
Blue = 0
A color profile could swap values or intensities; hence say that RGB(0,255,0) is RGB(255,0,0), which means interpret red as green and green as red. Another example could be RGB(128,0,0). A color profile might say that intensity of 128 on red DOES NOT MEAN USE 0.5 RED TONE but use 0.25 Red tone.

## Why do we need color profiles?

Color profiles are needed to preserve colors of images and make them look the same among devices. Each input/output device that deals with printing/displaying/capturing images has a color profile, which shows how this device interprets the colors that are sent to it.

## Chromatic diagram showing different color profiles

![alt text](/assets/data/iccColorProfiles/10821118-md.jpg)

Image taken from [here](http://photo.net/learn/digital-photography-workflow/advanced-photoshop-tutorials/using-lab-color-adjustments/){:target="_blank"}

The area under each triangle in the diagram, represents the colors that a color profile can display.

In this diagram we can see several different color spaces and where they intersect. As it can be observed, no color profile can represent every single color. Additionally, each color profile has a different set of colors it represents.

## Do Color Profiles guarantee preserving colors?

**NO!**

There are two reasons:

Computers are not extremely accurate
When you use 8bits of data per color (which is a common practice) there will be a big data loss. The more bits used per color, the more accurate and less corrupted the result is.

Not all color profiles represent the same/all colors

## Converting one color profile to another?

When transforming some color from color profile X to Y, the color from the source X gets mapped to the closest color that can be found is the set of Y. In order to accomplish that a transfer function is required from moving a value from the X set to the Y set.

## How to correctly apply alpha blending when using color profiles

Most color profiles are not linear whereas the alpha channel is. Let's assume we are using 8bits for the alpha channel of an image and the alpha is set to 127. This 127/256 means that half opacity needs to be used. This creates an error when blending images that are not linear.

In order to apply properly blending with alpha channels the images need to be converted to a linear color space, get blended and then converted to a non-linear color profile such as sRGB. (remember that as stated above these conversions also will result in losses)

## What are embedded color profiles?

Embedded Color Profiles hold the information on how to interpret the pixel map of the image in which they have been embedded. Embedded color profiles are placed within an image's meta data section when exporting from some image editing software (i.e. GIMP, Photoshop) or devices such as photo cameras. A very good page to read about embedde colot profiles and image formats that support them is on the ICC's website the link provided [here](http://www.color.org/profile_embedding.xalter){:target="_blank"}.

## What is the default color profile of images?

When images do not have a color profile, the pixel map they hold is in sRGB format. sRGB was initially used by CRT monitors and has been kept on new screens for compatibility reasons. Most devices out on the market have some hardware that emulates the sRGB color space for the cases that the screen's output uses a different color space.

## Library for applying color profiles?

Most open source applications I have seen so far that have a color profile implementation are using littleCMS which stands for little Color Management System. It is certified by ICC as a correct color profile implementation. You can read more about the library and download littleCMS [here](http://www.littlecms.com/){:target="_blank"}.

## Qt Color Profile support

I have already worked on a patch that adds basic support on Qt and color profiles which has not been finalized yet. You can find more info here.

Tags:
