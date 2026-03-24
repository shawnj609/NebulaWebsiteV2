# Repository Notes

## Image Asset Standard

This repository uses `.webp` for static image assets.

If a photo or other static image enters the repo in a different format, it should be converted to `.webp` before being used on the website.

Do not add non-WebP static image assets to production page content unless there is a specific exception that has been explicitly approved.

## Photo Inbox

The `photo_inbox/` folder is a staging area for raw photos that are not yet prepared for the website.

Use this folder for:
- New photos that still need cropping, resizing, compression, or renaming
- Source images that have not been placed into any page yet
- Temporary review selections before final website-ready assets are chosen

Do not use this folder for:
- Final production assets that are already referenced by the website
- Long-term storage of finished images
- Any files that should be tracked in git

`photo_inbox/` is intentionally ignored by git and should remain untracked.

## How To Add Photos To The Website

When adding new photos to the site in the future:

1. Drop the original files into `photo_inbox/`.
2. Review the images and choose the final ones that belong on the site.
3. Crop and resize them for their target layout so they are not larger than necessary.
4. Convert the selected image to `.webp`.
5. Rename the final files with clear, descriptive names.
6. Move the finished assets out of `photo_inbox/` and into a tracked location in the repo that matches the page or feature using them.
7. Update the relevant HTML to reference the finalized asset paths.
8. Verify the page locally to confirm the image displays correctly and looks good on desktop and mobile.

## How To Convert Images To WebP

Use `ffmpeg`, which is available in this environment.

Example:

```bash
ffmpeg -y -i photo_inbox/IMG_9555.png -c:v libwebp -quality 85 photo_inbox/IMG_9555.webp
```

Notes:
- Replace `IMG_9555.png` with the source filename you are converting.
- Keep the original file in `photo_inbox/` until the final website asset is approved.
- The `.webp` file can stay in `photo_inbox/` during review, but production HTML should point to a finalized tracked asset outside that folder.
- `-quality 85` is a good default for web use unless a different size or quality target is needed.

## Guidance For Future Agents

If asked to add photography to the website:

- Treat `photo_inbox/` as raw input only.
- Never reference files directly from `photo_inbox/` in production HTML.
- Prefer optimized final assets in tracked folders.
- Keep filenames readable and stable so future edits stay simple.
