# Community hugo theme
## Setup
As with any other hugo theme, you can use it by cloning this repository into your site's `themes` directory:
```bash
git clone https://github.com/ifosch/hugo-theme-community
```

## Configuration
### Title
This theme uses your site's title as the main title in the header.
You can specify the colors using a separate CSS snippet in your site's `/static/css/` directory, like the following:
```CSS
.navbar-light .navbar-brand {
    color: #006e9f;
}
.navbar-light .navbar-brand:hover {
    color: #ffd732;
}
```
You can use similar trick to handle the font, including the corresponding sizes depending on the device's screen width.

### Logo
This theme uses a logo located in the path indicated by the `logo` parameter. To specify it, use the following snippet in your `config.toml`:
```TOML
[params]
  logo = "/images/logo.png"
```

### Navigations items
To add navigation menu, you can use Hugo's menu features, including a second level, using the following in your `config.toml`:
```TOML
[menu]
  [[menu.main]]
    identifier = "pybcn-association"
    name = "PyBCN Association"
    url = "/association/"
    weight = 1000

  [[menu.main]]
    parent = "pybcn-association"
    identifier = "information"
    name = "Information"
    url = "/association/information/"
    weight = 1100
```

### Debug mode
By running Hugo using the `DEBUG` environment variable set to anything, it will show some debugging information in the footer.
