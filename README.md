# Personal App Store

A lightweight public Android app catalog hosted with GitHub Pages. APK binaries should be attached to GitHub Releases rather than committed to the website repository.

## Add an app

1. Open **Releases → Create a new release** and attach the APK.
2. Copy the APK asset's download URL.
3. Edit `apps.json` and add an entry under `apps`. Fields: `name`, `version`, `category`, `minAndroid`, `description`, `downloadUrl`, and optional `iconUrl`.
4. Commit the change. The public site reads `apps.json`.

## Hosting

The `.github/workflows/pages.yml` workflow publishes the repository root to GitHub Pages when changes are pushed to `main`. In repository Settings → Pages, choose **GitHub Actions** as the build and deployment source if it is not already selected.

## Admin security

The dashboard is a convenience page with links to GitHub's authenticated management screens. It does not contain a client-side password or GitHub token. Keep repository write access restricted to the owner.

## Safety

Only publish APKs you own or are authorized to distribute. Provide clear descriptions, version numbers, and minimum Android requirements.