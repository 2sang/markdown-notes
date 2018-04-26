parcel notes
------------

#### Keep complaining 'cannot read __ES6module ...' 
Every time I build project triggered by writing files, parcel console keep complains
above error message, and it turned out a bug, .babelrc file should be
separated with package.json file, like this.
```bash
# in package.json
"babel": {
    "presets": [
        "stage-3",
        "react-hmre",
        "react"
    ]
}
```
to separate .babelrc file
```bash
# in .babelrc
{
    "presets": [
        "stage-3",
        "react-hmre",
        "react"
    ]
}
```



