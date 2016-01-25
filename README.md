
quaint-sass
===========

Allows inline
[SASS](http://sass-lang.com/)
code in
[Quaint](http://breuleux.github.io/quaint)
markup.


## Install

    quaint --setup sass


## Sample configuration

This configuration entry must be added in the `plugins` section of
`quaint.json`:

```json
"sass": {
  "indentedSyntax": true
}
```


## Usage

`quaint-sass` provides the `sass` macro which you can use to inline
SASS or SCSS.

Using the sample configuration above:

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


## Options

### `indentedSyntax`

Default: false

Whether to use the indent-based syntax or not.

