# Hugo TRex theme

Hi. I'm the hugo TRex starter theme. I'm a theme meant for hacking so try turning me into the next awesome TRex website. That's what I'm here for.


## Getting start

+ download the **trex** theme folder into Hugo theme folder
+ add "trex" as theme value in `config.toml`
+ download sample content into hugo contents folders, if you need

### Params variable

In your config.toml define these parameters:

```
[params]
  description = ""
  subsite = "true"

  #colors
  background = "#FFF"
  primary = "#3C5A96"
  primary_light = ""
  secondary = ""
  tertiary_dark = ""
  tertiary = ""
```

+ `description`: is the main meta description for the website, usefull for SEO
+ `subsite`: if `true` it change the layout form generic ones into color specific one. It enable the colored header with the white logo version
+ `background`: the backgorund color, default: *#F2F6F5*
+ `primary`: the main subsite color, it define the header background color, default: *#003399*
+ `primary_light`: used for link hover, default *#5472cb*
+ `secondary`: used for alert and advise, default *#FFCC00*
+ `tertiary_dark`: used for button, default *#FC1D6A*
+ `tertiary`: used for button hover, default *#dc1a59*


## How to hack

+ Write custom CSS rules into `assets/sass/_site.scss`
+ Write custom JS into `static/js/script.js`
+ Use `layouts/page/custom-page.html` to create your own custom page connected to `content/page/custom-page.md`


## UI tool

### Built-in overlay

Add overlay elements into the DOM like this

``` 
<div class="overlay" id="overlay-ID">
    <a class="close-btn" href="#">x</a>
    <!--Your content-->
</div>
<div id="overlay_shade"></div>
``` 

Into `script.js` call the overlay with the trigger you want using this function `openOverlay('#overlay-ID')` with the overlay ID as argument;


## Menu manage

You have two menu: header and footer. Header menu support sub navigation adding in the `parent` element value the parent's identifier value

``` 
 menu = ["main", "footer"]
 
  #Header menu
  
  [[menu.main]]
     page = "Pages"
     identifier = "pages"
     name = "Pages"
     url = "#"
     weight = -100
  [[menu.main]]
     page = "#"
     identifier = "#"
     name = "Test"
     url = "#"
     parent = "pages"
     weight = -110
  [[menu.main]]
      page = "#"
      identifier = "#-2"
      name = "Test 2"
      url = "#"
      parent = "pages"
      weight = -120
  [[menu.main]]
     page = "Typography"
     identifier = "typography"
     name = "Typography"
     url = "/help/typography/"
     weight = -130
  [[menu.main]]
     page = "Images"
     identifier = "images"
     name = "Images Alignment"
     url = "/help/images/"
     weight = -140
  [[menu.main]]
     page = "Help"
     identifier = "help"
     name = "Help"
     url = "/help/"
     weight = -150
 
 
  #Footer menu

  [[menu.footer]]
      page = "Typography"
      identifier = "typography"
      name = "Typography"
      url = "/help/typography/"
      weight = -130
  [[menu.footer]]
      page = "Images"
      identifier = "images"
      name = "Images Alignment"
      url = "/help/images/"
      weight = -140
  [[menu.footer]]
      page = "Help"
      identifier = "help"
      name = "Help"
      url = "/help/"
      weight = -150
```