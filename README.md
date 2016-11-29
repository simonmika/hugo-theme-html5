# HTML 5 Theme for Hugo

HTML5 theme for the static site generator [Hugo](http://http://hugo.spf13.com).
It is not a complete theme but rather a set of templates that generates the necessary HTML. It also contains some sensible CSS reset.
It requires the end user to provide their custom design through CSS files.

## Getting started
### Clone
Clone this repository into your `themes` folder of your site. Issue the following command from within your Hugo sites root directory:

	git clone https://github.com/simonmika/hugo-theme-html5 themes/html5

### Add stylesheets
Add CSS for your site into the css folder. For example:

	static/css/layout.css
	static/css/colors.css

And add it to your config under `.params.css`:

#### TOML example:

	[params]
		...
		css = ["layout.css", "colors.css"]
		...

#### YAML example:

	params:
		...
		css: ["layout.css", "colors.css"]
		...

#### JSON example:

	"params": {
		...
		"css": ["layout.css", "colors.css"],
		...
	}

### Add Favicon
Add your sites favicon here:

	static/favicon.ico

### Create Menu
Add pages to the `main` menu.

## Features
 * CSS only designing
 * Menu with infinitive levels
 * Uses HTML 5 structural elements

## Contributing

Please clone this repository and create pull-requests for any features that could have a more general use and that fit within the vision of this theme.
