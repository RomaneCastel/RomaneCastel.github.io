# romanecastel.github.io

Personal website, served by GitHub Pages at https://romanecastel.github.io.
GitHub Pages builds it with Jekyll on every push to `master`.

## Writing a post

1. Create a Markdown file in `_posts/` named `YEAR-MONTH-DAY-title.md`,
   for example `_posts/2026-11-20-tracking-climbers-with-vitpose.md`.
   The name sets the date and the address: `/posts/tracking-climbers-with-vitpose/`.
2. Start it with:

   ```yaml
   ---
   title: "Tracking climbers with ViTPose"
   description: "One or two sentences, shown under the title and on the home page."
   tags: [ClimbVLA, Pose estimation]
   ---
   ```

   Then write the post in Markdown below it.
3. Put images and videos in `assets/posts/<post-name>/`.
4. Commit and push. The post appears on the home page within a minute or two.

`_drafts/example-post.md` shows every formatting option (headings, code,
tables, images, captions, video). Files in `_drafts/` are never published, so
it is also the place for posts that aren't ready yet.

The Posts section and its link in the menu only appear once there is at least
one post in `_posts/`.

## Previewing locally

Needs Ruby (`brew install ruby`) and Jekyll:

```bash
gem install jekyll
```

```bash
"$(gem environment gemdir)/bin/jekyll" serve --drafts
```

(Homebrew's Ruby doesn't put gem commands on the PATH, hence the long form.)
Then open http://localhost:4000. `--drafts` also shows the posts in `_drafts/`.
Jekyll rebuilds when you save a file; refresh the page to see it.

## Layout

```
index.html            home page
_posts/               published posts (Markdown)
_drafts/              unpublished posts
_layouts/post.html    the page around each post
_includes/            pieces shared by all pages (head, menu, footer, post card)
assets/css/site.css   all styles, light and dark
assets/js/site.js     dark mode toggle, scroll animations
assets/posts/         images and videos for posts
_config.yml           Jekyll settings
cv.pdf
```
