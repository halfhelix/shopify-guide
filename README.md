
# Shopify Guide

A mostly reasonable approach to Shopify theme development

## A note on the language:

- "Avoid" means don't do it unless you have good reason.
- "Don't" means there's never a good reason.
- "Prefer" indicates a better option and its alternative to watch out for.
- "Use" is a positive instruction.

## High-Level Rules

- Use Gulp, unless you have a good reason not to.
- Always commit your work to git after a feature is complete
- Always Use .SCSS flavor of SASS
- Use snippets/partials whenever possible
- [Shopify Docs](https://help.shopify.com/api) are your friend.
- When in doubt, copy the [Timber theme](https://github.com/Shopify/Timber) design patterns
- Use [Shopify Image Filters](https://www.shopify.com/partners/blog/the-img_url-filter-just-got-10x-better) to server properly sized media files.
- Use Shopify Theme Options for common variables, such as email, social links, hours
- Use Shopify Pages for static content.
- Use Shopify Blogs are looped content.
- Avoid deeply nested naviagtions.
- Avoid customizing checkout (Shopify Plus Only)

# Starter Theme

## Shopify Helix
User the Shopify-Helix starterkit unless there is a good reason not to.

https://github.com/halfhelix/shopify-helix

- SCSS Paritials
- Modular Javascript + ES6
- Gulp-based file syncing
- Minification

# Shopify Workflow

Shopify does not have a local server or git deployment strategy. This means it's extremely easy to either 1) overwrite a team members work or 2) introduce bugs into a live site. To avoid this, you should follow a development workflow that works with the SHopify system.

## Steps to make a feature

1. Setup your machine
* Create a branch
* Log into [Shopify Admin > Themes](https://YOUR_DOMAIN.myshopify.com/admin/themes)
* Duplicate the live theme
* Rename newly duplicated theme your branch name
* On your new theme, click `Customize Theme`
* Note the Theme ID in the URL (it should be the only integer in the URL)
* **IMPORTANT** paste the branched Theme ID into the `theme_id` value in `config.yml`
* Run Gulp
* Code all the things, and your changes will automatically be pushed up to the unpublished theme of the Theme ID you identified
* **IF** you change any theme settings on your branch (in the Shopify customize theme WYSIWYG), run `theme download config/settings_data.json` and commit that with your PR.
* Finish the feature, make a PR
* Merge the PR to `master`

# Snippets

Just a bunch of handy snippets to perform routine/desired tasks on Shopify.

## TODO:

- [ ] Product Image Zoom - Some javascript that works will with Slick Slider
- [ ] Ajax search / Algolia Search - Suggestive Search
- [ ] Advanced Collection Filters - Filter Product Catalog with Ajax
- [ ] Mega Menu / Deep Nested Forms - How deep can we nest navigations in a sane way?
- [ ] Currency Converter Ajax - We can probably do with thisout an app using Ajax and a currenly conversion API
- [ ] Email Sign Up Popup - Something simple w/ come cookies to avoid usaing useless apps.
- [ ] New Shopify Content Blocks - The draggable content blocks. Maybe a fre pre-styles blocks to plug & play.
- [ ] Related Products - Probably using tags? Or Vendor? Or Both? We should probably make this flexible.
- [ ] Catalog Grid Item
   - Image Fallbacks
   - Alt Image On Hover
   - Price + Sale Price
   - Badges - Sale, Low Stock, Featured, Out Of Stock
   - Buy It Now
   - Color Varients
- [ ] Dynamic Product Varient w/ Option.js for Selects
- [ ] 'View Per Page' toggle - Let the user choose how many products should be on a page
- [ ] Collections Page - How doe we deal with images?
- [ ] Advanced Product Options - Change images and sub-options when choosing different varients

## Usage

Take a look at the subfolder to see related snippets bundled together, along with their installation instructions.
