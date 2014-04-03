# Style Prototype

A style prototype is a single HTML page which outlines site colors, typography, photographic style, button styles, rollovers, and other necessary elements to establish design direction. In a sense, it is a safety measure intended to avoid rehashing (or completely scrapping) site designs in which hours of time and budget have been invested.

Samantha Warren introduced us to the great idea of presenting designed web elements to clients before creating full site comps. She refers to her Photoshop-based creations as [Style Tiles](http://styletil.es), and they contain most of the same elements that a Style Prototype typically would. However, a Style Prototype takes things one step further into the medium of the web. Rather than present the client a JPG of your Photoshop document, show them a responsive HTML/CSS Style Prototype instead.

[See it in action here.](http://sparkbox.github.com/style-prototype/)

## Building the project:

1. Clone the repo with the Git app for [Mac](https://mac.github.com/) or [Windows](https://windows.github.com/)
2. Compile the Sass to CSS with [Codekit](https://incident57.com/codekit/) (paid, Mac), [Prepros](http://alphapixels.com/prepros/) (paid, Mac and Windows), or [Scout](http://mhs.github.io/scout-app/) (free, Mac and Windows)
3. Open `index.html` in your browser

## Building the project in your terminal:

1. Clone the repo: `git clone https://github.com/sparkbox/style-prototype.git`
2. Install Sass: `gem install sass`
3. Compile Sass: `mkdir css && sass sass/base.scss css/base.css && sass sass/fallback.scss css/fallback.css`
4. Open `index.html` in your browser

## Don't want to build the project?

Fine. We won't hold it against you! Download the project with Sass already compiled [here](https://github.com/sparkbox/style-prototype/releases). Just download the latest .zip release, and open `index.html` in your browser.

But you should probably consider [learning Sass](http://sass-lang.com/guide). Just sayin'! Want a deeper dive? Check out one of [our workshops](http://buildright.io/).