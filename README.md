# ngen-ngen

`ngen` is a tool that will generate a new nodejs project
  for you. It includes best practices around the structure of
  your README and package.json

## Usage

`ngen [name] [description] [flags]`

See [usage.md][usage] for more documentation

## Example

You can use `ngen` in three modes.

Run `ngen` and then fill in the two fields for name & description.
Run `ngen {{name}}` and then fill in the field for description
Run `ngen {{name}} {{description}}` and fill in no fields.

`ngen` will generate a folder that is called `{{name}}` in your CWD.

## Templates

### Uber

Currently the only available template, creating the following 
  structure populated with content after the following questions 
  are asked from the cli:

     Project Name: ngen
     Project description: A cool scaffolder

structure:
 
     ./test/index.js
     ./.jshintignore
     ./.gitignore
     ./.jshintrc
     ./index.js
     ./package.json
     ./README.md
     ./LICENSE

## Docs

`ngen` can also be called directly

```js
var Template = require('ngen')

var t = Template('name-of-template', {
  templates: 'folder location of templates'
})
t.init('target location to write on disk', function (err) {
  // scaffolded the template to the location
  // calling init() will prompt on STDIN.
})
```

## MIT Licenced

  [usage]: https://github.com/uber/ngen/tree/master/bin/usage.md



