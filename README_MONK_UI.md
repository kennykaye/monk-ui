Monk UI
=======

UI theme for [MonkDev](http://monkdev.com) apps built on [Bootstrap for Sass](https://github.com/twbs/bootstrap-sass).

Usage
-----

```ruby
gem 'bootstrap-sass', :github => 'MonkDev/monk-ui', :branch => 'master'
```

```sass
@import "monk-ui";
```

Development
-----------

To ease the merging in of upstream changes from Bootstrap, Monk UI does not
alter any existing files. Instead, all customizations and overrides are done in
separate files within `vendor/assets/stylesheets/monk-ui`. These files are then
imported with Bootstrap files in `vendor/assets/stylesheets/monk-ui.scss`.

Be sure to [configure Bundler to work against a local checkout](http://bundler.io/v1.5/git.html#local)
of this repository during development.
