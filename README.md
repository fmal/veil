veil
====

veil is a very simple boilerplate for writing static sites.

It uses [Jade](http://jade-lang.com/) for templating,
[Stylus](http://learnboost.github.io/stylus/) for CSS generation and [GNU
Make](https://www.gnu.org/software/make/) for the build system.

Install
-------

``` console
# Create your project directory
$ mkdir my-website; cd my-website

# Download the Makefile
$ wget https://raw.github.com/madx/veil/master/Makefile

# Launch the setup task
$ make setup
```

Usage
-----

Run `make` to build the site.

- Pages are written with Jade and stored in `sources/pages/`. They will map to
  a file in your output dir (i.e. `sources/pages/index.jade` →
  `output/index.html`).
- Stylesheets are written with Stylus and stored in `sources/stylesheets/`.
  They will map to a file in the `assets/css/` folder of your output dir (i.e.
  `sources/stylesheets/styles.styl` → `output/assets/css/styles.css`).
- Static assets from the `static/` folder will be copied in the `assets/`
  folder of your output dir, preserving subdirectories (i.e. `static/js/app.js`
  → `output/assets/js/app.js`).

### watch

Provided you have installed either [inotify-tools](inotifytools) (Linux) or
[fswatch](fswatch) (OS X), you can use the `watch` task to continuously rebuild
the site as you modify the source files.

``` console
$ make watch
```

[inotifytools]: https://github.com/rvoicilas/inotify-tools
[fswatch]: https://github.com/alandipert/fswatch
