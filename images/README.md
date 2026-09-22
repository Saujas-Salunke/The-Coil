# Images folder

This folder holds the local images used throughout The Coil, one per
article plus the homepage hero (which reuses `article-ai-campus.jpg`).

| File | Used by |
|---|---|
| `article-ai-campus.jpg` | Homepage hero + `articles/article-ai-campus.html` |
| `article-coffee.jpg` | `articles/article-coffee.html` (and the cafeteria card) |
| `article-smartphone.jpg` | `articles/article-smartphone.html` |
| `article-student.jpg` | `articles/article-student.html` |
| `article-tea.jpg` | `articles/article-tea.html` |
| `article-almonds.jpg` | `articles/article-almond.html` |
| `article-attendance.jpg` | `articles/article-attendance.html` |
| `article-calculator.jpg` | `articles/article-calculator.html` |
| `article-charger.jpg` | `articles/article-charger.html` |
| `article-playlist.jpg` | `articles/article-playlist.html` |

If you add a new article, drop a matching `.jpg` here and reference it
from the article with a relative path (articles are one folder deep, so
use `../images/your-file.jpg`), and from the homepage with `images/your-file.jpg`.
