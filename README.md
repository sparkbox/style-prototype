# [HTML5 Boilerplate](http://html5boilerplate.com)

HTML5 Boilerplate is a professional front-end template that helps you build fast, robust, adaptable, and future-proof websites. Spend more time developing and less time reinventing the wheel.

This project is the product of many years of iterative development and combined community knowledge. It does not impose a specific development philosophy or framework, so you're free to architect your code in the way that you want.


## How to Build

1. Open "Terminal"
2. Next, simply type: ant build
3. Now, look in your project folder and see that there is a newly created "publish" directory within your project. Inside, you will find your minified CSS, JS and along with duplicates of the files from your original directory. This new set of files within "publish" is your production code.

## Build Options

**ant build**     # minor html optimizations (extra quotes removed). inline script/style minified (default)

**ant buildkit**  # all html whitespace retained. inline script/style minified

**ant basics**    # same as build minus the basic html minfication

**ant minify**    # same as build plus full html minification

**ant text**      # same as build but without image (png/jpg) optimizing


## Environments

**dev** - Increases build number, cleans and copies the build and optimises any images if the target originally did

**test** - Runs everything that the original target did, however it does not strip the console.log or profiling parts

**prod (default)** - Runs everything the original target did

To run it you simply use ant <target> -Denv=<environment>

ant build -Denv=dev


## Wordpress integration

Check out Jay George's wordpress screencast videos: http://www.jaygeorge.co.uk/1-html5-buildscript-wordpress-1/

Using the build script on a Wordpress theme introduces a significant problem: Wordpress themes are installed to a website's /wp-content/themes/<theme-name> directory while the build script's output references the minified/concatenated files in a relative URI as js/scripts-xxxx.min.js. Therefore, output of the build script will reference files in the wrong location.

To make the build script output files that reference the correct url /wp-content/themes/<theme-name>/js/scripts-xxxx.js, the build.xml file must be modified. Edit the 2 regular expressions near lines 599 (for js) and 699 (for css) to include the Wordpress PHP that dynamically references the theme's folder: (the line to add is indented)

<replaceregexp match="&lt;!-- scripts concatenated [\d\w\s\W]*?!-- 
end ((scripts)|(concatenated and minified scripts))--&gt;" 
replace="&lt;script src='
    &lt;?php bloginfo('template_url'); ?&gt;/
${dir.js}/scripts-${build.number}.min.js\'&gt;&lt;/script&gt;" flags="m">


## Anything Else

[Build Script Docs](http://html5boilerplate.com/docs/Build-script/)
