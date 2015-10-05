
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

```quaint
plugin sass ::
  indentedSyntax = true

sass ::
  #post
    color: blue
    background: red
    .article
      color: green
```


## Options

### `indentedSyntax`

Default: false

Whether to use the indent-based syntax or not.

