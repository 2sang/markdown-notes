parcel notes
------------

#### Keep complaining 'cannot read __ES6module ...' When write to files
[Parcel-bundler github issue](https://github.com/parcel-bundler/parcel/issues/927)  
Every time I build project triggered by writing files, parcel console keep complains
above error message, and it turned out a tiny bug. .babelrc file should be placed
separately with package.json file, like this.  
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



