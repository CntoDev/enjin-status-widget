This web page is designed to show status of components on a small sized Enjin widget.

## Requirements
 - jQuery (any version)

## Usage
Configure the Cachet API URL in `script.js` under `cachet_api_url` in the `config` object, i.e.:
```javascript
var config = {
    cachet_api_url: "your api url",
    ...
}
```

To add the widget on Enjin follow these steps:
 1. from Enjin panel create a new HTML module
 2. copy content from `status-widget.html` into the HTML section
 3. copy content from `script.js` into the JS section
 4. copy content from `style.css` into the CSS section

### Showing different names for components
Aliases allow to display a component with a different name from its name on Cachet.
To add an alias add an object into the `config.alias` array where `cachet_name` is the component's name on Cachet and `widget_name` is the name displayed on the widget, i.e.:
```javascript
var config = {
    ...
    aliases: [
        {   cachet_name: "name on Cachet",
            widget_name: "name on the widget" },
        {   cachet_name: "main server",
            widget_name: "server1" },
    ]
}
```
**NB**: `cachet_name` is case *insensitive* and its casing can be different than Cachet's one, but it *must* match letter by letter the component's name on Cachet (whitespaces included).
