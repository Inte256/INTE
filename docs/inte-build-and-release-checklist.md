# INTE build and release checklist

This repository is a browser-extension wallet project (a fork of Psychedelic/Plug), not the separate Vite/ICP starter. These steps build the extension locally; they do not deploy an ICP canister or publish a browser-store release.

## Prerequisites

- Use a trusted checkout and review the source and dependency changes before installing.
- Install a Node.js version compatible with the repository and Yarn Classic (the project documents Yarn v1/v2).
- If installation needs GitHub Packages, authenticate interactively with a least-privilege token that has only the required package access. Never put tokens in source, shell history, screenshots, or chat.

## Install and build

```sh
yarn install
yarn build
```

The `build` script creates Chrome and Firefox builds under `extension/`. To build one target only:

```sh
yarn build:chrome
yarn build:firefox
```

For local development, use the matching target script, for example `yarn dev:chrome` or `yarn dev:firefox`.

## Local smoke test

1. Inspect the generated `extension/chrome` and `extension/firefox` output and confirm only expected files are present.
2. In Chrome, open `chrome://extensions`, enable Developer mode, and load the unpacked `extension/chrome` directory.
3. In Firefox, open `about:debugging`, select This Firefox, and load the built manifest as a temporary add-on. Temporary add-ons may be removed when Firefox restarts.
4. Test using a disposable wallet with no funds. Never enter a production seed phrase into a development build.
5. Verify wallet creation/import, account display, network selection, and signing/transfer warnings in a controlled test environment before any release.

## Release gates

- Review code, permissions, dependency changes, secrets, and generated artifacts; run the repository's lint and test scripts where supported.
- Arrange an independent security review before inviting users to install a wallet build.
- Confirm authorization to use upstream Plug code, names, icons, and store listings. Do not imply endorsement by Plug/Psychedelic without permission.
- Publish only through authorized, reviewed release channels with clear versioning, support, privacy, and recovery information.
- Do not claim a live canister, connected account, verified balance, or production deployment unless it has actually been configured and independently checked.

No secrets, canister IDs, account balances, tax identifiers, or personal device/network identifiers belong in this checklist. `icp deploy` is not a deployment step for this browser-extension repository.
