# INTE release plan (draft; not a release authorization)

**Current scope:** Prepare a reviewable release process for the browser-extension repository. This document does not assert that a build passed, a security audit was completed, a store listing is approved, or any release was published.

## 1. Confirm the release target

- Confirm the repository is `Inte256/INTE` and the release branch is based on the intended, reviewed commit.
- Confirm the release owner has permission to publish from the project's authorized Chrome/Firefox publisher accounts.
- Confirm license compliance and permission for all upstream Plug/Psychedelic code, names, icons, and store assets. Do not imply upstream endorsement without permission.
- Agree on version number, target browsers, supported platforms, release date, and support contact.
- Review `SECURITY.md`, manifest permissions, dependency changes, CI results, repository history, and release artifacts for secrets or unnecessary personal/device identifiers.

## 2. Install, validate, and build

Use a clean checkout and a supported Node/Yarn version. The project documents Yarn and defines these scripts in `package.json`:

```sh
yarn install
yarn lint
yarn test
yarn build
```

The `build` script creates Chrome and Firefox extension packages under `extension/`. To build one target:

```sh
yarn build:chrome
yarn build:firefox
```

Check every command's exit status. Investigate and fix failures; do not mark a release as validated based on a partial build. Review the dependency audit output and resolve or document material findings before release. Do not indiscriminately run automated dependency upgrades on a wallet project.

## 3. Test the built extensions

- Inspect the package contents and manifests; confirm requested permissions and host access are necessary and expected.
- Install the unpacked Chrome build via `chrome://extensions` with Developer mode enabled.
- Load the Firefox build temporarily via `about:debugging` → This Firefox. Temporary installation may not persist after restart.
- Exercise onboarding, lock/unlock, account display, network selection, connection prompts, transaction review/warnings, and failure states using a disposable test wallet with no funds.
- Never enter a production seed phrase or private key into a development/test build.
- Record browser/version, build commit, test results, and known issues. Stop if unexpected network requests, permissions, signing prompts, or wallet behavior appear.

## 4. Security and release approval gates

Do not distribute a wallet build to users until the project owner confirms all applicable gates:

- Independent security review and remediation of findings.
- Source-to-artifact review and reproducible/traceable build process.
- License, trademark, branding, and store-account authorization.
- Accurate privacy disclosures, data handling, support, recovery, and incident-response information.
- Store policy compliance and review approval.
- Explicit human approval of the exact version, artifacts, release notes, and publishing destination.

If a gate is incomplete, label the artifact as an internal preview/test build and restrict distribution. Do not claim production readiness, audit completion, live financial data, or upstream endorsement without evidence.

## 5. Prepare release artifacts

1. Choose and verify the version in `package.json` and the generated manifest.
2. Build from the reviewed commit using the commands above.
3. Inspect the `extension/` directory and calculate checksums for the exact packages to be uploaded.
4. Store the packages and checksums with the release record; do not commit secrets or local credentials.
5. Prepare the release notes below and have an authorized reviewer approve them.

## 6. Publish only through authorized channels

- Chrome: use the project's authorized Chrome Web Store publisher account and follow its current submission/review flow.
- Firefox: use the project's authorized AMO publisher account and follow its current submission/review flow.
- For private/internal preview distribution, restrict access to approved testers and communicate installation risks.
- Verify the resulting listing/version and download links after publication. Record publisher, timestamp, commit, version, artifact checksums, and listing URLs.

No store submission, ICP canister deployment, payment processing, or external publishing is performed by this document. This repository's build scripts are for browser extensions; `icp deploy` is not a release command for this project.

## 7. Draft release notes (fill in only after verification)

### INTE [VERSION] — [DATE]

**Status:** [internal preview / public release — choose only after approval]

- Summary: [describe changes verified in this build]
- Browser packages: Chrome [version/link]; Firefox [version/link]
- Tested on: [browser versions and test results]
- Known issues: [list, or state none only if verified]
- Security review: [status and public reference, if approved for disclosure]
- Support: [verified support channel]

INTE is a browser extension. Do not describe it as an ICP canister deployment or a production financial service unless separately implemented and verified.

## 8. Draft announcement (preview wording)

> **INTE build update**
>
> A new INTE browser-extension build is prepared for [internal testing / release] on [supported browsers]. This build is based on [version/commit]. See the release notes for verified changes, known issues, and installation guidance.
>
> Wallet software can involve security risks. Install only from the authorized distribution channel, review permission prompts, and never share your recovery phrase or private key. [Include a security-review statement only if independently verified.]

Replace every bracketed field, verify all claims, and obtain approval before publishing.
