# termux-core-package

The [`termux-core`](https://github.com/termux/termux-core-package) package
provides utilities and libraries required for the basic functionality of Termux.
It is part of every bootstrap package, and forks of Termux will need to provide
forks of this package, too. Major components of this package include:

// list deliberately not exhaustive

* **[termux-exec](/something/sensible.md)**: Binary execution helper required
  to `exec` any file that isn't part of an `apk` on Android 10 and later (see
  [W^X discussion](/you/know/the/one/issue). Also provides implicit shebang
  rewriting to allow unmodified scripts (see [Differences from
  Linux#FHS](/we/should/rewrite/those/too)).
* **[termux-settings](/something/relevant.md)**: Script to get and set
  configuration of Termux's terminal emulator and execution environment.

## Building

The best way to develop this package is within the
[`termux-packages`](/termux/termux-packages) environment. Set that up by
following the instructions [here](/don't/think/this/exists) and then, in the
root of your `termux-packages` clone:

// whatever works today, to unblock the next person who needs it
* scripts/run-docker.sh ./build-package.sh termux-core
* docker cp ... /tmp/termux-core.dpkg

## Testing

// is there currently any defined testing for the overall package, as opposed to
the programs it contains? skip the whole section if not

## Contributing

See [the main Termux contributing doc](/goes/somewhere/).

[](TOC and Project deliberately removed)
