# Poke Stick Studio — website v0.1.1

26 October 2026. Replaces the three screenshot placeholders with fresh Unity Editor captures of the current local Popposite UI: Android menu, puzzle board, and completion screen. Existing v0.1.0 report is retained as historical evidence.

## Capture provenance

Unity 6000.3.26f1 ran these existing PlayMode tests against the local project on 26 October 2026:

- `ZeroPop.Tests.MainMenuPlatformTests.AndroidAndDesktopKeepActionsAlignedAndCenteredAcrossPortraits`
- `ZeroPop.Tests.GameplayArtTests.GameplayVictoryAndWarningRenderAcrossPortraits`

Result: **2 passed, 0 failed**. New local test results and original PNG captures are under `Website/Evidence-v0.1.1/`. Nothing from that evidence directory is uploaded to the public repository.

The menu is the Android presentation fixture (no desktop Exit button). The board is the existing 3×3 visual fixture with positive, negative and zero tiles plus one inactive cell; it is not a claimed campaign-level screenshot. The completion view uses the existing isolated two-star/one-Undo fixture. The gallery explicitly labels these pre-release Unity Editor UI previews using test boards and results. These are actual Unity renders, not fabricated screenshot artwork or physical Android captures.

Original captures: `MainMenu_v0.9.3.6/Android_1080x1920.png`, `ZeroTiles_v0.9.2.3/Gameplay_1080x1920.png`, `ZeroTiles_v0.9.2.3/Victory_1080x1920.png`. These historical group names are retained by the current test helper; all three images were regenerated in this run. Local capture root was set per process so earlier evidence was not overwritten.

Web copies are 1080×1920 JPEGs at quality 90 (no cropping or retouching), totaling about 515 KiB instead of 3.3 MiB of PNGs. Raw game art, Unity code, configuration, player saves, logs, and credentials are excluded from the website repository.

## Website changes and validation

- Three-image gallery with descriptive alt text, intrinsic image dimensions, lazy loading, full-size image links, and responsive layout.
- Website footer version v0.1.1; existing privacy-policy effective date and substantive policy unchanged.
- `node verify.cjs`: PASS, 3 pages, 52 internal file references, 20 anchors.
- Browser loaded all three screenshot images at their correct 1080×1920 intrinsic dimensions. Desktop and mobile layout/full-image navigation checked before publication.
- Existing Unity presentation tests passed; this is not a claim that the whole Unity suite, Android build, or physical-device validation ran.
- No Unity production source, assets, campaign data, player settings, or player saves were changed. Capture fixtures do not reset player saves.

The v0.1.0 privacy review items (target age audience, release advertising configuration, legal details, support retention and regional consent) remain outstanding. GitHub Pages activation/public-hosting state must be checked separately from a repository push.
