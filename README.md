# citizo-legal

Support, Privacy Policy and Terms of Use (EULA) for **Citizo**, the French civic exam
preparation app (App Store id 6824220744, bundle id `com.gaureac.citizo.fr`), served by
GitHub Pages at https://gaureac.github.io/citizo-legal/.

| Page | French | English |
|---|---|---|
| Support | `index.html` | `en/index.html` |
| Privacy | `privacy.html` | `en/privacy.html` |
| Terms (EULA) | `terms.html` | `en/terms.html` |

The app opens the French pages for the French interface and the English ones for every
other interface language. App Store Connect uses the same URLs (privacy policy URL per
locale, support URL, Terms link in the description).

Keep the pages true to the app: no «à vie» / «lifetime» for the one-time payment, no
trial claim beyond the conditional clause, and a «last updated» date that changes with
any edit. If a release changes how data is handled, update the Privacy Policy and the
App Privacy answers in App Store Connect before it ships.

## app-version.json

Read by the app at most once a day (https://gaureac.github.io/citizo-legal/app-version.json),
the same contract as Receipt Scanner's. **Bump `latestVersion` only once a release is
downloadable on the App Store**, never at submission, with `releaseNotes` in every
Interface language (`fr`, `en`, `ar`, `ru`, `prs`; `en` is the fallback). Only for a
broken release: raise `minimumSupportedVersion` above it, or set `required: true`. Both
make affected builds ask to update on launch; it is a prompt, never a lock.
