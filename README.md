# Package Hub
> An extension for displaying dependencies for different package managers on GitHub

![](screenshot.png)

### Package Manager Support
- [x] Npm.
- [x] Composer (incomplete).
- [ ] Cargo.
- [ ] Yarn.
- [ ] Pip.

### Rationale
Why build this? We already have [npmhub](https://github.com/npmhub/npmhub)?
> npmhub is great, but why should npm have all the fun?
I wanted to see if I could implement something similar while making it easy to
add support for other package managers.
Also, to make it more fun, I decided to accomplish this without any fancy libraries (jQuery) or apis (fetch). So, packagehub should have support for most browsers in use today.

### Todo
- [ ] Design extension logo.

## Related
* [npmhub](https://github.com/npmhub/npmhub) - inspired the idea for this extension.

## Installation

[![Install from chrome web store](https://developer.chrome.com/webstore/images/ChromeWebStore_Badge_v2_340x96.png)](https://chrome.google.com/webstore/detail/package-hub/hnnjnbmjanpeoeapjllonejjgoonilal)

Install extension from [Chrome Web Store](https://chrome.google.com/webstore/detail/package-hub/hnnjnbmjanpeoeapjllonejjgoonilal)

## Development

1. Clone this repo.
2. Go to chrome extensions [chrome://extensions](chrome://extensions).
3. Enable developer mode.
4. Click on load unpacked extension and select the source folder of this cloned repo.

To add support for a new package manager

1. Add a new [config](src/config.js) entry with the relevant details.
2. Add a new [parser](src/parser.js) if the package manager dependencies are not specified in JSON.
3. Add a new [registry](src/registry.js) function to retrieve extra details of the package. This function should provide `latest-version`, `description`, and `repository` as arguments to the callback.


## License
MIT © Ezinwa Okpoechi
