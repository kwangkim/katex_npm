# `math/tex` Custom Script Type Extension

This is an extension to automatically display code inside `script` tags with `type=math/tex` using KaTeX.
This script type is commonly used by MathJax, so this can be used to support compatibility with MathJax.

### Usage

This extension isn't part of KaTeX proper, so the script should be separately
included in the page, in addition to KaTeX.

Load the extension by adding the following line to your HTML file.
This extension should be loaded *after* all `script type=math/tex` blocks that you want to render.

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.9.0-alpha/contrib/mathtex-script-type.min.js" integrity="sha384-ZczMDLnJco4ux56ynOlucmSH4zomXiztaTOG16jaFnYLKtlq1ks4E015DkR9g5Ub"></script>
```
Note that if the URL above contains `...` in-place of a version string, then this script has not yet
been deployed to the CDN.
You can download the script and use it locally, or from a local KaTeX installation instead.

For example, in the following simple page, we first load KaTeX as usual.
Then, in the body, we use a `math/tex` script to typeset the equation `x+\sqrt{1-x^2}`.
After we're done writing `math/tex` scripts, we load this extension.

```html
<html>
   <head>
       <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.9.0-alpha/katex.min.css" integrity="sha384-FkMHIpkXHDi3o2XSOOa5/9TpXg4AX4DXPSC6z28hi2Eqn/27ea8MTV18rTq9OyQR" crossorigin="anonymous">
       <script src="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.9.0-alpha/katex.min.js" integrity="sha384-wt0V9VomB0kx/jgLEkR18Slo+aNALuRwOOrWkicjQ0HHpFqu0JKzaFkbtmsku5a/" crossorigin="anonymous"></script>
   </head>
   <body>
      <script type="math/tex">x+\sqrt{1-x^2}</script>
      <script src="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.9.0-alpha/contrib/mathtex-script-type.min.js" integrity="sha384-o+v+EkJWQmZj7XwHBxehTGJKE18182WyyN2glZMTPw9g5XxjN1uwrquNuMX/NJiF"></script>
   </body>
</html>
```
