---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "publish-post"
    },
    {
      "type": "capability",
      "id": "add-comment"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "app/Rules/ImageUpload.php"
    }
  ]
}
---

# A post or comment carries up to 3 images of up to 8 MB and 4000 by 4000 pixels

Images are JPEG, PNG, GIF or WebP and at least two fifths as wide as they are tall.
