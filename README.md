<div  align="center">
<img src="images/logo.svg" alt="logo" align="center" style="width:200px; height:200px; margin-top:50px;"/>
<h1>iconThai</h1>
<h3>A premium open source Thai style font-icon, designed for everyone.</h3></div>
<div align="center">
  <!-- NPM Version -->
  <a href="https://badge.fury.io/js/mole-fetch">
    <img src="https://badge.fury.io/js/mole-fetch.svg" alt="npm version" />
  </a>
  <!-- Release -->
  <a href="https://github.com/jukbot/smart-industry/releases/">
    <img src="https://img.shields.io/github/release/jukbot/smart-industry/all.svg" alt="npm version" />
  </a>
  <!-- Download -->
  <a href="https://www.npmjs.com/package/mole-fetch">
    <img src="http://img.shields.io/npm/dm/mole-fetch.svg" alt="Downloads" />
  </a>
  <!-- Quality -->
  <a href="http://packagequality.com/#?package=mole-fetch">
    <img src="http://npm.packagequality.com/shield/mole-fetch.svg" alt="Package Quality" />
  </a>
    <!-- License -->
  <a href="https://opensource.org/licenses/Apache-2.0">
    <img src="https://img.shields.io/badge/License-Apache%202.0-green.svg" alt="Package Quality" />
  </a>
</div>
<br />


## Installation
```
npm install icon-thai --save
```

## Example Usage

### HTML file
```javascript
const moleFetch = new MoleFetch()

function fetchFacebook() {
    //Call sendRequest for request HTTP
    moleFetch.sendRequest('facebook', 'http://localhost:5555/mock-api/online', false, 'GET')
}

// Register Service Wokers
if ('serviceWorker' in navigator && 'SyncManager' in window) {
    navigator.serviceWorker.register("sw.js").then((registration) => {
        console.log('Service Workers registration successful with scope: ', registration.scope)
    }).catch(function(err) {
        console.error('Service Workers registration failed: ', err)
    })
}

// Implement onResponse for recieve response from ServiceWorker when site is online
moleFetch.onResponse('facebook').then((value) => {
    document.getElementById("result").innerHTML = value;
})

// Implement onResponse for recieve response from Cache when site is offline
moleFetch.getCacheResponse('facebook',false).then((value) => {
    document.getElementById("result").innerHTML = value;
})
```


## Browser Supported

| [<img src="https://cdn.rawgit.com/alrra/browser-logos/f50d4cc8/src/edge/edge.png" alt="IE / Edge" width="64px" height="64px" />](http://caniuse.com/#feat=fetch)</br>Edge | [<img src="https://cdn.rawgit.com/alrra/browser-logos/f50d4cc8/src/firefox/firefox.png" alt="Firefox" width="64px" height="64px" />](http://caniuse.com/#feat=fetch)</br>Firefox | [<img src="https://cdn.rawgit.com/alrra/browser-logos/f50d4cc8/src/chrome/chrome.png" alt="Chrome" width="64px" height="64px" />](http://caniuse.com/#feat=fetch)</br>Chrome | [<img src="https://cdn.rawgit.com/alrra/browser-logos/f50d4cc8/src/safari/safari.png" alt="Safari" width="64px" height="64px" />](http://caniuse.com/#feat=fetch)</br>Safari | [<img src="https://cdn.rawgit.com/alrra/browser-logos/f50d4cc8/src/opera/opera.png" alt="Opera" width="64px" height="64px" />](http://caniuse.com/#feat=fetch)</br>Opera | 
| ---------: | ---------: | ---------: | ---------: | ---------:
| 15+ (Flag) | 55+ | 49+ | 10.1+ | 47+


## Contribution

If you’ve found an error in this library, please file an issue at: https://github.com/Nutn0n/iconThai/issues

Patches are encouraged, and may be submitted by forking this project and submitting a pull request through GitHub.


## License

Copyright 2015-2017 Nattanon.

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
