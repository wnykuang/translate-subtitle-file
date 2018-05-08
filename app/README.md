# Readme (for developer)
I put all file into `app/`   
just want the folder structure look more clean.   


## 为什么 commit 那么少
因为我想整理文件夹，把所有文件扔进了 `app/`，     
因为大部分访问这个 git 库的人是用户，而不是开发者。顶部少占点空间 README 就在上面一点。      
智商感人，整理的时候不小心把 node_modules 也提交上去了。        
后面又要删，git push 70多 M 的文件，我一烦就重置了 git log      
所以就这样了，所以 commit 那么少     

## Version
* 0.0.1 release at 2018-5-8 (for Windows and macOS)

## Tech Stack
* Electron (v2.0.0)
* jQuery (v3.3.1)
* Vue (v2.5.13)

## Run
```
git clone https://github.com/1c7/translate-subtitle-file.git ~/Desktop/translate-subtitle-file
cd ~/Desktop/translate-subtitle-file
electron .
```

## Release 如何打包
### for macOS      
```bash
  npm run dist
```
output file in `dist/`        

### for Windows
```
  electron-packager .
```
because somehow `electron-builder` not working on Windows, so we use `electron-packager`

Note: in `package.json`, some config are for `electron-builder`


### Translate Service Provider: Google
there are only 3 Translate API: Google/Microsort/Yandex

### Google doesn't have free quote:
FAQ: https://cloud.google.com/translate/faq?hl=en#pricing
> Is there any free quota?         
> No, the Google Cloud Translation API is only available as a paid service. Please see Pricing for more details.

### Tried
tried `google-translate-api` on Github, it's a node.js module or something, not working.      

### Third Party Lib
eush77/ass-parser    https://github.com/eush77/ass-parser
eush77/ass-stringify https://github.com/eush77/ass-stringify

### Testing
`test file/` folder have file to test.         
because trasnlation is not the same everytime, it can only test by hand         