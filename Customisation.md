<b><font size='6'>Customisation</font></b>

A quick guide on how to edit the main features of my HUD.





<b><font size='5'>Index</font></b>

1. <a href='http://code.google.com/p/starks-hud/wiki/Customisation#1._How_to_Edit_the_HUD_Files'>How to Edit the HUD Files</a>

2. <a href='http://code.google.com/p/starks-hud/wiki/Customisation#2._Custom_Crosshairs'>Custom Crosshairs</a>

3. <a href='http://code.google.com/p/starks-hud/wiki/Customisation#3._Colours_and_Positioning'>Colours and Positioning</a>

4. <a href='http://code.google.com/p/starks-hud/wiki/Customisation#4._Removing_the_Health_Cross'>Removing the Health Cross</a>

5. <a href='http://code.google.com/p/starks-hud/wiki/Customisation?ts=1347460439&updated=Customisation#5._Main_Menu'>Main Menu</a>






# <font size='3'>1. How to Edit the HUD Files</font> #

Assuming you've installed the HUD correctly, the HUD files you'll want to be editing will be in the <i>Resource</i> and <i>Scripts</i> folders in <i>steam/steamapps/USER NAME/team fortress 2/tf/</i>.

The main file in question is the <i>.res</i> file which can be opened with Notepad. Personally, I prefer <a href='http://notepad-plus-plus.org/download/v6.1.7.html'>Notepad++</a> as it makes editing several files at the same time much easier but you can use whatever.

To edit the <i>.res</i> files, just open with Notepad and change the values you wish. You can save most HUD files while in the game and reload the HUD to view your changes (with the console command <i>hud_reloadscheme</i>) but for other files (e.g. <i>clientscheme.res</i>) you will have to reopen TF2 to view the changes.




# <font size='3'>2. Custom Crosshairs</font> #


To enable or disable custom crosshairs already in my HUD (currently only 1) go into <i>tf/scripts/</i> and open <i>hudlayout.res</i> in Notepad. Look through the first few paragraphs looking at the titles of each paragraph (the only one at the moment is called <i>xHair // ...</i>). When you find the crosshair you want to enable look under the title for the <i>visible</i> and <i>visible_minmode</i> entries and change them both from "0" to "1".

You can also change the colour here as well by editing the <i>fgcolor</i> entry. The colour code is RGBA. A stands for Alpha or transparency (with 255 being opaque and 0 being transparent). You can find most RGB colours <a href='http://www.webdiner.com/annexe/hexcode/hexcode.htm.'>here</a> or refer to the <a href='http://code.google.com/p/starks-hud/wiki/Customisation#3._Colours_and_Positioning'>Colours and Positioning</a> section of this guide.

In the likely event that the crosshair is not centered (you can check using the in-game crosshairs) you can either:

1. Whine to me to get off my lazy arse and fix the custom crosshairs or...

2. Attempt fix the crosshair position yourself by changing the <i>xpos, ypos, wide</i> and <i>tall</i> values.

If you want to edit the colour change when you hit someone (<i>example</i>) then you'll need to go into <i>tf/scripts/</i> and open the <i>hudanimations_tf.txt</i> file. Once in, scroll right to the bottom of the document to <i>event damagedplayer</i>. The top value is the colour the crosshair changes to when you damage someone and the second value is the colour the crosshair changes back to after damaging someone (this should be the same as the fgcolor in <i>hudlayout.res</i>


# <font size='3'>3. Colours and Positioning</font> #
Ninety percent of the time, changing the colours and positioning of elements in a HUD is very simple. We'll take the health acount as an example.

<b>Positioning</b>

The ammo <i>.res</i> file is called <i>hudammoweapons</i> and is in <i>tf/resource/ui/</i>. Once you've opened that, go to the <i>ammoinclip</i> section and you can change the <i>xpos</i> and <i>ypos</i> values to move it around the screen <i>(note that increasing the ypos will move the element downwards)</i>.
Position values can be changed with putting a <i>r</i> or <i>c</i> in front of the number (no space). An <i>r</i> in front will reverse which direction of the number (so increasing the <i>ypos</i> value would move it upwards rather than downwards). A <i>c</i> in front means you're drawing the position from the center of the screen (so if you had a . on the screen with the <i>xpos</i> and <i>ypos</i> value of "c0" it would be directly in the center ). Using the <i>c</i> prefix is good if you're planning to make a HUD which works on all resolutions.

If you're changing the <i>xpos</i> and <i>ypos</i> values and nothing is happening when you use <i>hud_reloadscheme</i>, check if you are in min mode <i>(cl_hud_minmode 1)</i>. If you are in min mode, change the <i>xpos/ypos_minmode</i> commands. If there is no _minmode entry and you're in min mode, it will use the normal value._

<b>Colours</b>


# <font size='3'>4. Removing the Health Cross</font> #

# <font size='3'>5. Main Menu</font> #

<b><font size='3'>Still got an issue?</font></b>

Try reading <a href='http://flamehud.googlecode.com/files/FlameHUD.pdf'>Flame's guide</a> or watching <a href='http://www.youtube.com/playlist?list=PLE43CB433F747821E'>Rads' tutorials on Youtube</a>