# Toddler Playtime Privacy Package

This repository contains a production-grade privacy and Google Play disclosure package for:

- App: Toddler Playtime
- Package: com.bkapp.toddlersplaytime
- Platform: Android (Google Play)

## Files

- index.html: Full policy package with both strict variants, Data Safety mapping, Play Console answer drafts, and compliance checklist.
- style.css: Presentational style for GitHub Pages.

## Publish on GitHub Pages

1. Push this folder to a GitHub repository.
2. Open repository Settings -> Pages.
3. Under Build and deployment:
   - Source: Deploy from a branch
   - Branch: main (or your default branch)
   - Folder: / (root)
4. Save settings.
5. Wait for the Pages deployment to finish.
6. Copy the published URL and place it in the Google Play Console Privacy Policy field.

## Required Placeholder Replacements

Before publishing, replace all placeholders in index.html:

- REPLACE_WITH_MY_EMAIL
- REPLACE_WITH_DATE
- REPLACE_WITH_ENTITY
- REPLACE_WITH_SUPPORT_URL
- REPLACE_WITH_ENTITLEMENT_RETENTION_DAYS
- REPLACE_WITH_PURCHASE_LOG_RETENTION_DAYS
- REPLACE_WITH_BACKEND_URL (Variant B)

## Variant Selection Guidance

- Use Variant A only if your shipped build does not send purchase tokens to your backend.
- Use Variant B if your shipped build sends purchase tokens or purchase metadata to backend verification services.
- If architecture changes between releases, update policy text and Data Safety answers before rollout.

## Update Workflow for Every Release

1. Confirm whether billing flow is Variant A or Variant B in live code.
2. Verify all SDKs and network endpoints in production build.
3. Update policy sections and retention windows.
4. Reconcile with Play Data Safety form answers.
5. Republish GitHub Pages and validate public URL.

## Legal Note

This package is intended as a strict operational draft for Play review and audit readiness. Obtain legal review for country-specific compliance requirements.
