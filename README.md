
quaint-sass
===========

Allows inline
[SASS](http://sass-lang.com/)
code in
[Quaint](http://breuleux.github.io/quaint)
markup.

## Usage

### Command-line

```bash
$ npm install quaint-sass
$ quaint -p sass file.q
$ quaint -p 'sass{"indentedSyntax": true}' file.q
```


### Quaint

`quaint-sass` provides the `sass` macro which you can use to inline
SASS or SCSS.

```quaint
plugin sass ::
  indentedSyntax = true

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

