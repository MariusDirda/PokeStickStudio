# Poke Stick Studio — website v0.1.0 report

Date: 26 October 2026. Repository: `MariusDirda/PokeStickStudio`, target branch `main`.

## Delivered

Three static pages: studio home, Popposite overview, and Popposite privacy policy. Shared responsive CSS, original SVG favicon and CSS illustration, semantic landmarks, keyboard focus/skip link, reduced-motion support, metadata and canonical URLs, contact `pokestickstudio@gmail.com`, disabled Coming Soon store button, and explicitly labeled screenshot placeholders. No runtime JavaScript or external dependencies. Relative navigation and assets support `/PokeStickStudio/`. Includes `.nojekyll`, README deployment instructions, and repeatable `node verify.cjs` checks.

## Implementation review

Inspected the local Unity handover and actual relevant sources before drafting. Actual editor version is 6000.3.26f1. Reviewed advertising service/controller, Google SDK adapter and UMP calls, Settings privacy-choice entry point, Firebase analytics policy and service, Android privacy manifest, progress repository, and authoritative BoardState addition rules.

Findings: rewarded/interstitial adapters and UMP exist; production ad requests are disabled, Android development builds use test ads, Firebase Analytics is disabled/deactivated, advertising-ID permission is removed, and local progression includes recovery backups. The policy distinguishes implementation from launch behavior. No Unity files, identifiers, private settings, signing material, logs, or saves are included in the website repository.

Official references checked on 26 October 2026:

- [Google Mobile Ads Unity disclosure](https://developers.google.com/admob/unity/privacy/play-data-disclosure)
- [UMP Unity setup](https://developers.google.com/admob/unity/privacy)
- [Google Privacy Policy](https://policies.google.com/privacy)
- [Google Play user-data policy](https://support.google.com/googleplay/android-developer/answer/10144311)
- [GitHub Pages data collection](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages#data-collection)

Google's latest SDK documentation is general guidance, not proof of the installed SDK's exact behavior. Final release review remains required.

## Validation

- PASS: `node verify.cjs`: all 3 pages, 46 local file references, 20 fragment references; no missing targets or duplicate IDs. One h1 per page, viewport/SEO/Open Graph metadata, no scripts/iframes/external styles or fonts, focus/reduced-motion CSS, disabled store control.
- PASS: website served locally at `http://127.0.0.1:4173/PokeStickStudio/` and loaded in the browser after resolving sandbox loopback restrictions.
- PASS: browser navigation home → game → privacy and home → studio anchor.
- Browser DOM layout checks: 3 pages × 7 viewports: 320×480, 360×640, 768×1024, 1080×1920, 390×845 (19.5:9), 360×800 (20:9), 1440×900. No broken image elements. Initial decorative orbit overflow was fixed using local clipping. A final 3px content overflow at 320px on the game title was fixed by reducing that title responsively; browser confirmed document scrollWidth equals clientWidth (305px with scrollbar).
- Visual inspection: desktop homepage, studio/contact section, narrow mobile home, game and privacy introductions. Automated dimension checks are not a complete accessibility or cross-browser audit.
- NOT RUN: physical-device testing, complete screen-reader audit, Safari/Firefox checks, external email delivery, or game/SDK runtime tests. Unity code was not changed; no Unity/Android build results are claimed.
- Public hosting is pending Pages configuration. The connector has repository-write tools but no Pages settings mutation. A signed-out browser cannot access repository settings. Enable **Settings → Pages → Deploy from a branch → main → / (root)**, then verify the public policy URL without authentication. Repository publication alone is not a Pages deployment or Google Play approval.

## Developer review required

1. Confirm legal operator details and distribution regions; add any required regional disclosures.
2. Confirm target age audience/age rating and appropriate child-related SDK, advertising, and consent settings. No child-directed compliance claim is made.
3. Confirm the final signed release's ad enablement, merged manifest, SDK versions and third-party partners. Reconcile policy and Play Data safety answers before enabling live ads.
4. Verify AdMob account privacy-message configuration and regional UMP choices on release devices.
5. Specify how long studio support emails are retained and how deletion requests are handled.
6. Review Android/device backup behavior and deletion instructions for the shipping package.
7. Replace screenshot placeholders with approved real game images and add the verified Google Play URL when available.
8. Enable GitHub Pages and verify unauthenticated HTTPS access to `/PokeStickStudio/privacy/popposite.html`; add the final link to Play Console and the game as appropriate.

Contact email was supplied explicitly by the developer. Effective date: 26 October 2026. This is an implementation-informed pre-release policy with visible unresolved items, not a certification of legal or Google Play compliance.
