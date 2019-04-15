## config.toml example

``` baseURL = "/"
 languageCode = "en-us"
 title = ""
 theme = "trex"
 enableRobotsTXT = true
 canonifyURLs = true
 [params]
   description = ""
   #set true if it's a sub site
   subsite = "true"
   #colors
   background = "#FFF"
   primary = "#3C5A96"
   primary_light = ""
   secondary = ""
   tertiary_dark = ""
   tertiary = ""
 
 
 [permalinks]
   posts = "/:slug/"
 
 menu = ["main", "footer"]
 
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