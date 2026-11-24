# Bridge City Apps

The public site for Bridge City Apps — <https://bridgecityapps.ca>

Static HTML. No build step, no dependencies, no JavaScript. Served by GitHub
Pages, which is why this repo is public while the apps themselves are not.

```
index.html                    /                        studio landing
style.css                     /style.css               shared
muscle-loom/
  index.html                  /muscle-loom/            support
  privacy/
    index.html                /muscle-loom/privacy/    privacy policy
```

A second app is a sibling folder. Nothing about the first one moves.

## Don't edit this repo directly

`site/` in the (private) app repo is the source of truth. These files are
copied from there and pushed, so an edit made here is lost on the next sync.

Two conventions worth preserving if you do touch them:

- **Each page is an `index.html` inside a directory**, so the published URLs
  carry no `.html` and no trailing filename. Two of them are registered in App
  Store Connect as an app's Privacy Policy and Support URLs, and are addresses
  users land on for years.
- **Links between pages are relative, never root-absolute** (`../style.css`,
  not `/style.css`). The site answers at both the custom domain and
  `rdesnoyers.github.io/bridgecityapps/`, and a leading slash only resolves at
  one of them.
