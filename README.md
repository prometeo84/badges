# Badges (public)

This repository is intended to host public badges generated from the private `apusystem` repository. Files under `validators/` are served via GitHub Pages.

Placeholders exist here to allow first push from the private repo workflow.

## Public endpoint

- JSON: https://prometeo84.github.io/badges/validators/validators-badge.json

The JSON follows Shields.io endpoint schema and is published to the `gh-pages` branch by the private repository workflow (`publish-badge.yml`).

## Usage examples

- Markdown (README):

    ```markdown
    ![validators](https://img.shields.io/endpoint?url=https%3A%2F%2Fprometeo84.github.io%2Fbadges%2Fvalidators%2Fvalidators-badge.json&style=flat-square)
    ```

- HTML:

    ```html
    <img
        src="https://img.shields.io/endpoint?url=https%3A%2F%2Fprometeo84.github.io%2Fbadges%2Fvalidators%2Fvalidators-badge.json&style=flat-square"
        alt="validators badge"
    />
    ```

- Twig (example used in the application login page):

    ```twig
    <a href="https://prometeo84.github.io/badges/validators/validators-badge.json" target="_blank" rel="noopener noreferrer">
        <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Fprometeo84.github.io%2Fbadges%2Fvalidators%2Fvalidators-badge.json&style=flat-square" alt="Validators badge (public)" onerror="this.onerror=null;this.src='{{ asset('badges/validators-badge.svg') }}';" />
    </a>
    ```

## Notes

- The private repository workflow uses a GitHub App to authenticate and push the JSON into this repo. See `.github/workflows/publish-badge.yml` in the private repo for details (secrets used: `BADGES_APP_ID`, `BADGES_APP_PRIVATE_KEY`).

--
Generated and published by the `apusystem` CI workflow.
