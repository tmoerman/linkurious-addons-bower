# linkurious-sigma-bower

A repository to add some custom [Linkurious](https://github.com/Linkurious/linkurious.js) add-ons (a.k.a. plugins) as a dependency with [Bower](https://bower.io/). This library contains new Linkurious plugins (not maintained by Linkurious) or modified versions of existing Linkurious plugins.

Companion repository to [linkurious-sigma-bower](https://github.com/tmoerman/linkurious-sigma-bower).

Also see [linkurious-plugins-bower](https://github.com/tmoerman/linkurious-plugins-bower).

#### Current add-ons:

* `customActiveState`

    Partially addresses [this Linkurious issue](https://github.com/Linkurious/linkurious.js/issues/370), but currently only supports immutable Sigma graphs. A `customActiveState` should be instantiated *after* the data is read into a Sigma graph, otherwise the indexes will not correctly reflect the data.
    
    Linkurious' activeState [attaches methods to the graph to keep indexes updated](https://github.com/Linkurious/linkurious.js/blob/develop/plugins/sigma.plugins.activeState/sigma.plugins.activeState.js#L52). `customActiveState` plugins omits this functionality, frankly because I haven't yet figured out how to fix this for multiple `activeState` instances. This explains why it is discouraged to use `customActiveState` with mutable graphs.

#### Installation
```
bower install --save linkurious-addons-bower
```

#### Disclaimer
This repository is not affiliated with Linkurious or Sigma.