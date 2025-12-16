# 6S Builders Documentation

This folder contains documentation for the 6S Builders website and integration guides.

## Contents

### [Web Analytics Guide](./web-analytics-guide.md)

A comprehensive guide for getting started with Vercel Web Analytics on your project. This guide covers:

- Prerequisites for setting up Web Analytics
- How to enable Web Analytics in the Vercel dashboard
- Framework-specific implementation instructions for:
  - Next.js (Pages and App Router)
  - Remix
  - Nuxt
  - SvelteKit
  - Astro
  - Create React App
  - Vue
  - Plain HTML (static sites)
  - Other frameworks
- How to add the `@vercel/analytics` package
- Deployment instructions
- How to view analytics data in the dashboard
- Next steps for learning more

## Current Implementation

The main `index.html` file has been updated with Vercel Web Analytics integration. The analytics script has been added to the `<head>` section and will automatically track visitor data once the site is deployed to Vercel.

### How Analytics Was Added

For this static HTML project, we use the HTML implementation of Vercel Web Analytics:

```html
<!-- Vercel Web Analytics -->
<script>
  window.va = window.va || function () { (window.vaq = window.vaq || []).push(arguments); };
</script>
<script defer src="/_vercel/insights/script.js"></script>
```

This approach:
- ✅ Requires no npm packages for static sites
- ✅ Automatically tracks page views
- ✅ Works with the Vercel deployment pipeline
- ℹ️ Does not include route support (specific to static HTML sites)

## Quick Start

1. **Enable Web Analytics** in your Vercel project dashboard
2. **Deploy** your project to Vercel
3. **Wait a few minutes** for the analytics to begin collecting data
4. **View your data** in the Vercel dashboard under the Analytics tab

## Resources

- [Vercel Analytics Documentation](https://vercel.com/docs/analytics)
- [Vercel Dashboard](https://vercel.com/dashboard)
- [Setting Custom Events](https://vercel.com/docs/analytics/custom-events)
- [Privacy and Compliance](https://vercel.com/docs/analytics/privacy-policy)
