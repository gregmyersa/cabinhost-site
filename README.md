# cabinhost-site

The website for cabinhostconsulting.com. Netlify publishes the `site/` folder straight from this repo
(`netlify.toml`: publish = "site", no build step).

```
site/                  everything Netlify serves (pages, blog/, assets/, sitemap.xml, robots.txt, _redirects)
content/posts/         markdown source of each studio-written post (title, description, category, body)
legacy-backup/blog/    the old dark-theme HTML of 16 posts, kept in case you want to compare (not published)
```

Posts are created by **cabinhost-studio**; it edits `site/blog/index.html` (between the `AUTO-POSTS` markers),
`site/sitemap.xml` (between the `AUTO-SITEMAP` markers), and adds `site/blog/<slug>.html` + `content/posts/<slug>.md`.
Don't delete those marker comments.
You can still edit the other pages by hand and commit them; Netlify redeploys on every push.
