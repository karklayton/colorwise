# ColorWise
CTO and co-founder for dental resin shade matching startup.

Built a web app that analyzes cross-polarized photos of teeth and matches the shade to the closest resin composite in a color database.

## Approach

Built a custom web component that lets a user upload a cross-polarized tooth photo, click the area to sample, and get an instant shade recommendation. RGB taken from a 100×100px region around the click point, then converted to CIELab color space.

Backend runs the sampled Lab value against a database of resin composite shades using CIEDE2000 — the perceptual color-difference formula used in professional colorimetry and returns the closest match in a set of dental colors from resin brands.

## Built With

`Wix` Velo (frontend) · `Supabase` (`PostgreSQL` + Deno Edge Functions) · CIEDE2000 color-difference `algorithm`

[Demo](./demo/demo.mp4)

## Outcome

Bootstrapped, built and validated the shade-matching pipeline end to end, from image capture through color-space conversion to database matching. Didn't pursue further after being unable to raise funding for laboratory research.
