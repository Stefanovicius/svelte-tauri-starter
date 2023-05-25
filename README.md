# SvelteKit + Tauri - Starter Template

This template was made following the [quick start guide](https://tauri.app/v1/guides/getting-started/setup/sveltekit) for SvelteKit, I recommend reading it as it provides some insights about the configuration of Tauri and communication with SvelteKit.

### Tauri

Tauri is a toolkit built with Rust, and the CLI leveraging Node.js, that helps developers make applications for the major desktop platforms - using virtually any frontend framework in existence.

### SvelteKit

SvelteKit is a framework for rapidly developing robust, performant web applications using Svelte. If you're coming from React, SvelteKit is similar to Next. If you're coming from Vue, SvelteKit is similar to Nuxt. It's primarily designed for Server-Side Rendering (SSR), though can be adapted for many different deployment targets using [adapters](https://kit.svelte.dev/docs/adapters).

Tauri requires SvelteKit to be used as Static-Site Generator (SSG) or a Single-Page Application (SPA), this template is pre-configured as SSG as it is recommended. If you prefer SPA mode over SSG, you can make changes as per the [documentation](https://kit.svelte.dev/docs/single-page-apps).

## Prerequisites

Read and install the [prerequisites](https://tauri.app/v1/guides/getting-started/prerequisites) first.

## Configuration

Check out `src-tauri/tauri.conf.json` to make changes to the package and window names.

## Developing

Once you've made sure to have the prerequisites and installed the dependencies via `npm install`, start the development server:

```bash
npm run tauri dev
```

## Testing

### Browser Testing

SvelteKit offers built-in Playwright support for browser testing, but since Tauri APIs don't work in Playwright, it's not recommended. Check out Tauri's [WebDriver documentation](https://tauri.app/v1/guides/testing/webdriver/introduction) for alternatives using Selenium or WebdriverIO instead of Playwright.

### Unit Testing

For unit testing [Vitest](https://vitest.dev) is pre-installed.

## Building

To create a production version of your app:

```bash
npm run tauri build
```

It will build your front-end, compile the Rust binary, collect all external binaries and resources and finally produce neat platform-specific bundles and installers. Read more on [Tauri building documentation](https://tauri.app/v1/guides/building/)
