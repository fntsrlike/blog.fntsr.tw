
- [δΈ­ζη](https://github.com/ethantw/Han/blob/master/README.md)
- <b>English version</b>


Han.css
=======

Han.css is a Sass/JavaScript typesetting framework featuring style normalisation to semantic elements, typography and advanced typesetting. Its elegant, standardised Hanzi (CJK) environment provides not only the legacy of reading convention but also the de facto specification in the digital. Han.css is the solution to Hanzi web design for the time being.

Han.css supports Traditional Chinese, Simplified Chinese and Japanese.

[View the test pages (zh) β]
(http://ethantw.github.io/Han/latest/)

## Installation
- NPM `npm install --save han-css`
- Bower `bower install --save Han`
- Component `component install ethantw/Han`
- Rails `gem install 'hanzi-rails'` ([Check out the details here](https://github.com/billy3321/hanzi-rails))

### Customisation
Han.css provides plenty of customisable features. By variable configuration or module import, it is easy to compile projects own style sheets. [Check out the manual (zh)][api] for detailed information.

[api]: http://css.hanzi.co/manual/sass-api

### Use of CDN
For high-speed downloads and cache, in need of customisation otherwise, you can use the CDN style sheets, JavaScript files and web fonts compiled by default configuration. The service [is hosted on cdnjs.com][cdnjs].

[cdnjs]: http://cdnjs.com/libraries/han

````html
<link rel="stylesheet" media="all" href="//cdnjs.cloudflare.com/ajax/libs/Han/3.1.1/han.min.css">
````

JavaScript,

````html
<script src="//cdnjs.cloudflare.com/ajax/libs/Han/3.1.1/han.min.js"></script>
````

Web fonts,

- WOFF `//cdnjs.cloudflare.com/ajax/libs/Han/3.1.1/font/han.woff`
- OTF `//cdnjs.cloudflare.com/ajax/libs/Han/3.1.1/font/han.otf`

## How to use

1. Include `han.min.css` before all other styles (or import it in Sass).
2. Include the script file, `han.min.js`, according to own requirements. Then add the class name `han-init` onto `<html>` tag to activate DOM-ready rendering.
3. Or, customise your own rendering routine. [Check out the manual][rendering] for further information.

[rendering]: http://css.hanzi.co/manual/js-api#rendering

### JavaScript is optional
Han.css is of low coupling and high semantics. Style sheets and JavaScript depend *little* on each other. Multi-level fallback can be applied within the style sheets, hence the optional use of the scripts.

## FAQ
### Issue of overwriting styles
Different from most of the CSS frameworks, Han.css contains numerous style correction aiming at the language attribute `:lang`. It may cause unexpected results such as style overwritting not carried out.

#### Element types with language-based style correction:
- <i>Text-level semantics</i>
- <i>Grouping content</i> and combining situations with <i>sections</i> **(font-family only)**
- The <i>root</i> element `html` **(font-family only)**

#### Solution
In order to handle these circumstances properly, please be well-alarmed with rules of style inheritance. It is recommended to add the corresponding language attribute, parental elements or other selectors, rather to overuse the `!important` declaration for maintainability.

Use the βDOM Inspectorβ in browsers to observe the inheritance and overwritten relations of style sheets while in need.

### Working environments
Han.js runs in DOM environments only. Introduce modules such as [jsdom] for server-side usage.

[jsdom]: https://github.com/tmpvar/jsdom

## Browser support

- Google Chrome (latest)
- Mozilla Firefox (latest)
- Opera Next (latest)
- Apple Safari 7+
- Internet Explorer 10+

## Development
Contributions are pretty much welcomed. Below goes the list with some useful developing commands:

- Install dev-dependencies: `sudo npm i`
- Start the dev-environment: `npm start` or `gulp dev` (including local server running and auto compiling)
- Compile the distribution files: `gulp build`
- Test `han.js`βs API: `gulp test` (PhantomJS)
- Update dependencies: `npm update && gulp dep`

* * *
Han.css v3.1.1  
Last-modified: 2015-3-14 01:47 (GMT+8)
