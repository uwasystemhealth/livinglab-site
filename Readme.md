# Living Lab site

(uwasystemhealth.github.io/livinglab-site)[https://uwasystemhealth.github.io/livinglab-site/]

This is a static one-pager that is compiled using hugo, and hosted on Github pages

Hugo is a static website generator that is built of golang, is super fast and simple to put together using markdown.
The current theme being used is [Dimension](https://themes.gohugo.io/dimension/)

## Builing the site

### Initial

1. [install hugo](https://gohugo.io/getting-started/installing/)
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

### Building

Once happy with the changed site, you need to compile the website into static html.

```
$ hugo -d docs
```

This will compile and save the files to the docs folder. Github pages will display the contents of the docs folder.

*Bug Fix* Until the domain is pointing at the website, the absolute references break the website, to fix it, run this command before commiting the changes:
```
$ sed -i 's/href="\//href="/g' docs/index.html && sed -i 's/src="\//src="/g' docs/index.html && sed -i 's/url("\//url("/g' docs/css/main.css
```

Commit and push your changes.

```
$ git commit -a -m "Message about what you changed"
$ git push
```
