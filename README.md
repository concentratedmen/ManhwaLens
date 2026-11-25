# ManhwaLens EN
Phase 1: project skeleton, PDF picker, high-res PdfRenderer with quality presets, CI APK build.

## Build without Android Studio
1. Create a GitHub repo, upload this folder's contents, push to `main`.
2. Actions tab -> "Build APK" -> download `ManhwaLensEN-apks` artifact -> install the debug APK.

## Memory tuning
`RenderQuality.MAX_PIXELS` caps bitmap size (12 MP default). Use 8 MP on 3 GB phones, and prefer Standard quality.

## Phase 2
OCR (ML Kit Latin) -> bubble grouping -> SFX filter -> ML Kit id->en -> bubble cleanup/auto-fit render.
First translation downloads the ~30 MB offline model (needs internet once). Translated pages are saved in app storage.
