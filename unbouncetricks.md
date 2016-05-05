# Unbounce Tricks and Frequently Asked Questions

None of these tricks will show up in the page builder part of Unbounce. You have to at least be in the preview screen of your site, and even then sometimes Unbounce will not read the code you have added, so to be overly safe publish the page to see these changes. 

### Sticky Header

  - Ex. http://www.liceclinicsmedway.com/immediate-contact2/

1. Click on Javascript, then click Add. Name this file whatever you would like to. 
2. Paste this code in the new file you just created
```sh
<script type="text/javascript">
  // Fixed Header v1.1
  // Replace ID below with your own box ID
  var boxToAppend = '#lp-pom-box-88';
  var boxParent = $(boxToAppend).parent();
  $(boxToAppend).clone().appendTo(boxParent).css({"position":"fixed", "left":"0", "top":"0", "width":"100%", "z-index":"899"}).children().remove();
  $(boxToAppend).css({"position":"fixed", "left":"auto", "top":"0px", "width":"100%", "z-index":"999", "border-style":"none none none none", "border-width":"0px", "background":"none"});
</script>
```
3. Set the placement of this script to "Before Body End Tag". 
4. Now hit the blue button that says "Save Code". 
5. Now insert a box the size you want your header to be into your Unbounce page and put all of the content on top of it (*Note* Make sure the items make the box turn a grey checkered, to make sure they are actually a part of the new box you created) that you want to be displayed on the header. Your box will only be the width of the page, but the code will make it stretch the full width of the screen.
6. Copy the ID tag of the box.
7.	Click on “Javascripts” and open the “Scrolling Header” (or otherwise named) script you just created.
8.	Replace #lp-pom-box-88 with the box ID tag you just copied.
9.	Save and publish!

### Take away Underline!!! 

This is a frequently asked question. How to take away the underline of a link you have made. 

##### Take away all underlines on page

1. Click on Stylesheets
2. Add a new one and name it whatever you want. 
3. Add this code to you blank style sheet (*Note* stylesheet must be blank or elese this will throw errors)
```sh
<style>
  a{
    text-decoration: none!important;
  }
</style>
```
4. Click the blue button to save code and all underlines will be gone. 
##### Take one underline on page - Maybe a linked phone number ect. 
1. Click on the text that is underlined. 
2. Click on the source so you see all the raw code. 
3. Go into the <a> tag and add style="text-decoration: none!important;"
4. Here is an example of where exactly to put it 
```sh
<a style="text-decoration: none!important;" href="tel:1-508-203-6971"><span style="color:#00a8ca;"><span style="font-size:36px;">508-556-1261</span></span></a>
```

### Make a phone number clickable, to make the call
*Note:* If you have a phone number on a landing page you should always do this! It raises conversions by 80% some articles claim. Don't quote me on that fact, that is off the top of my head. 

1. Click on the text where the phone number is at. 
2. Highlihgt the phone number within the text editor and click the link icon (It is the globe with the linked pieces of chain). 
3. Once the pop up window come up change the protocol to "tel:". 
4. Then simply put the phone number where a link usually goes. However it must be in this format!!!
```sh
541-680-5840
```
5. Also for international calling I always add the one in from of the number just to be safe. 
```sh
1-541-680-5840
```
6. Then simply click the "Okay" button and you have linked your phone number! 

### Add an Interactive Google Map

1. Go to https://www.google.com/maps
2. Enter in the address you would like the map to use. 
3. Once it has found the address click on the "Share" button
4. Once the window come up to share switch the the "Embed Map" section. 
5. Copy the Iframe code it provides you. 
6. Now go back to Unbounce. 
7. Drag a custom HTML box onto your page. 
8. In the window it pops up, paste the Iframe code you copied from Google. 
9. Hit save code. 
10. *If a problem occurs and the map does not initially show your location.*
11. Find the exact width and height of your custom HTML box. 
12. Go into the iframe code in the custom HTML box. 
13. Towards the end of the Iframe you will see 
```sh
width="600"
height="450"
```
14. Change these numbers to the exact width and height of your custom HTML box
ex. 
```sh
width="400"
height="250"
```
15. Save the code and your problem should be fixed. 
### List Item Bullets
##### Change the color of the actuall bullets
1. Click on "StyleSheets" and add a new Stylesheet. 
2. Name it whatever you would like. 
3. Copy and paste this code into the stylesheet. *Note: the stylesheet must be blank previous to the copy and paste or else it will throw errors.*
```sh
<style>
  ul {
    list-style: none!important;
    padding:0;
    margin:0;
}

ul li { 
    list-style: none!important;
    padding-left: 1em; 
    text-indent: -.7em;
}

ul li:before {
    content: "• ";
    color: #fff; /* or whatever color you prefer */
}
</style>
```
4. This exact code will turn the bullets white. However where it says "/* or whatever color you prefer */" just change the #fff to whatever the hexidecimal number is you want the color to be. 
5. Save the code and that it it. 
##### Put the bullets on the right hand side of a right aligned list
1. Click on Stylesheets and add a new Stylesheet
2. Name it whatever you would like.
3. Copy and paste this code into the stylesheet. *Note: the stylesheet must be blank previous to the copy and paste or else it will throw errors.*
```sh
<style>
  ul {
    direction: rtl!important;
  }
</style>
```

### Google Fonts
Clients sometimes ask for fonts that Unbounce does not have. Well Do not fear Google is here.
1. Go to https://www.google.com/fonts
2. Find the font that you want on your Unbounce page.
3. Click on the blue "Add to Collection" button for that font. 
4. A grey box will appear at the bottom of your screen. Click the "Use" button in the right hand corner of this grey box. 
5. It will take you to another screen. Scroll to the bottom of this screen. 
6. Where it says "Add this code to your website:" copy that line of code it provides. 
7. Now go back to unbounce. 
8. Create a new stylesheet and name it whatever you would like. 
9. Add this line of code you just coppied to this sytlesheet. Just this line and nothing else!!! It will probably say the stylesheet is invalid and give you an error. Well ignore this, Unbounce it dumb sometimes. 
10. Now you have 2 options. Proceed to the option you want to take. 
##### Add this font to all the text on the page!
1. Go back to google where it gave you the last piece of code. 
2. Now where it says "Integrate the fonts into your CSS:" copy that bit of code it provides you. 
3. Add a new sytlesheet once again and name it whatever you want. 
4. Add this code to the blank stylesheet. 
```sh
<style>
  p, h1, h2, h3, h4, h5, h6, span{
      font-family: 'Raleway', sans-serif!important;
  }
</style>
```
5. Replace "font-family: 'Raleway', sans-serif" with the line of code Google last provided you. However make sure to leave the "!important" at the end with no space inbetween the start of it and the end of your code. NO SPACE!!!!
6. Save your code and BAM!
##### You just want this new font for one piece of text. 
1. Click on the text you want to change the font of. 
2. Click on the Source. 
3. Take the line of code google gave to you and combine it with 
```sh
style="font-family: YourFont!important"
```
So it should look something like this
```sh
style="font-family: 'Raleway', sans-serif!important;"
```
4. Then take this new formed piece of code and add it within the p, h1, h2, h3, h4, h5, h6, or span tag. *This one isn't as straight forward, so don't hesitate to call me over for help*
Ex. 
```sh
<p style="font-family: 'Raleway', sans-serif!important;" class="lplh-58">Hello World</p>
```

