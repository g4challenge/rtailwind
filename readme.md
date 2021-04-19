# rtailwind

integrate [tailwindcss]() with R.


This package uses [Postcss-modules](https://github.com/madyankin/postcss-modules)


Transform your HTML bookdown output to complete tailwindcss

### Inspiration

This project is similar to tachyons

xaringanExtra::use_tachyons()
htmltools::htmlDependency(
    name = "tachyons",
    version = tachyons_version,
    package = "xaringanExtra",
    src = "jslib/tachyons",
    stylesheet = paste0("tachyons", if (minified) ".min", ".css"),
    all_files = FALSE
  )
  
htmltools::tagList(
    html_dependency_tachyons(minified)
  )


## Prerequisites
Node.js installed


```
npm install --save posthtml posthtml-css-modules
```

```
var fs = require("fs");
var posthtml = require("posthtml");
var posthtmlCssModules = require("posthtml-css-modules");
var template = fs.readFileSync("./about.html", "utf8");

posthtml([posthtmlCssModules("./cssModules.json")]).process(template).then(function (result) {
    console.log(result.html);
  });
```
