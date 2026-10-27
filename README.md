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

**Important:** Image paths are relative to the location of the Markdown file itself, not the repository root.

**Examples:**

1. **For files in the repository root (e.g., README.md):**
   ```markdown
   ![A farm landscape](2026/assets/farm.png)
   <img src="2026/assets/analyzing-data/media/image5.png" style="width:5.83333in;height:3.36458in" />
   ```

2. **For files in `2026/` subdirectory (e.g., Lectures.md, Harjoitus1.md):**
   ```markdown
   ![A farm landscape](assets/farm.png)
   <img src="assets/analyzing-data/media/image5.png" style="width:5.83333in;height:3.36458in" />
   ```

3. **For files in nested subdirectories, use `../` to go up:**
   ```markdown
   ![Example](../assets/analyzing-data/media/image5.png)
   ```

**Tips:**
- Always provide descriptive `alt text` for accessibility
- Remember that relative paths are from the Markdown file's location, not the repo root
- Store images in organized subdirectories under `2026/assets/`
- For precise sizing, use HTML `<img>` tags with style attributes
- Supported formats: PNG, JPG, GIF, SVG
