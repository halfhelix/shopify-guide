
# Shopify Guide

A mostly reasonable approach to Shopify theme development

# Starter Theme

## Shopify Helix
https://github.com/halfhelix/shopify-helix

- SCSS Paritials
- Modular Javascript + ES6
- Gulp-based file syncing

# Snippets

Just a bunch of handy snippets to perform routine/desired tasks on Shopify.

## TODO:

[] Product Image Zoom - Some javascript that works will with Slick Slider
[] Ajax search / Algolia Search - Suggestive Search
[] Advanced Collection Filters - Filter Product Catalog with Ajax
[] Mega Menu / Deep Nested Forms - How deep can we nest navigations in a sane way?
[] Currency Converter Ajax - We can probably do with thisout an app using Ajax and a currenly conversion API
[] Email Sign Up Popup - Something simple w/ come cookies to avoid usaing useless apps.
[] New Shopify Content Blocks - The draggable content blocks. Maybe a fre pre-styles blocks to plug & play.
[] Related Products - Probably using tags? Or Vendor? Or Both? We should probably make this flexible.
[] Catalog Grid Item
   - Image Fallbacks
   - Alt Image On Hover
   - Price + Sale Price
   - Badges - Sale, Low Stock, Featured, Out Of Stock
   - Buy It Now
   - Color Varients
[] Dynamic Product Varient w/ Option.js for Selects
[] 'View Per Page' toggle - Let the user choose how many products should be on a page
[] Collections Page - How doe we deal with images?
[] Advanced Product Options - Change images and sub-options when choosing different varients

## Usage

Take a look at the subfolder to see related snippets bundled together, along with their installation instructions.

# Shopify Workflow

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
