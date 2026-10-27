# farmdata
Example farm data

## Lecture notes

- [Analyzing data (English)](2026/Lectures.md)
- [Datatalous (Finnish)](2026/Luennot.md)

The Markdown versions are being revised for autumn 2026. Lecture 1 retains its
original content; sessions 2–8 are pending revision.
Lectures 1–7 link to separate exercise files in both languages. Exercise 1 contains
the Fibonacci assignment; exercises 2–7 are placeholders pending revision.
Images used by the lecture notes are stored in `2026/assets/`.

## Adding images to Markdown

To include an image in a Markdown file, use the following syntax:

```markdown
![alt text](image_path)
```

**Examples:**

1. **Basic image reference:**
   ```markdown
   ![A farm landscape](2026/assets/farm.png)
   ```

2. **With custom dimensions (HTML syntax):**
   ```markdown
   <img src="2026/assets/analyzing-data/media/image5.png" style="width:5.83333in;height:3.36458in" />
   ```

3. **Relative path from the Markdown file location:**
   ```markdown
   ![Description](assets/analyzing-data/media/image5.png)
   ```

**Tips:**
- Always provide descriptive `alt text` for accessibility
- Store images in organized subdirectories under `2026/assets/`
- Use relative paths for portability
- For precise sizing, use HTML `<img>` tags with style attributes
- Supported formats: PNG, JPG, GIF, SVG
