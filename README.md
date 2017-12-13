# Demonstrating an issue with Electron Builders Auto-Update

The prerequisites for this issue:
1. package.json should have a `productName` field.
2. package.json should have two elements in the publish list: S3 and GitHub.

Steps to reproduce:
1. Install the package `npm install`
2. Run the electron builder `npm run package`
3. Open the `dist/latest-mac.yml` to find that it references files that does not exist:

```
version: 0.1.0
files:
  - url: electron-builder-auto-updating-issue-0.1.0-mac.zip
    sha512: uterlc7srauyxZ42Uze1bgltL0WSeVsY2s23EhVs9KZ8dwtbk5e/vjEauiR0dZ/GtVWmPLaLbGBspefn9XwgBg==
  - url: electron-builder-auto-updating-issue-0.1.0.dmg
    sha512: WWjjRBfuZBLnjyQkL42Z5gSurnq0yO4mzs8a+/dDODgtMCPvY3ajTVTJrSh4P6J22mSpx+Rz+WSn52mO3Vc+gA==
    size: 46763411
path: Electron Builder Auto Updating Issue-0.1.0-mac.zip
sha512: uterlc7srauyxZ42Uze1bgltL0WSeVsY2s23EhVs9KZ8dwtbk5e/vjEauiR0dZ/GtVWmPLaLbGBspefn9XwgBg==
releaseDate: '2017-12-13T12:13:44.418Z'
```
