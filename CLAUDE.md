# Afterthought

Personal reading timeline website for recording and reviewing book/podcast reflections.

## Tech Stack

- Single HTML file (`index.html`) with embedded CSS and JavaScript
- No build tools or dependencies
- Deployed on GitHub Pages: https://kaka-jun.github.io/afterthought/

## Data Structure

Content entries are stored in the `contentData` array (around line 480). Each entry:

```javascript
{
  title: "书名",
  author: "作者",
  type: "book" | "podcast",
  date: "YYYY-MM-DD",
  rating: number | null,  // out of 10
  tags: ["tag1", "tag2"],
  review: `多行读后感内容`
}
```

Entries are sorted by date (newest first) and grouped by year.

## Important Conventions

- Use template literals (backticks) for multi-line reviews
- Use Chinese quotes 「」 instead of "" inside review text to avoid JavaScript parsing errors
- Use ● for bullet points, not numbered lists (1. 2. 3.)
- Dates use YYYY-MM-DD format

## Adding New Entries

1. Add entry to the beginning of `contentData` array
2. Commit and push to GitHub
3. Site auto-updates via GitHub Pages (may take 1-2 minutes)

## Deployment

```bash
git add index.html
git commit -m "描述"
git push
```

GitHub account: `kaka-jun`

## Features

- Dark/light mode toggle (persisted in localStorage)
- Search by title, author, tags, or review content
- Filter by type (book/podcast)
- Year summaries (pre-generated, stored in `yearSummaries` object)
- Expandable review cards

## Privacy Note

The entry "斯坦福人生设计课 - 人生仪表盘评估" contains personal content about relationships/partner.
