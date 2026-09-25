# Proposed Reddit Data API Use

## Status

Gikachbot has not been granted Reddit Data API access. The integration
described here is the proposed behavior if Reddit approves the application.
It will not be activated with Reddit Data API credentials before approval.

## Purpose and user benefit

A user voluntarily sends Gikachbot the URL of one public Reddit post. The bot
uses read-only access to retrieve that specific post's title, self-text,
author attribution and public media metadata. It returns the result to the
same requesting Telegram chat and includes the Reddit username and canonical
link to the original post.

The benefit is an accessible, consistent presentation of an individual post
inside a user's existing Telegram workflow. The service is non-commercial.

## Requested scope

- Individual public, non-NSFW posts explicitly submitted by users.
- Read-only post metadata required to process the submitted URL.
- No private, quarantined, deleted, suspended or otherwise restricted content.
- No subreddit feeds, search, crawling, bulk collection, monitoring or export.
- No votes, posts, comments, direct messages or moderation actions.
- No advertising, profiling, surveillance, sale of data or AI/ML training.

## Why Devvit is not suitable

The utility operates outside Reddit, inside Telegram, and responds to a URL
that a Telegram user provides. It does not run inside, administer or interact
with a particular subreddit, so an in-Reddit Devvit application cannot provide
the requested Telegram workflow.

## Access and limits

If approved, Reddit metadata access will use Reddit-authorized OAuth endpoints
with an identifiable user agent. The Reddit integration will enforce a limit
of 30 user-initiated post requests per hour and an initial operational target
below 100 requests per day. Reddit rate-limit responses will be honored without
attempting to bypass them.

The approved integration will not use browser cookies, automated scraping or
third-party Reddit download services as substitutes for Reddit API metadata.

## Retention and attribution

- Request-scoped media files are deleted immediately after the Telegram send
  completes or fails.
- Minimal callback metadata may be retained for up to 24 hours and is then
  removed automatically.
- Results identify the applicable Reddit username, clearly identify Reddit as
  the source and link to the canonical Reddit post.
- Content that Reddit marks unavailable will not be intentionally retrieved or
  newly displayed through the approved integration.

## App account behavior

The application does not operate a Reddit bot account and does not post,
comment, vote or communicate with Redditors. Its Telegram username is
[@gikachbot](https://t.me/gikachbot).

