# Mockups

Website mockups for clients, served from GitHub Pages. Each mockup is one folder under `sites/`, and the URL query picks which one opens:

```
https://khgs2411.github.io/mockups/?mockups=israeltechforce
```

The value is normalised (lowercased, spaces and punctuation removed), so `?mockups=Israel Tech Force` opens the same mockup.

## Add a mockup

1. Create `sites/<name>/index.html`, where `<name>` is lowercase letters and digits only.
2. Add `<meta name="robots" content="noindex, nofollow">` to its `<head>`.
3. Commit to `master`. Pages publishes it within a minute or two.

The root `index.html` loads the chosen site in a full-screen frame, so the address keeps its query. It does not list the mockups: each client only sees the link they are given.

## Preview locally

```bash
python3 -m http.server 5181
```

Then open `http://localhost:5181/?mockups=israeltechforce`.
