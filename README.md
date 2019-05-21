

Some notes

## Add or update a module

* TODO(bep) imports 

The following will add or update a module:

```bash
hugo mod get -u  github.com/bep/my-theme
```

## Update all modules

The following will update all modules to their latest minor or patch version:

```bash
hugo mod get -u
```

## Local development

Add a replace directive:

```bash
replace github.com/bep/hugotestmods/mypartials => /Users/bep/sites/hugomod/hugotestmods/mypartials
```

## Major versions

The simplest is to stick with v1 and increment minor and patch versions, e.g. `v1.0.0`, `v1.0.1`, `v1.1.0` and so on.

If you really need to release a new (breaking) major version, you can do this:

Edit your module's `go.mod` file and add the major version at the end of the path, e.g 

```
module github.com/bep/hugotestmods/myv2/v2
```

Then tag a new release version, e.g. `myv2/v2.0.0`.

**Note:** Hugo will currently only use one version of a given module (the first), so if you have a dependency that is depending on the `v1` version of that same module, but you really want to try out `v2`, then you must insert the `v2`-path higher up. The command `hugo mod graph` is useful in debugging these issues.

TODOS:

* More on v2
* GOPROXY="https://proxy.golang.org" seems to break/delay GitHub updates? 
* GO111MODULE=on 
