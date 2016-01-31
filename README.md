
quaint-sass
===========

[Quaint](http://breuleux.github.io/quaint)
plugin for [SASS](http://sass-lang.com/).

Allows `.sass` and `.scss` files to be required as resources, as well
as inline sass/scss code in markup. Common variables and functions may
also be included in configuration.


## Install

    quaint --setup sass


## Sample configuration

This configuration entry must be added in the `plugins` section of
`quaint.json`:

```json
"sass": {
  "sassDefinitions": "@function double($x)\n  @return $x * 2"
  "variables": {
    "width-body": "100px",
    "width-side": "double($width-body)"
  }
}
```


## Resources

With this plugin, you can include SASS/SCSS files as resources, for
instance:

```
resources ::
  style.sass
```

The files will be compiled and saved in CSS format.


## Inline styles

`quaint-sass` provides the `sass` and `scss` macros which you can use
to inline SASS or SCSS:

```quaint
sass ::
  #post
    color: blue
    background: red
    .author
      color: green

#post %
  .author % ME
  Hello this is a post! I have horrible taste in color!
```

Or:

```quaint
scss ::
  #post {
    color: blue;
    background: red;
    .author {
      color: green;
    }
  }
```


## Options

### `sassDefinitions` and `scssDefinitions`

The contents of that string will be inserted before every `.sass` or
`.scss` file imported, and also before every inline `sass` or `scss`
directive.

### `variables`

This is a map of variable name to value. The variables will be
available in every `.sass` or `.scss` file, and in every inline `sass`
or `scss` directive.


