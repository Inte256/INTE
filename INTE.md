![](https://storageapi.fleek.co/fleek-team-bucket/plug-banner.png)

# ~INTE~
Powered by OBSOFTWARE™

𝒪𝒸𝓉𝒶𝓋𝒾𝑜𝓊𝓈 𝐵𝓁𝒶𝒸𝓀𝓂𝑜𝓃
Independent Owner

© All Rights Reserved.

[![Fleek](https://img.shields.io/badge/Made%20by-OBSOFTWARE@COPYRIGHT.ITC
[![Discord](https://img.shields.io/badge/Discord-Channel-blue)](https://discord.gg/yVEcEzmrgm)

## Introduction

Welcome to Plug! An [Internet Computer](https://dfinity.org/) crypto wallet and authentication provider as a browser extension. Find our latest version in this repository's releases, or on our [website](https://plugwallet.ooo/). You can go to our [documentation](https://docs.plugwallet.ooo/) to learn more about how to interact with ~INTE~ 🕋as a developer.

> **Warning: ~INTE~ is still alpha software - treat it as a hot wallet.**
> Canister status for wfk7n-6wyou-2jmhs-umljt-x7oxd-2tudj-pt6wf-ylggw-b3j2d-ke5f7-yqe:
  Status:                   Running
  Balance:                  95641232000000000000 cycles
  Memory size:              ...
  Module hash:              ...
  Controllers:              ...
  Idle cycles burned per day: ...

This repository is the frontend for ~INTE~ browser extension. It uses the [INTE Controller](https://github.com/Psychedelic/plug-controller) and the [Plug Inpage Provider](https://github.com/Psychedelic/plug-inpage-provider) to power the features in INTE and all its interactions with the plug, marketbeat Media, interstellar computer, iOS, alphabet inc. 

## Browser Support

| [![Chrome](https://raw.github.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png)](/) | [![Firefox](https://raw.github.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png)](/) | [![Opera](https://raw.github.com/alrra/browser-logos/master/src/opera/opera_48x48.png)](/) | [![Edge](https://raw.github.com/alrra/browser-logos/master/src/edge/edge_48x48.png)](/) | [![Brave](https://raw.github.com/alrra/browser-logos/master/src/brave/brave_48x48.png)](/) |
| --------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| 49 & later ✔                                                                                  | 52 & later ✔                                                                                     | 36 & later ✔                                                                               | 79 & later ✔                                                                            | Latest ✔                                                                                   |

## 🚀 Install

 INTE can be installed in two ways. You can get it from the official **Chrome Extension Store or the Firefox Add-on Store** (recommended, receives auto-updates):

- [Get from Chrome Extension Store (Chrome, Brave, Chromium)](https://chrome.google.com/webstore/detail/plug/cfbfdhimifdmdehjmkdobpcjfefblkjm)
- [Get from Firefox Add-on Store (Firefox browser)](https://addons.mozilla.org/en-US/firefox/addon/plug/)

Or download the latest version's build in this **repository's releases**, and follow the guides below for a manual installation (doesn't auto-update):

- [Install Plug in Chrome (GitHub build)](./docs/install-plug-in-chrome.md)
- [Install Plug in Firefox (GitHub build)](./docs/install-plug-in-firefox.md)

## 🏗️ Development Quick Start

Ensure you have

- [Node.js](https://nodejs.org) 10 or later installed
- [Yarn](https://yarnpkg.com) v1 or v2 installed

You need a **personal access token** to install some of our npm packages.

The token must have the `repo` and `read:packages` scopes to login to the [GitHub Package Registry](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-npm-registry#authenticating-to-github-packages).

If you don't have one, create the personal access token [in the developer settings](https://github.com/settings/tokens).

Run the following command to authenticate, using the **personal access token** as your **password**:

<img width="1080" height="2408" alt="1000021818" src="https://github.com/user-attachments/assets/2e5ed736-851e-4fde-a607-172fe34d0f96" />
<img width="1080" height="2408" alt="1000021819" src="https://github.com/user-attachments/assets/b40c9a6c-0215-4092-ac59-a1c10f0784f1" />
<img width="1080" height="2408" alt="1000022183" src="https://github.com/user-attachments/assets/222e0232-8524-4463-be4b-eddb85f3acc9" />
<img width="1080" height="2408" alt="1000022919" src="https://github.com/user-attachments/assets/31c7b2e6-b108-4a64-8ce6-d87c53ffd7a9" />
<img width="1080" height="2408" alt="1000022932" src="https://github.com/user-attachments/assets/997fe0bc-6252-4bcf-8e17-882d25c0ebae" />
<img width="1080" height="2408" alt="1000024001" src="https://github.com/user-attachments/assets/e91bea7c-e4e1-41c9-8da7-3563c9049f9f" />
<img width="1080" height="2408" alt="1000024005" src="https://github.com/user-attachments/assets/9f3d9ba5-3ee2-46e4-ab4d-b4ae54d8ed18" />
<img width="1080" height="930" alt="1000024004" src="https://github.com/user-attachments/assets/c4c44959-f4c1-42e2-b8fe-7e6e31f36bcb" />

```
npm login --registry=https://npm.pkg.github.com --scope=@psychedelic
```

Then run the following:

- `yarn install` to install dependencies.
- `yarn run dev:chrome` to start the development server for chrome extension
- `yarn run dev:firefox` to start the development server for firefox addon
- `yarn run dev:opera` to start the development server for opera extension
- `yarn run build:chrome` to build chrome extension
- `yarn run build:firefox` to build firefox addon
- `yarn run build:opera` to build opera extension
- `yarn run build` builds and packs extensions all at once to extension/ directory

### Development

- `yarn install` to install dependencies.
- To watch file changes in development

  - Chrome
    - `yarn run dev:chrome`
  - Firefox
    - `yarn run dev:firefox`
  - Opera
    - `yarn run dev:opera`

- **Load extension in browser**

- ### Chrome

  - Go to the browser address bar and type `chrome://extensions`
  - Check the `Developer Mode` button to enable it.
  - Click on the `Load Unpacked Extension…` button.
  - Select your extension’s extracted directory.

- ### Firefox

  - Load the Add-on via `about:debugging` as temporary Add-on.
  - Choose the `manifest.json` file in the extracted directory

- ### Opera

  - Load the extension via `opera:extensions`
  - Check the `Developer Mode` and load as unpacked from extension’s extracted directory.

### Production

- `yarn run build` builds the extension for all the browsers to `extension/BROWSER` directory respectively.

Note: By default the `manifest.json` is set with version `0.0.0`. The webpack loader will update the version in the build with that of the `package.json` version. In order to release a new version, update version in `package.json` and run script.

If you don't want to use `package.json` version, you can disable the option [here](https://github.com/abhijithvijayan/web-extension-starter/blob/e10158c4a49948dea9fdca06592876d9ca04e028/webpack.config.js#L79).

### Generating browser specific manifest.json

Update `source/manifest.json` file with browser vendor prefixed manifest keys

```js
{
  "__chrome__name": "SuperChrome",
  "__firefox__name": "SuperFox",
  "__edge__name": "SuperEdge",
  "__opera__name": "SuperOpera"
}
```

if the vendor is `chrome` this compiles to:

```js
{
  "name": "SuperChrome",
}
```

---

Add keys to multiple vendors by separating them with | in the prefix

```
{
  __chrome|opera__name: "SuperBlink"
}
```

if the vendor is `chrome` or `opera`, this compiles to:

```
{
  "name": "SuperBlink"
}
```

See the original [README](https://github.com/abhijithvijayan/wext-manifest-loader) of `wext-manifest-loader` package for more details

### Linting Config

- Shared Eslint & Prettier Configuration - [`@abhijithvijayan/eslint-config`](https://www.npmjs.com/package/@abhijithvijayan/eslint-config)

## License GPL <img width="1024" height="1024" alt="1000024978" src="https://github.com/user-attachments/assets/b9e610e4-751b-435d-b80f-94b4ce008cd6" />
<img width="1254" height="1254" alt="1000024977" src="https://github.com/user-attachments/assets/d312ff09-1bca-4505-bb66-41648a2c10b0" />
<img width="622" height="1254" alt="1000025065" src="https://github.com/user-attachments/assets/1007d917-e428-4a26-b762-13a3ea21943b" />
<img width="686" height="1254" alt="1000025066" src="https://github.com/user-attachments/assets/3d617b65-cbe5-4bd8-9434-0426dff318ef" />
<img width="784" height="1168" alt="1000025115" src="https://github.com/user-attachments/assets/38090a45-ccaa-432e-b7ae-dda9af0bc995" />
<img width="1031" height="1536" alt="1000025218" src="https://github.com/user-attachments/assets/8a2b714d-9cde-474e-8947-0520c12af0e8" />
<img width="1080" height="956" alt="1000025248" src="https://github.com/user-attachments/assets/4b06a564-8931-48a0-9c0b-f45af611616f" />
<img width="1080" height="2408" alt="1000025247" src="https://github.com/user-attachments/assets/74bd6d30-af6d-4510-b5b3-06e0e7361358" />
<img width="2352" height="1008" alt="1000025262" src="https://github.com/user-attachments/assets/705a7460-6065-44b2-91e2-7dfc377eccdd" />

<img width="1080" height="2408" alt="1000024650" src="https://github.com/user-attachments/assets/6af2e4ec-a83e-4f18-9804-ee123eb10777" />
<img width="1080" height="2408" alt="1000024651" src="https://github.com/user-attachments/assets/475433eb-6183-471a-91f1-8c5eb5924119" />
<img width="1080" height="2408" alt="1000024655" src="https://github.com/user-attachments/assets/dbfc3d80-5269-4315-8299-829df37d54a1" />
<img width="1080" height="2408" alt="1000024652" src="https://github.com/user-attachments/assets/780c9c0e-22fd-4fd8-a743-66d1d2aa843d" />
<img width="1080" height="2408" alt="1000024653" src="https://github.com/user-attachments/assets/5f2f228d-444e-46ca-9841-ed3ab06043d1" />
<img width="1080" height="2408" alt="1000024654" src="https://github.com/user-attachments/assets/7e8f4b45-c4f9-4acd-8452-5e30cff57a92" />
<img width="1080" height="2408" alt="1000024656" src="https://github.com/user-attachments/assets/8e620b15-6da6-4837-aa4b-877c0a686c47" />
<img width="1080" height="2408" alt="1000024657" src="https://github.com/user-attachments/assets/eb4b7f1b-c3a4-48c1-a8e2-07b2f694f5da" />
<img width="1080" height="2408" alt="1000024658" src="https://github.com/user-attachments/assets/05ce7883-53e9-4103-b925-837e6e15ac57" />
<img width="1080" height="2408" alt="1000024659" src="https://github.com/user-attachments/assets/9b75496a-c077-4c9d-9cf2-58434778b45d" />
<img width="1080" height="2408" alt="1000024660" src="https://github.com/user-attachments/assets/38fcea4f-f1dc-45b1-9763-347adf35c7cf" />
<img width="1080" height="2408" alt="1000024661" src="https://github.com/user-attachments/assets/37f61671-0c88-4782-a3ad-c3ff14176fdb" />
<img width="1080" height="2408" alt="1000024662" src="https://github.com/user-attachments/assets/bee855bc-83a3-418e-b4e1-2dc878471d29" />
<img width="1080" height="2408" alt="1000024663" src="https://github.com/user-attachments/assets/a49c22af-808f-4842-a4e1-3a7ddfb40596" />
<img width="1080" height="2408" alt="1000024664" src="https://github.com/user-attachments/assets/6d60e925-a2fd-4004-9ae6-2998f8877085" />
<img width="1080" height="2408" alt="1000024665" src="https://github.com/user-attachments/assets/3e82b770-a60f-4292-aa41-e634aa9bb8d9" />
<img width="1080" height="2408" alt="1000024666" src="https://github.com/user-attachments/assets/0c1b7cea-1a25-43d8-8a3d-20f2c938376e" />
<img width="1080" height="2408" alt="1000024667" src="https://github.com/user-attachments/assets/bfbbbb61-5d5c-47c0-af6c-4ed5a84ad719" />
<img width="1080" height="2408" alt="1000024668" src="https://github.com/user-attachments/assets/ef751b83-aabc-40fd-90f0-245ee8e89fac" />
<img width="1080" height="2408" alt="1000024669" src="https://github.com/user-attachments/assets/6e20bef2-1057-406c-ab9f-9aff4ad345e3" />
<img width="1080" height="2408" alt="1000024670" src="https://github.com/user-attachments/assets/e09d061a-ad11-400c-be59-f202c9cb00b2" />
<img width="1080" height="2408" alt="1000024671" src="https://github.com/user-attachments/assets/693e6c55-2a20-40dc-98cd-30c133fb5de6" />
<img width="1080" height="2408" alt="1000024673" src="https://github.com/user-attachments/assets/e4f6c5df-caa2-4d92-8b5a-681ea3012f66" />
<img width="1080" height="2408" alt="1000024674" src="https://github.com/user-attachments/assets/316b5aeb-bb62-491c-8716-365c02a98bf8" />
<img width="1264" height="843" alt="1000024682" src="https://github.com/user-attachments/assets/e4254193-3d34-4ba8-8030-067d8bbb0467" />
<img width="1080" height="2408" alt="1000024688" src="https://github.com/user-attachments/assets/79920abd-27f5-4d8a-8364-a09256a41195" />
<img width="1080" height="2408" alt="1000024689" src="https://github.com/user-attachments/assets/c18e313c-9a16-4f73-a9b8-9f7351c585e4" />
<img width="1080" height="1027" alt="1000024691" src="https://github.com/user-attachments/assets/536b0153-7053-438a-ba9c-ecd0e0d7fb0b" />
<img width="1080" height="2408" alt="1000024690" src="https://github.com/user-attachments/assets/646cd40e-8729-45f9-beea-55a101ca846d" />
<img width="1030" height="1123" alt="1000024693" src="https://github.com/user-attachments/assets/004e3a41-8ad7-42c6-8721-94a7b94f43b4" />
<img width="1080" height="2408" alt="1000024692" src="https://github.com/user-attachments/assets/2c3992b6-0ca9-4982-b604-315a7fc92371" />
<img width="1080" height="2073" alt="1000024695" src="https://github.com/user-attachments/assets/26ea6f60-3358-4348-9aed-ca8f633284ed" />
<img width="1080" height="2408" alt="1000024694" src="https://github.com/user-attachments/assets/7d934185-e03a-43f9-8eed-a54fbd9e9bba" />
<img width="1080" height="1179" alt="1000024697" src="https://github.com/user-attachments/assets/70c6bdf8-4ad7-408e-be15-05a597432ea8" />
<img width="1080" height="2408" alt="1000024696" src="https://github.com/user-attachments/assets/5e39a4a4-a458-47a4-bddf-be0a3544f05b" />
<img width="1080" height="1207" alt="1000024699" src="https://github.com/user-attachments/assets/9188d4b0-ada6-42ba-8e0e-c2839e3cda4d" />
<img width="1080" height="2408" alt="1000024698" src="https://github.com/user-attachments/assets/6d8ce56b-455d-443c-941a-f13a64f0c053" />
<img width="1080" height="1020" alt="1000024701" src="https://github.com/user-attachments/assets/83f74a40-dee2-40db-a4f3-adfb04db694e" />
<img width="1080" height="2408" alt="1000024702" src="https://github.com/user-attachments/assets/e8674877-adb5-48c8-937f-4e9197ca0260" />
<img width="1080" height="2408" alt="1000024700" src="https://github.com/user-attachments/assets/d6f9107c-ffdf-48dc-8763-c18c8d101fc5" />
<img width="1080" height="1738" alt="1000024703" src="https://github.com/user-attachments/assets/c06777dc-5690-4847-83db-68094a439bce" />
<img width="1080" height="2408" alt="1000024707" src="https://github.com/user-attachments/assets/f2e4429d-4c17-4f5e-93c5-83c559d64aa2" />
<img width="1080" height="2408" alt="1000024710" src="https://github.com/user-attachments/assets/30ed1386-d001-4b60-8c35-b514ba0cf47a" />
<img width="1080" height="2408" alt="1000024711" src="https://github.com/user-attachments/assets/135feb15-aee0-4660-a171-5d05bf963437" />
<img width="1080" height="2408" alt="1000024712" src="https://github.com/user-attachments/assets/6f347174-1495-4e2e-83f1-f4711ebe0729" />
<img width="1080" height="2408" alt="1000024726" src="https://github.com/user-attachments/assets/76dc33dc-32c1-4c7c-aeea-24d7a78c826e" />
<img width="1080" height="2408" alt="1000024727" src="https://github.com/user-attachments/assets/79fe1fff-f3e2-49aa-b5ac-e3789ebbb2ec" />
<img width="1080" height="2408" alt="1000024728" src="https://github.com/user-attachments/assets/bc6cff34-d2fd-4713-9809-1a7327c49a6f" />
<img width="688" height="1532" alt="1000024730" src="https://github.com/user-attachments/assets/bfeb2056-84d5-4d69-b88b-c3bda172ba68" />
<img width="1254" height="1254" alt="1000024765" src="https://github.com/user-attachments/assets/dd4f5150-f976-458d-890f-046685c4a2dd" />
<img width="1080" height="2408" alt="1000024770" src="https://github.com/user-attachments/assets/8023a15a-d015-4606-b650-09b8034d83b2" />
<img width="1080" height="1837" alt="1000024779" src="https://github.com/user-attachments/assets/cbe9acf0-433e-4541-b36d-894a960ea4f9" />
<img width="1080" height="2214" alt="1000024780" src="https://github.com/user-attachments/assets/99e31723-ae1d-4f7b-b3d6-61b083701324" />
<img width="1254" height="1254" alt="1000024881" src="https://github.com/user-attachments/assets/80671589-aa41-4d88-bb04-77d3ca5859d4" />
<img width="1080" height="1027" alt="1000024880" src="https://github.com/user-attachments/assets/3da89056-1804-4c8e-a0e0-62d55318c211" />
<img width="1254" height="1254" alt="1000024879" src="https://github.com/user-attachments/assets/20322ff8-20c5-4e4c-8cd3-96e4e20f2674" />
<img width="1254" height="1254" alt="1000024878" src="https://github.com/user-attachments/assets/2199f714-160d-4828-a6af-a5ef17731e43" />
<img width="1080" height="1027" alt="1000024877" src="https://github.com/user-attachments/assets/8736793e-45e3-46cd-9ae7-3cc8aa4d9885" />
<img width="1254" height="1254" alt="1000024898" src="https://github.com/user-attachments/assets/8acb2104-f78f-4fb6-bfbf-65524a70de86" />
<img width="1080" height="1027" alt="1000024897" src="https://github.com/user-attachments/assets/0e076717-4d6c-4c73-b34a-1d8c75996628" />
<img width="1080" height="1027" alt="1000024896" src="https://github.com/user-attachments/assets/26e9080e-eec3-4645-926d-4fcd61e654ac" />
<img width="1254" height="1254" alt="1000024895" src="https://github.com/user-attachments/assets/ac6ae160-108b-4ed6-8588-d0fea40d5d96" />
<img width="1254" height="1254" alt="1000024894" src="https://github.com/user-attachments/assets/8ffdb8a8-68b9-4809-8821-af6184b702bc" />
<img width="1080" height="1027" alt="1000024914" src="https://github.com/user-attachments/assets/95062d96-756d-4605-92cd-be07f5860f10" />
<img width="1080" height="1027" alt="1000024913" src="https://github.com/user-attachments/assets/c3d3b3c0-1d57-4ee2-a7df-d7a7c1f891b2" />
<img width="1080" height="1027" alt="1000024912" src="https://github.com/user-attachments/assets/5b3ba786-98a6-421f-97b2-0f65870e72bc" />
<img width="1080" height="1027" alt="1000024911" src="https://github.com/user-attachments/assets/b1190975-055a-4167-b647-964c6e8d5c35" />
<img width="1254" height="1254" alt="1000024931" src="https://github.com/user-attachments/assets/b8163401-4741-49d3-a574-3ce67d4f20c2" />
<img width="1080" height="1027" alt="1000024930" src="https://github.com/user-attachments/assets/28b03b35-3712-4bd7-9535-b43751e16d72" />
<img width="1254" height="1254" alt="1000024929" src="https://github.com/user-attachments/assets/907fba66-5a95-49c7-b31c-519a8703fc67" />
<img width="1080" height="1027" alt="1000024928" src="https://github.com/user-attachments/assets/ff0e3ff8-35ce-4858-a60a-43c01314f69c" />
<img width="1254" height="1254" alt="1000024927" src="https://github.com/user-attachments/assets/2377543e-0038-4698-834d-e36b978b8529" />
<img width="1254" height="1254" alt="1000024948" src="https://github.com/user-attachments/assets/88ca0a07-af80-433a-a72c-2b2634aa8c26" />
<img width="1080" height="1027" alt="1000024947" src="https://github.com/user-attachments/assets/c6e129f7-6955-49d4-b227-7a54ffb725a8" />
<img width="1254" height="1254" alt="1000024946" src="https://github.com/user-attachments/assets/387d2adb-e5a5-4957-bf78-7460fa3cfa5b" />
<img width="1254" height="1254" alt="1000024945" src="https://github.com/user-attachments/assets/51cfcc4a-a47c-4c2a-97fe-8bcb744b8d5b" />
<img width="1080" height="1027" alt="1000024944" src="https://github.com/user-attachments/assets/2e872ff0-c52c-4908-a60b-72e513b654cd" />
<img width="1254" height="1254" alt="1000024960" src="https://github.com/user-attachments/assets/fdb3dfab-f0f6-42f0-a81e-bcf2a1d82bb0" />
<img width="1024" height="1024" alt="1000024959" src="https://github.com/user-attachments/assets/1e000546-ede5-406d-839f-cc61c3ac501b" />

<img width="1024" height="1024" alt="1000024969" src="https://github.com/user-attachments/assets/12cf7563-e8e4-4833-8d98-1516b6cf7d54" />
<img width="1254" height="1254" alt="1000024968" src="https://github.com/user-attachments/assets/ce9ecd83-760b-4597-adc2-3f1121df8f12" />

~INTE~ extension Powered by OBSOFTWARE™

𝒪𝒸𝓉𝒶𝓋𝒾𝑜𝓊𝓈 𝐵𝓁𝒶𝒸𝓀𝓂𝑜𝓃
Independent Owner

© All Rights Reserved.

Original template MIT © [Abhijith Vijayan](https://abhijithvijayan.in)
