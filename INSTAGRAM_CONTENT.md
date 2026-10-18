# Gold Perfume — real Instagram content

> **Status:** the home-page Instagram gallery was removed, and no page reads this file yet. `instagram-content.json` keeps the verified post links for the product photos, which are not wired up. The notes below describe the old gallery and are kept for reference.

The mockup has an Instagram gallery on the homepage. It reads `instagram-content.json` and **does not invent** product images, captions, prices or posts.

## Adding posts

Copy public post/reel links from [@gold_perfume.jo](https://www.instagram.com/gold_perfume.jo/), then edit `instagram-content.json`:

```json
{
  "account": "gold_perfume.jo",
  "posts": [
    {
      "url": "PASTE_A_REAL_POST_URL_HERE",
      "caption_ar": "Paste the verified post caption",
      "caption_en": "Optional translated caption"
    }
  ]
}
```

When `image` is **omitted**, the site uses Instagram's **official embedded post**, which retrieves the original photo (assuming Instagram allows embeds in the visitor's browser). For more reliable display, save a photo that you own or have permission to use to `assets/instagram/photo-name.jpg`, then add `"image": "assets/instagram/photo-name.jpg"` to the post. The image itself will be clickable to the original Instagram post.

Do not copy CDN media URLs into the mockup for long-term use: Instagram CDN URLs may expire. The page limits display to 12 posts and only accepts links to `instagram.com/p/`, `/reel/`, or `/tv/`.

The **product catalogue, prices, reviews, delivery and contact information** are still demo content in `index.html` until authentic product records are separately supplied. Social posts are not automatically converted into product listings, and an Instagram account URL alone cannot be read from a static GitHub Pages website without Meta API access.

For an automatic synchronized feed later, use Meta's supported Instagram Graph API with the business owner's permission and keep any access token on a backend/serverless worker — never in public frontend code.
