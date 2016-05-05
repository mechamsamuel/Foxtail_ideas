# Unbounce Tricks

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
