## Encore.js

# No longer being maintained

3 other projects are used as modules in this project, and you have to use `npm link` to include them, if you want to get this project running. The projects you need to clone are rm-rf-etc/runway, rm-rf-etc/typeof, and rm-rf-etc/connected. The following steps should get things working for you.
```
$ cd ~/projects/typeof
$ npm link
$ cd ~/projects/runway
$ npm install
$ npm link typeof
$ npm link
$ cd ~/projects/connected
$ npm install
$ npm link typeof
$ npm link
$ cd ~/projects/encore
$ npm link typeof runway connected
$ npm link
```
You should now be able to use `npm link encore` in your project directory to symlink encore in your `node_modules`. My encore-docs-site provides an example working site. github.com/rm-rf-etc/encore-docs-site


[![NPM](https://nodei.co/npm/encore.png?compact=true)](https://nodei.co/npm/encore/)

This is an MVC framework for node.js that I'm building. I've authored 3 modules specifically for this project,
and you can find them on npm and github:  

* Runway - the router  
* FileFetcher - project file loader  
* Easyioc - inversion of control module  

Current Features List:

* Inversion of control dependency loading  
* Cleanest routing syntax ever
* Route groups  
* Route wildcards  
* RESTful controllers  
* Filters on routes or controllers  
* View templating _(any 3rd party templating library)_  
* Performance optimized view rendering  
* Flexible recursive project loading

For examples, please visit:  
http://encore.jit.su

More coming soon.

## License

The MIT License (MIT)

Copyright (c) 2013 Rob Christian

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
