# testraylib

## Setup Directions

Delete the raylib directory in external

Then run this:
```git submodule deinit external/raylib
git rm external/raylib
rm -rf .git/modules/external/raylib
git submodule add https://github.com/raysan5/raylib.git external/raylib
```
