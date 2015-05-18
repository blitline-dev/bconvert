### bconvert

<br/>

A utility script to use Blitline as if you were just using ImageMagick's convert from the command line. You can use this on a machine that has NO image processing libraries installed. That's right, you don't need to install anything!*

<br/>

\*not entirely true... You need linux and perl installed. Most default distros come with this out of the box, so just fire up an AWS instance, or DigitalOcean and run imagemagick convert commands without ever intsalling anything else.

<br/>

##Usage:

Use bconvert as you would use convert. Parameters should match directly to convert params.

    bconvert rose: -set label "rose with a label" output.png

    bconvert -size 10x30 xc: -draw 'line 5,0 5,30' -background white   -rotate 17  -scale 500%  output.png

    bconvert https://s3.amazonaws.com/img.blitline/test_pngs/apple.png -background none  -shear 30  output.png

<br/>

##Installation:

-Mac-

brew install python

-Linux-

Should just work. Might have to install 'requests' (sudo apt-get install pip && pip install requests) on old distributions

-PC-

Dunno. If someone out there wants to try it and tell us what is necessary, we'll update these here instructions.


##Getting Started:

- Copy the bconvert file in this repo to your /usr/bin directory
- chmod 755 /usr/bin/bconvert


You MUST have a [Blitline.com](http://www.blitline.com) subscription (developer accounts are FREE!)

Once you have a Blitline account, you will have a Blitline Application ID.

On your system, set the environment variable BLITLINE_APP_ID to be your Blitline Application ID.

Now, you should be able to just run the examples above.

bconvert rose: -set label "rose with a label" output.png

<br/>
