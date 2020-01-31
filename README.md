# Example app with Storybook and visual regression test

- [Next.js](https://github.com/zeit/next.js)
- [Storybook](https://github.com/storybookjs/storybook)
- [Chromatic](https://www.chromaticqa.com/)

This example shows a default set up of Storybook. Also included in the example is a custom component included in both Storybook and the Next.js application.

### Install it and run the Next.js app

```bash
yarn
yarn dev
```

## Run Storybook

```bash
yarn storybook
```

## Using Chromatic visual regression

On the first run, we need to use `npx chromatic --app-code=xxxxxxxxxx`.
 
Replace xxxxxxxxxx with the key provided by the platform on sign up.

This will create the baselines on the platform and ask to add the script to package.json

Use the added script (`yarn chromatic`) to run the current changes to against the baselines.

This script can be used on pre commit. It will return `error Command failed with exit code 1.` if the current differs from the baseline.

Running this will also log the url to the online platform where the diff can be inspected. If there are diffs, the platform allows the developer to accept the change and replace the baseline.

### worth to check alternatives:

- [webdriver.io](https://github.com/webdriverio/webdriverio) + [Spectre](https://github.com/wearefriday/spectre)
- [BackstopJS](https://github.com/garris/BackstopJS)
- [Loki](loki.js.org) + [Kaleidoscope](https://www.kaleidoscopeapp.com/)
