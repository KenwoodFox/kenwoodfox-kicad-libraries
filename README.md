# Kenwood's Custom KiCAD libraries

I really liked the way ![Espressif](https://github.com/espressif/kicad-libraries) laid their library out, it made it
easy to add as a submodule. I tried to use a similar format to theirs.

I hope you find these parts helpful!

Just:

```
git submodule add https://github.com/KenwoodFox/kenwoodfox-kicad-libraries
```

Just like the espressif library, if you want 3D models, you'll need to
open `Preferences` and `Configure Paths` then add the following enviorment variable:

```
Name: KENWOODFOX_3DMODELS
Path: <Path to folder>
```

And if you use kibot, add this to your `pre_flight`

```
preflight:
  ...
  set_text_variables:
    - name: "KENWOODFOX_3DMODELS" # 3D models for KenwoodFox Library
      command: "echo 'Hardware/Board/Libraries/kenwoodfox-kicad-libraries/3d'"
```

# Projects using this lib:

https://github.com/KenwoodFox/APRN-pi
