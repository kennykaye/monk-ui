Monk UI
=======

UI theme built on [Bootstrap for Sass](https://github.com/twbs/bootstrap-sass).

The **master** version of this repository is set to **v3.3.1** of Bootstrap.

Usage
-----

```ruby
gem 'bootstrap-sass', github: 'MonkDev/monk-ui', branch: 'master'
```

```sass
@import "bootstrap-sprockets";
@import "your/application/variables";
@import "monk-ui";
@import "your/application";
```

Development
-----------

To ease the merging in of upstream changes from Bootstrap, Monk UI does not
alter any existing files. Instead, all customizations and overrides are done in
separate files within `assets/stylesheets/monk-ui`. These files are then
imported with Bootstrap files in `assets/stylesheets/_monk-ui.scss`.

Be sure to [configure Bundler to work against a local checkout](http://bundler.io/v1.7/git.html#local)
of this repository during development.

### Updating Bootstrap

The Bootstrap version can be updated by merging in upstream changes.

Start by setting the upstream:

```bash
$ git remote add upstream https://github.com/twbs/bootstrap-sass
```

Then merge in the desired release version to `master`:

```bash
$ git fetch upstream
$ git checkout master
$ git merge vX.Y.Z
```

It's important to merge in a specific release version tag and not `master` or
any other unstable branch/tag/commit. Test the changes in an app that uses Monk
UI to ensure everything still works.

Finally, push the changes:

```bash
$ git push origin master --tags
```
