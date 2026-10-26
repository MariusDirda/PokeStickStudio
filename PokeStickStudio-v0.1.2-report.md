# Poke Stick Studio — website v0.1.2

26 October 2026. Replaces generic number-tile hero illustrations and the homepage's text-only game wordmark with existing Popposite branding from the local Unity project.

- Hero areas on the studio homepage and Popposite page now show the real game logo and Android icon artwork.
- Homepage featured-game card shows the actual logo on its lavender background.
- Uses resized web copies of `Assets/Images/Candy Cloud Popposite Logo.png` (the logo referenced by Unity's presentation asset) and `Assets/ZeroPop/Android/Icons/PoppositeLauncher.png`. Logo transparency retained; no new artwork generated or source Unity assets modified.
- Studio favicon remains distinct from Popposite branding. Screenshot gallery, gameplay copy, consent/privacy content, and store availability preserved.
- Branding file sizes: logo PNG 586,863 bytes, icon JPEG 59,030 bytes. Only website-ready copies are published; no Unity source, configuration, saves, or unrelated art pack files.
- PASS: `node verify.cjs` — 3 pages, 57 internal file references, 20 anchors.
- Browser validation: branding assets load; homepage and game page fit at seven viewport sizes (320×480, 360×640, 768×1024, 1080×1920, 390×845, 360×800, 1440×900), with no document-width overflow.
- NOT RUN: new Unity tests/builds or physical Android validation; this is a website presentation change. Existing v0.1.1 Unity capture results remain specific to that capture run.

Prior versioned reports preserved. Outstanding privacy review and hosting activation checks in the earlier reports remain applicable.
