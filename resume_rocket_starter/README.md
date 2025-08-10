# ResumeRocket — Starter Flutter App (no-cost path)

Thanks — this is the starter project for **ResumeRocket**: a simple, fully offline-capable Flutter app that lets you create ATS-friendly resumes, pick templates, and export PDFs.

## What this starter includes
- Local resume editor (save resumes locally; no account required)
- Template selector (free ATS & modern templates; premium templates can be toggled for testing via Admin toggle)
- PDF export using `pdf` + `printing`
- A mock "AI rewrite" button (offline heuristic) — no external API keys required
- GitHub Actions workflow that builds an APK artifact automatically

**Everything in this starter can be used without spending money.** Real payments (subscriptions) and cloud backups require external services and accounts — those are optional and documented below.

---

## How to run the app locally (no coding required, step-by-step)

### 1) Install Flutter
Follow the official Flutter install guide for your OS: https://flutter.dev/docs/get-started/install

(On Windows/Mac/Linux you only need the Flutter SDK and Android SDK to build an APK. These are free.)

### 2) Get the project
- Download the zip you received (`resume_rocket_starter.zip`) and unzip it.
- Or clone the repo if you push to GitHub.

### 3) Open a terminal in the project folder and run:
```bash
flutter pub get
flutter run
```
The `flutter run` command will launch the app on a connected device or an emulator. This is the easiest way to test.

### 4) Build a release APK (one command)
```bash
flutter build apk --release
```
The APK will be at `build/app/outputs/flutter-apk/app-release.apk`. You can transfer that file to your Android phone and install it.

> If Android blocks installation from unknown sources, enable "Install unknown apps" temporarily for your file manager.

---

## Build via GitHub Actions (automatic APK on push)
1. Push this project to a GitHub repository.
2. The included workflow `.github/workflows/flutter-build.yml` will run on each push and create an `app-release.apk` artifact.
3. Go to Actions → select the workflow run → download artifact.

This route requires no local machine setup — GitHub Actions runs the build **for free** (within GitHub's limits).

---

## About premium / payments (no-cost alternative)
Real subscription payments (Stripe, Google Play Billing) require accounts and may have fees. Because you requested *no spending*, this starter:
- Implements premium templates behind a toggle called **Admin → toggle premium** on the Home screen.
- For production billing you'd connect Stripe/Play Billing later; I include notes in the code about where to add them.

---

## Adding AI features later (optional)
- The app includes a mock offline "AI rewrite". If you want real AI suggestions (OpenAI or other), you will need an API key and that service may charge per usage.
- I can provide step-by-step instructions to enable OpenAI integration so you only pay if/when you want real API calls.

---

## Next steps I can do for you (pick any)
1. Hookup Firebase for cloud backup, auth, and free-tier hosting (I will give exact steps; Firebase Spark tier is free for basic usage).
2. Add real Stripe/Play Billing integration (requires accounts).
3. Replace the mock AI with OpenAI integration and show exactly where to paste your API key.
4. Expand templates and polish PDF visual design.

Which of the above would you like next? If you want, I can also walk you step-by-step (with screenshots) to run `flutter build apk` on your machine or to use GitHub Actions — whichever you prefer.

