# Living Lab site

[![Build Status](https://travis-ci.com/uwasystemhealth/livinglab-site.svg?branch=master)](https://travis-ci.com/uwasystemhealth/livinglab-site)

#### [uwasystemhealth.github.io/livinglab-site/](https://uwasystemhealth.github.io/livinglab-site/)

This is a static one-pager that is compiled using hugo, and hosted on Github pages

Hugo is a static website generator that is built of golang, is super fast and simple to put together using markdown.
The current theme being used is [Dimension](https://themes.gohugo.io/dimension/)

## Builing the site

### Initial

1. [install hugo](https://gohugo.io/getting-started/installing/) (if using 64-bit linux, you can just use `$ ./bin/hugo` instead)
2. get the repo `$ git clone https://github.com/uwasystemhealth/livinglab-site.git && cd livinglab-site`
3. install the theme:
  ```
$ git submodule init
$ git submodule update
  ```

### Testing

To run a local server to view the website you can run the following:
```
$ hugo server -D
```
The flag `-D` will load in pages marked as draft, remove that flag to see what the final website will look like.

Any saved changes made to the website will automagically recompile and the preview in your browser will auto-refresh.

### Deploy changes

Any changes made to the master branch will automagically be compiled and deployed using travis-ci. All you need to do is commit and push your changes:

```
$ git commit -a -m "Message about what you changed"
$ git push
```
