# Full-page screenshots

Capture comparable full-page screenshots before and after interface changes. Use the browser tool available to the agent. Read its documentation before selecting a capture method. Do not assume that a tool supports standard Playwright syntax or options.

## Capture and compare

1. Start or use the local preview. Make sure its build matches the source before changes.
2. Open the page in a browser with a supported full-page capture method.
3. Set a fixed viewport, such as 1440 × 1000 for desktop or 390 × 844 for a narrow screen. Use the user's requested sizes when supplied. Record the viewport and zoom.
4. Wait for the page, fonts, and images to load. If content loads only after scrolling, reveal it and wait for it to load. Return to the starting position and set the interface state for comparison.
5. Save the before screenshot **before editing**. Use the supported full-page capture option. Save to an absolute file path. If the tool returns image bytes, save them with a supported file method before continuing.
6. Open and inspect the saved image. Check that it includes the complete page, including the header and footer when present. Check for missing content, cut edges, repeated sections, and incorrect image joins.
7. Make the interface changes. Rebuild if needed, reload the page, and confirm that the preview shows the changed source. Wait for content, fonts, and images again.
8. Restore the same viewport, zoom, and interface state. Keep form values, expanded sections, focus, and displayed data consistent where possible. Record differences that could affect the comparison.
9. Save and inspect the after screenshot with the same capture method. The page height can differ. Do not overwrite the before image.
10. Keep both files. Record their absolute paths, page, viewport, and interface state. Show requested before and after images with clear labels. Specialists must confirm that they opened the supplied files.

## If capture fails

Use another supported capture method or browser. Do not repeat a failed method without correcting its cause. Do not present a broken capture as complete.

If only viewport captures work, save labeled images of the visible page areas. State that these are partial captures. Report missing areas and any limits on comparison. If the before capture failed and changes have started, do not label an image of the changed interface as the before image.

## Standard Playwright example

Use this example only when the available tool supports these methods and options. Replace the example path with an absolute output path for the task. Use a separate path for the after image.

```javascript
await page.setViewportSize({ width: 1440, height: 1000 });
// Wait for page content, fonts, and images before capture.
await page.screenshot({
  path: "/absolute/output/before.png",
  fullPage: true,
});
```

Some browser tools use different methods or return image bytes without saving a file. Follow the available tool's documentation. Confirm that the saved file can be opened before reporting success.
