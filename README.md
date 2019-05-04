

Some notes

## Add or update a module

* TODO(bep) imports 

The following will add or update a module:

```bash
go get -u  github.com/bep/my-theme
```

## Update all modules

The following will update all modules to their latest minor or patch version:

```bash
go get -u
```

## Local development

Add a replace directive:

```bash
replace github.com/bep/hugotestmods/mypartials => /Users/bep/sites/hugomod/hugotestmods/mypartials
```


TODOS:

*  GOPROXY="https://proxy.golang.org" seems to break/delay GitHub updates? 
* GO111MODULE=on 
