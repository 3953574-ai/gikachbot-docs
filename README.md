# Gikachbot

Gikachbot is a small, non-commercial Telegram utility that processes links
explicitly submitted by its users. It returns the text and, when available,
media from an individual public post together with author attribution and a
link to the original source.

- Telegram: [@gikachbot](https://t.me/gikachbot)
- Privacy policy: [PRIVACY.md](PRIVACY.md)
- Proposed Reddit API use: [REDDIT_DATA_ACCESS.md](REDDIT_DATA_ACCESS.md)

## User-initiated operation

The bot does not crawl feeds or communities. Processing begins only after a
user sends the URL of a specific post. The result is returned to the same
Telegram chat that requested it.

## Data handling

- Temporary media files exist only while a request is processed and are
  removed after success, failure, timeout or cancellation.
- Minimal callback metadata may be cached for up to 24 hours so that Telegram
  buttons can operate. It is then removed automatically.
- Translation is optional and begins only after the user presses the
  translation button.
- The service does not sell data, build user profiles or use content for
  advertising or AI/ML training.

## Contact

For documentation or privacy questions, open a GitHub issue without including
private account information. A private contact method can then be arranged if
identity verification is required.

