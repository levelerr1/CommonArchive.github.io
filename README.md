# The Commons

A free, article-collecting site for you and your friends, built with Jekyll
and hosted free on GitHub Pages. No server, no database, no monthly bill.

## Get it online (fastest path — no install needed)

You don't need Jekyll installed on your computer at all. GitHub builds the
site for you automatically every time you push a change.

1. Create a free GitHub account at github.com if you don't have one.
2. Create a new repository. If you want your site at
   `https://yourname.github.io` (no extra path), name the repo exactly
   `yourname.github.io`. Any other name works too, it'll just live at
   `https://yourname.github.io/repo-name/` instead — if you do that, set
   `baseurl: "/repo-name"` in `_config.yml`.
3. Upload every file in this folder to that repository (drag-and-drop
   works fine on github.com, or use `git push` if you're comfortable
   with it).
4. In the repo, go to **Settings → Pages**, and under "Build and
   deployment" choose **Deploy from a branch**, branch `main`, folder
   `/ (root)`. Save.
5. Wait a minute or two, then visit the URL GitHub gives you. Done —
   that's your live site, for free, forever.

Every time you upload a new file or edit one, the site rebuilds itself
automatically within about a minute.

## Adding a new article

1. Go to the `_posts` folder.
2. Copy one of the two example files as a starting point.
3. Rename it to `YYYY-MM-DD-a-short-title.md` (the date must be first,
   real hyphens, no spaces).
4. Edit the top section between the `---` lines:
   - `title:` — the article's title
   - `author:` — must exactly match a name in `_data/contributors.yml`
   - `image:` — optional, path to a cover image (see below)
5. Write the article underneath in plain Markdown.
6. Upload the file to GitHub (or push it). It appears on the homepage
   automatically, newest first.

## Adding a picture

1. Drop the image file into `assets/images/` (jpg, png, or svg all work).
   Keep file sizes reasonable — under ~500KB per image loads much faster.
2. To use it as the big cover image at the top of an article, set in the
   front matter:
   ```
   image: /assets/images/your-file.jpg
   ```
3. To place an image inside the body of the article, write:
   ```
   ![description of the image](/assets/images/your-file.jpg)
   ```
   anywhere in the text.

## Adding a new friend as a contributor

Open `_data/contributors.yml` and add a new entry:

```yaml
YourFriendsName:
  initials: "XY"
  color: "#445566"
```

Then use `author: YourFriendsName` (spelled exactly the same way) in any
post they write. Their byline badge, color, and initials will show up
automatically everywhere.

## Previewing changes on your own computer (optional)

You don't need this to publish — GitHub Pages builds it for you. But if
you want to preview edits before uploading:

1. Install Ruby (ruby-lang.org has installers for every OS).
2. In this folder, run:
   ```
   bundle install
   bundle exec jekyll serve
   ```
3. Open `http://localhost:4000` in your browser. It live-reloads as you
   edit files.

## What this costs

$0. GitHub Pages hosting is free indefinitely. The only thing that ever
costs money is an optional custom domain (roughly $10–15/year), which
you can add later, whenever you want, or never.
