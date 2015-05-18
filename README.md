### bconvert

A utility script to use Blitline as if you were just using ImageMagick's convert from the command line. You can use this on a machine that has NO image processing libraries installed. That's right, you don't need to install anything!* *not entirely true*... You need linux and python installed. Most default distros come with this out of the box, so just fire up an AWS instance, or DigitalOcean and run imagemagick convert commands without ever intsalling anything else.

Please note, this is NOT a production solution! It's a handy tool when you want to process something locally without having to set up a Blitline application. It's effectively a "toy" so please treat it as such.

<br/>


##Usage:

Use bconvert as you would use convert. Parameters should match directly to convert params.

    bconvert rose: -set label "rose with a label" output.png

    bconvert -size 10x30 xc: -draw 'line 5,0 5,30' -background white   -rotate 17  -scale 500%  output.png

    bconvert https://s3.amazonaws.com/img.blitline/test_pngs/apple.png -background none  -shear 30  output.png

####Caveats! Important! READ!

- You must output a file called **output.png**
- Input files will need to be built-in ones, or URLs. It WON'T work with local image files (Blitline doesn't allow **UPLOADS**)

<br>


##Installation:

####Mac

brew install python

####Linux

Should just work. Might have to install 'requests' (sudo apt-get install pip && pip install requests) on old distributions

####PC

Dunno. If someone out there wants to try it and tell us what is necessary, we'll update these here instructions.

<br>

##Getting Started:

1. Get an Application ID from [Blitline.com](http://www.blitline.com) (it's free!)
2. Copy the bconvert file in this repo to your /usr/bin directory
3. chmod 755 /usr/bin/bconvert
4. export BLITLINE_APP_ID=<YOUR APP ID from step 1)

<br/>

Now, you should be able to just run the examples above.

		bconvert rose: -set label "rose with a label" output.png

<br/>
