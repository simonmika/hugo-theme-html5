# HTML 5 Theme for Hugo

HTML5 theme for the static site generator [Hugo](http://http://hugo.spf13.com).
It is not a complete theme but rather a set of templates that generates the necessary HTML. It also contains some sensible CSS reset.
It requires the end user to provide their custom design through CSS files.

## Features
 * CSS only designing.
 * Menu with infinitive levels.
 * Uses HTML 5 structural elements.
 * Contains a CSS reset.

## Getting Started
### Installing the Theme
#### Downloading
##### Git Submodule (recommended)
If you are keeping your full site in a git repository the recommended way is to use the theme as a submodule by issuing the following command in your Hugo site root directory:
```bash
git submodule add https://github.com/simonmika/hugo-theme-html5 themes/hugo-theme-html5
```
##### Git Clone
Clone this repository into your `themes` folder of your site. Issue the following command from within your Hugo sites root directory:
```bash
git clone https://github.com/simonmika/hugo-theme-html5 themes/hugo-theme-html5
```
##### Download
If you for some reason don't want to use Git simply download and unpack the theme from [here](https://github.com/simonmika/hugo-theme-html5/archive/master.zip).

#### Set theme as default
Set the theme as default in your sites configuration file located in your sites root directory.
##### JSON example (config.json)
```json
{
	...
	"theme": "hugo-theme-html5";
	...
}
```
##### TOML example (config.toml)
```toml
theme: hugo-theme-html5
```
##### YAML example (config.yaml)
```yaml
theme = hugo-theme-html5
```

### Add Stylesheets
Add CSS for your site into the static folder. For example:
```
static/css/layout.css
static/css/colors.css
```
And add it to your sites configuration file under the key `.params.css`:
##### JSON example
```json
{
	...
	"params": {
		...
		"css": ["layout.css", "colors.css"],
		...
	}
	...
}
```
##### TOML example
```toml
[params]
	...
	css = ["layout.css", "colors.css"]
	...
```
##### YAML example
```yaml
params:
	...
	css: ["layout.css", "colors.css"]
	...
```

### Add Icons
Add your sites favicon as a 192 by 192 pixels PNG file here:
```
static/favicon-192.png
```
The theme also supports an apple touch icon as a 180 by 180 pixels PNG file located at:
```
static/favicon-180.png
```
### Front Page Section and Lists
You can configure which section is used to populate the front page by setting the `Params.FrontPageSection` parameter to the section name.

To control how much of the article is showed for listing pages you may set the `Params.ListMode` and for the front page the `Params.FrontPageMode` to one of:
* `full` - showing the full article including header and footer
* `body` - showing the full article and the footer but no header
* `header` - only showing the header
* `summary` - showing the header and a possible truncated summary of the content but no footer

When using the `header` mode or if the content is actually truncated when using the `summary` mode, the article will have a self-link item added to it.
The purpose is to enable different styles of links to the full content selectable by using the right CSS styling. Here comes a few examples:

##### Read more link
```css
body > main > article > .self-link > a > span:before {
	content: "read more"
}
```
##### Article link
```css
body > main > article {
	position: relative;
}
body > main > article > .self-link > a > span {
	position: absolute;
	width: 100%;
	height: 100%;
	top: 0;
	left: 0;
	z-index: 1;
	background-image: url('transparent.gif');
}
```
The article link uses a single pixel transparent gif necessary in older browsers. It may be downloaded [here](https://github.com/simonmika/hugo-theme-html5/raw/example/static/css/transparent.gif) and placed with your CSS file.

### Create Menu
The menu used by the theme is called `main`.

## Additional Configurations

### Table Of Contents
By default, every article is preceded by a table of contents.
To disable this globally, set `Params.toc` to `false` in your site configuration.
To override the global setting, set `toc` in the front matter of an individual article.

### Word Counts
By default, every article is preceded by a word count and estimated reading time.
To disable this globally, set `Params.showWordCount` to `false` in your site configuration.

## Contributing

Please clone this repository and create pull-requests for any features that could have a more general use and that fit within the vision of this theme.
