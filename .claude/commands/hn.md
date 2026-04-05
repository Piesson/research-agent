---
description: Hacker News daily digest - Top 10 stories with top 5 comments each
---

# HN Digest

## Phase 1: Fetch Top Stories

Call this URL with WebFetch:
https://hn.algolia.com/api/v1/search?tags=front_page&hitsPerPage=10

Extract from JSON response (.hits array):
- objectID (story ID)
- title
- url (external link) or story_text (for Ask HN etc.)
- points
- num_comments
- author
- created_at

## Phase 2: Fetch Comments for Each Story

For each of the 10 stories, call WebFetch:
https://hn.algolia.com/api/v1/items/{objectID}

From the response, extract .children array (direct comments only, not nested replies).
Sort children by points descending, take top 5.
For each comment, use: author, points, text (strip all HTML tags cleanly).

Skip comments with null/empty text (deleted/dead comments).

## Phase 3: Format & Output

Print the full digest using today's date from MEMORY.md context (currentDate).

---

# 🟠 HN Digest — {today's date}

For each story (1–10):

## {rank}. {title}                              ⬆ {points} | 💬 {num_comments}
🔗 {domain extracted from url} · {url}

**Top Comments:**
• **{author}** ({points}pts): "{first 200 chars of comment text}..."
  → 한: {1-2 sentence Korean summary of what the commenter is saying}

[repeat for top 5 comments, skip if fewer available]

---

[repeat for all 10 stories]

---

*Powered by Algolia HN API · fetched at {current time KST}*

---

## Notes

- Domain extraction: parse just the hostname from the URL (e.g. "github.com", "arxiv.org")
- If a story has no external URL (Ask HN, Show HN), show "news.ycombinator.com" as domain
- HTML stripping: remove all `<p>`, `<a href="...">`, `</a>`, `<i>`, `</i>` etc. tags from comment text
- If a story has fewer than 5 comments, show all available
- Korean summaries should capture the commenter's main point, not just translate word-for-word
