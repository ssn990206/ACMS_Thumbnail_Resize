# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

ACMS content administrators who manage localized thumbnail assets for content distributed across many countries.

## Product Purpose

ACMS lets administrators attach multiple image and video thumbnail variants to a content item. Country targeting lets them adapt faces, skin tones, and text or language embedded in thumbnails while keeping a global default as the baseline.

## Operating Context

Thumbnail info is organized by country set. The main content page always shows Default Set first, followed by any added country sets, and previews only the first field (`Placeholder Image(Video Thumbnail)`) from each set. Administrators add common country sets or a Custom Set from the main page. `Edit Thumbnail` opens the full editor, where every existing set exposes all six thumbnail fields without an introductory helper sentence. Each set assigns one or more countries and may replace any subset of the default thumbnail assets. The country list contains more than 30 countries.

Main Thumbnail info summary previews preserve the uploaded Thumbnail's original aspect ratio within the summary column instead of cropping or stretching it into a fixed 1:1 frame. Empty `edit thumbnail` upload tiles retain their fixed size.

The page title is `Edit Multiple Mix`, left-aligned above a two-column desktop layout. `Basic Info` and `Thumbnail info` use equal-width columns, with Thumbnail info on the right. Before content selection, both sections show `Need to select content first`; only Basic Info exposes the `Select Content` action. Select Content opens a modal with Type, Category, and Style selectors plus a scrollable Style Configuration preview. Cancel or Escape closes it without changing the page; Save adds the selected content. After saving, Basic Info shows the required `Style Name` input, while Thumbnail info reveals Default Set, country-set actions, and `Edit Thumbnail`. The left navigation can collapse to a compact icon-oriented rail and expand again; narrow screens stack the page content into one column.

## Capabilities and Constraints

- Every country may have its own thumbnail configuration.
- Multiple countries may share one configuration.
- Countries without an override automatically inherit the default thumbnails from the main content form.
- A country configuration may replace only selected thumbnail fields; all remaining fields inherit their default values.
- The main page provides direct add buttons for Eastern Set, Japan Set, Taiwan Set, and Custom Set; the full editor does not duplicate this add action.
- Eastern Set includes Hong Kong, Indonesia, Japan, Korea (Republic of Korea), Malaysia, Philippines, Singapore, Taiwan, and Thailand.
- Country membership becomes read-only after a set is created. To change the countries, administrators delete the set from the main-page summary and add a new one.
- Custom country selection is grouped by region without search and prevents overlap with existing sets.
- Thumbnail upload areas are directly clickable; there are no separate Override or Replace buttons.
- Uploaded images and videos render inside their thumbnail fields at their actual aspect ratio. In the editor, the top-right controls are vertically stacked: replace first, then remove directly underneath for optional fields; the bottom-right control downloads the file. Clicking the media opens a full-screen preview over a 40% black backdrop.
- On the main Thumbnail info summary, clicking any set's `edit thumbnail` tile opens the Edit Thumbnail popup whether or not that set already has an image. Full-screen media preview remains available inside the editor.
- Uploading one editor cell updates only that cell; other country-set cells do not visually fill from the Default Set.
- Country summaries list every included country without truncation.
- Image and video placeholders use only the labels `image` and `video`.
- Thumbnail fields include Placeholder Image(Video Thumbnail), Video Thumbnail, Placeholder Image (3:4 Video Small Thumbnail), 3:4 Video Small Thumbnail, Placeholder Image (9:16 Video Large Thumbnail), and 9:16 Video Large Thumbnail.
- Placeholder Image(Video Thumbnail) and Video Thumbnail are required. After Video Thumbnail is uploaded for a set, its cell shows Auto Resize. Auto Resize uses the original Video Thumbnail's first frame for Placeholder Image(Video Thumbnail), creates a 3:4 Video Small Thumbnail at `FPS 18 · 270 × 360` and uses that resized video's first frame for its Placeholder Image, then creates a 9:16 Video Large Thumbnail at `960 × 1280` and uses that resized video's first frame for its Placeholder Image. The operation affects only that set.
- Uploaded image fields show `File Size` and `Dimensions` metadata below the preview. Uploaded video fields, including Video Thumbnail, show `File Size`, `Dimensions`, and `FPS`. File Size is presented in B, KB, MB, or GB; Dimensions use pixels, for example `1080 × 1920 px`.
- Full-screen media preview renders at the media's actual pixel dimensions rather than fitting it down to the viewport. Media larger than the viewport scrolls inside the preview, and an `Actual Dimensions` badge remains visible at the bottom.

## Evidence on Hand

The supplied ACMS screenshot is the visual and terminology reference. No production data ranges beyond a country list of more than 30 entries have been supplied.

## Product Principles

- Explain inheritance once at the modal level instead of repeating status labels in every thumbnail.
- Optimize for country groups and exceptions instead of repetitive country-by-country entry.
- Preserve partial overrides so localized changes do not duplicate unaffected assets.
- Prevent overlapping country assignments from creating ambiguous delivery behavior.
