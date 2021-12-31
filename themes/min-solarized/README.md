## min-solarized-theme

A minimal solarized hugo theme 


## Getting started

Inside your project hugo folder, copy the theme to your `themes` folder.

```bash
git clone https://github.com/thanatoslayer6/min-solarized-theme themes/min-solarized
rm -rf themes/min-solarized/.git
```

If you'd like some example content and an example config file to get started, you can copy the `exampleSite` directory into your root Hugo directory.
Simply execute the command below inside your project root or hugo site.

```bash
cp -r themes/min-solarized/exampleSite/* ./
```

To learn more about building themes in Hugo, refer to Hugo's [templating documentation](https://gohugo.io/templates/).

## Configuration

#### Homepage

To change the contents of the homepage, simply edit the file located in `content/_index.md` 
```md
---
heading: "Hello_World!" <!-- Main heading --!>
subheading: "Welcome to my personal site" <!-- some desc --!>
handle: "example@gmail.com" <!-- your email here --!>
---
```
### Links and others (Homepage) (Navigation menu)

To change the links in the navigation bar to your liking, edit `config.toml` file in your project directory, also changing
the social icons in the Homepage would require you to edit this file

```toml
baseURL = 'http://example.org/'
languageCode = 'en-us'
title = ''
paginate = 5
theme = "min-solarized"

[params]
  # Icon order here change to "" to display nothing
  iconOrder = [ "GitHub" ]
  github = "https://github.com/yourusernamehere"
  twitter = "https://twitter.com/yourusernamehere"

## Menu change the values if you want here
[menu]
  [[menu.main]]
    name = "home"
    url = "/"
    weight = 1

  [[menu.main]]
    name = "blog"
    url = "/blog"
    weight = 2

  [[menu.main]]
    name = "tags"
    url = "/tags"
    weight = 3

## Changed Markup settings for compatability
[markup]
  [markup.highlight]
    codeFences = true
    
  # Set to false to disallow raw HTML in markdown files
  [markup.goldmark.renderer]
      unsafe = true
      hardwraps = true
```
