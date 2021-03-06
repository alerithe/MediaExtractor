# socialrip
Extracts media from social platforms and attempts to open them in new tabs.

## Currently supported Platforms:
* [Instagram](https://instagram.com/) (posts, stories, reels, and IGTV)
* [TikTok](https://tiktok.com/)
* [Twitter](https://twitter.com/) (photos only)
* [VSCO](https://vsco.co/)

## Use as a UserScript
To run from a UserScript extension such as Tampermonkey or Greasemonkey, append the following to the script's headers:
```javascript
// @include *://*instagram.com/*
// @include *://*tiktok.com/*/video/*
// @include *://*tiktok.com/v/*
// @include *://*twitter.com/*/status/*
// @include *://*vsco.co/*/media/*
```
Make the script's source code the content of [`index.js`](https://github.com/alerithe/socialrip/blob/master/index.js).

## Use as an executable Bookmark
Save the following code block as a bookmark to run it from your Bookmarks toolbar
```javascript
javascript:(function(){let s=document.createElement('script');s.type='text/javascript';s.src='https://alerithe.github.io/socialrip/index.js';document.head.appendChild(s);})();
```
Note: This bookmarklet will not always work due to `Content Security Policies`. My recommendation is `javascript:` preceding a minified version of [`index.js`](https://github.com/alerithe/socialrip/blob/master/index.js).
