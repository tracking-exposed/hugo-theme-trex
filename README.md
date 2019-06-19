Hugo TRex Theme
===============

Hi. I'm the hugo TRex starter theme. I'm a theme meant for hacking so try
turning me into the next awesome TRex website. That's what I'm here for.


## Getting Started

1. Download the **trex** theme folder into Hugo theme folder

```
cd new-site.tracking.exposed/themes
git clone https://github.com/tracking-exposed/hugo-theme-trex trex
```

2. In the `config.toml` file of your new site edit the value `theme="trex"`
3. Copy sample content from `exampleSite` into the sites `contents` folder


## Config File

For each site modify the `config.toml` to define the following Hugo `[params]`

```
[params]
  subtitle = ""
  subsite = "default"
  description = ""  
  tagline = ""
```

- `subtitle` - title of the site as written along side `Tracking Exposed`
- `subsite` - name-space used in HTML and CSS classes (lowercase + no spaces)
- `description` - the main `<meta>` description for the site used for SEO
- `tagline` - text that is shown in the home page banner above featured


## Menus

There are multipe *"menus"* that get re-used in different areas of the site.
The following are the three that are **required** for the theme to build.

- `[[menu.main]]` - the links in the `<navbar>` at the top of pages
- `[[menu.featured]]` - featured boxes on home page of each site (max 3)
- `[[menu.footer]]` - special per site links in `<footer>` of pages

``` 
[menu] 
  [[menu.main]]
     page = "Help"
     identifier = "help"
     name = "Help"
     url = "/help/"
     weight = -150
  
  [[menu.featured]]
     page = "Facebook"
     identifier = "facebook"
     name= "Facebook"
     url = "https://facebook.tracking.exposed"
     weight = -180

  [[menu.footer]]
      page = "Help"
      identifier = "help"
      name = "Help"
      url = "/help/"
      weight = -150
```

Extra menus can be added as needed such as in `tracking.exposed/config.toml`


## SASS Architecture

The following files are how the SASS that is compiled into CSS are organized.
The theme is built on top of using [Bootstrap 4](https://getbootstrap.com)
framework.

- `assets/_bootstrap_customization.scss` - proper extensions of various Bootstrap classes
- `assets/_components.scss` - specific custom classes for areas of sites for apps (Reality Check, Zuckless News)
- `assets/_mixins.scss` - reusable SASS mixins that extend or customize Boostrap styles or custom things
- `assets/_variables.scss` - used throughout all SASS files
- `assets/main.scss` - main file which has global `body.subsite` class and other custom things


## Updating Theme

As the theme is updated and developed in the future, for instance once a new
color scheme (for a subsite) is created, do the following steps

```
cd new-site.tracking.exposed/theses/trex
git pull origin master
```

Then `hugo build` and voila the theme is updated
