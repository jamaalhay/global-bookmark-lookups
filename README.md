# Global Bookmark lookups

This page identifies the HTTP client behind the User-Agent
`GlobalBookmark/1.0 (+https://github.com/jamaalhay/global-bookmark-lookups)`.

Global Bookmark is a personal bookmarking app. When its owner saves a book, film or
show, the app's server looks up that one title, for example on Open Library, to show
basic facts and a source link.

How it behaves:

- One owner, low volume: a lookup happens only when something is saved.
- Requests are made one at a time, never in parallel, and respect the provider's
  published rate limits.
- Answers are cached (30 days for found titles, 7 days for "not found"), so the same
  title is not requested again.
- No scraping, crawling or bulk download.

To report a problem or ask us to change how we call your service, please
[open an issue](https://github.com/jamaalhay/global-bookmark-lookups/issues) in this
repository.
