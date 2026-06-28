# Chrome Extensions samples

Official samples for Chrome Extensions and the Chrome Apps platform. (Chrome Apps are deprecated. Learn more [on the Chromium blog](https://blog.chromium.org/2020/08/changes-to-chrome-app-support-timeline.html)).

For more information on extensions, see [Chrome Developers](https://developer.chrome.com).

## Explore samples

The directory structure is as follows:

- [api-samples/](api-samples/) - extensions focused on a single API package
- [functional-samples/](functional-samples/) - full featured extensions spanning multiple API packages
- [\_archive/apps/](_archive/apps/) - deprecated Chrome Apps platform (not listed below)
- [\_archive/mv2/](_archive/mv2/) - resources for manifest version 2

You can also use the [Samples](https://developer.chrome.com/docs/extensions/samples/) page to discover extensions by type, permissions, and extension API.

## Installation

To experiment with these samples, clone this repo and load a sample as an unpacked extension:

1. Clone the repository: `git clone https://github.com/GoogleChrome/chrome-extensions-samples.git`
2. Open `chrome://extensions` in Chrome.
3. Enable **Developer mode** using the toggle in the top-right corner.
4. Click **Load unpacked** and select the directory of the sample you want to try (the folder containing its `manifest.json`).

Some samples require a build step or dependency installation first — check the sample's own `README.md` for any extra instructions.

Read more on [Development Basics](https://developer.chrome.com/docs/extensions/mv3/getstarted/development-basics/#load-unpacked).

## Contributing

Please see [the CONTRIBUTING file](/CONTRIBUTING.md) for information on contributing to the `chrome-extensions-samples` project.

## License

`chrome-extensions-samples` are authored by Google and are licensed under the [Apache License, Version 2.0](/LICENSE).
