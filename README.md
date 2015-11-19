# git-nm
Gitify Node Modules

## What problem does this solve?

This is an alternative to `npm link`. Running this will crawl your tree of node modules, turning modules that you own into git repositories, checked out to the same commit that you published to npm. This is sort of a hacky way to develop, but super useful if you can't `npm link` for some reason.

## Installation
```bs
npm install -g git-nm
```

## Usage
```bs
git-nm pwmckenna rackt ...
```

Now just navigate into those dependency directories and commit away!
```bs
cd node_modules/my_other_node_module
rm -rf .
git commit -a -m "This module has too many files in it"
git push -f
```

## Logging
Want more info?
DEBUG=* git-nm [organization]
