#PostCSS

##What is PostCSS?
[PostCSS](https://github.com/postcss/postcss) is meant to help create a lean development environment. It does this by adding CSS development tools modularly.

For example we use the following:
- Nesting
- Variables
- Importing other CSS files into one central CSS file
- Autoprefixer

These are only a fraction of the problems PostCSS plugins can solve. Take a look at [http://postcss.parts](http://postcss.parts/), you will see the wide range of plugins that can solve many problems.

The awesome people at DockYard and have combined them into a package called [narwin-pack](https://github.com/cirroweb/narwin-pack). Having one package that we maintain provides an easy way for the team to use the same development tools within PostCSS. If we find any new plugins we need in our projects we will add it to narwin-pack.

To learn about the plugins we choose to use in narwin-pack read through the narwin-pack slides at [http://ctannerweb.github.io/talks/narwin-pack/](http://ctannerweb.github.io/talks/narwin-pack/).

To get a grasp on how to use PostCSS use the steps below to add PostCSS and narwin-pack to an Ember project.

##How to install
###Add PostCSS to your project

```shell
$npm install --save ember-cli-postcss
```

###Add narwin-pack

```shell
$npm install --save narwin-pack
```

Add PostCSS to the `ember-cli-build.js` file on the root of the Ember project.

```js
var app = new EmberApp(defaults, {
  postcssOptions: {
    plugins: [
      {
        module: require('narwin-pack')
      }
    ]
  }
});
```

If you want to add another plugin to your project go over it with the team and the new plugin can always be added to narwin-pack.

##Further reading
- [PostCSS Deep Dive](http://webdesign.tutsplus.com/series/postcss-deep-dive--cms-889)
