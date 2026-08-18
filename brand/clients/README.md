# Client logos

Empty for now, and that is deliberate.

The `#clients` slot on the home page currently shows a proof strip that links
into `work.html`, because a logo sitting under a "companies running on Engaz"
heading is read as a claim of a real client relationship. Inventing one — or
borrowing a company's mark without asking — misleads every prospect who
scrolls past it. The logo grid is still in `index.html` directly below that
strip, carrying the `hidden` attribute, ready for real logos.

## Adding a real logo

1. Drop the file here. SVG preferred; otherwise a transparent PNG at roughly
   320x104. Name it after the client in lowercase with hyphens, e.g.
   `acme-medical.svg`.
2. In `index.html`, find `<ul class="clients-grid …" hidden>` and remove the
   `hidden` attribute.
3. Fill a slot:

   ```html
   <li class="client">
     <img src="brand/clients/acme-medical.svg" alt="Acme Medical"
          loading="lazy" width="160" height="52">
   </li>
   ```

4. Delete the placeholder slots you do not need — the grid reflows on its own.

Once a few real logos are in place, consider dropping the proof strip and
letting the logos carry the section, or keep both.

## The consent rule

Only add a logo once that client has given **written** consent to appear.
A signed contract is not consent to be named publicly; ask separately, and
keep the reply. The line under the section — "we show a client's logo only
with their written consent" — has to stay true.
