parcel notes
------------

#### What is parcel? - [Parceljs.org docs](https://parceljs.org/getting_started.html)
Parcel is a web application bundler, just like Webpack. 
to install parcel using yarn:
```bash
# add parcel-bundler
yarn add parcel-bundler
# Configurable using pacakge.json file by yarn, but no specific configuration needed at first time.
yarn init -y
# Run parcel
yarn run parcel index.html
yarn run watch index.html
# Build for production
yarn run build entry.js
```
And also in dev or production, you may want to alias those commands using yarn script.


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



