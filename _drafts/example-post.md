---
title: "Example post: how posts are written"
description: "One or two sentences. Shown under the title and on the home page card."
tags: [ClimbVLA, Pose estimation]
---

This file is a **draft**: anything in `_drafts/` is never published. Copy it
into `_posts/` with a date in the file name to publish it, for example
`_posts/2026-11-20-tracking-climbers-with-vitpose.md`.

The first paragraph is used as the summary when there is no `description`.

## A section heading

Normal Markdown works: *italics*, **bold**, [links](https://github.com/RomaneCastel),
and `inline code`.

- Bullet lists
- with several items

1. Numbered lists
2. too

> A quote, for a key result or something someone said.

## Code

```python
def keypoints_visible(scores, threshold=0.5):
    """ViTPose outputs below the threshold count as not visible."""
    return [s >= threshold for s in scores]  # 17 COCO joints
```

## A table

| Pose model | PCK@0.2 | Speed |
|---|---|---|
| ViTPose-B | 0.00 | 0.2 s/frame |
| RTMPose-m | 0.00 | 0.05 s/frame |

## Images and videos

Put files in `assets/posts/<post-name>/`, then:

```markdown
![Skeleton overlay on a climbing video](/assets/posts/tracking-climbers/overlay.png)
```

For a caption, or a video:

```html
<figure>
  <img src="/assets/posts/tracking-climbers/overlay.png" alt="Skeleton overlay">
  <figcaption>ViTPose keypoints drawn on every frame.</figcaption>
</figure>

<video src="/assets/posts/tracking-climbers/overlay.mp4" controls muted playsinline></video>
```

Keep videos short and small (a few MB): GitHub rejects files over 100 MB, and
large files make the page slow.
