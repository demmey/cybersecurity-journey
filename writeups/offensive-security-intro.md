# Offensive Security Intro — TryHackMe

**Date completed:** 2026-06-28
**Difficulty:** Easy
**Category:** General

## What this room covers
An intro room that walks through the idea that pages on a website can be "hidden" from normal navigation (not linked anywhere visible) but are still fully reachable if someone finds or guesses the URL.

## My approach
1. First I went through the room expecting that an unlisted page would be inherently safer just because it's not advertised anywhere.
2. Then I saw that "hidden" just means *not linked* — it doesn't mean *protected*. If you know or discover the URL, you're in.
3. This led me to think about real-world examples — like a banking site with an unlinked admin or transfer page. If there's no login check on that page, anyone who finds the URL could potentially access account actions (e.g. moving money) without ever authenticating.

## Tools used
- Browser — manually navigating to discover/access the hidden page

## Key commands / techniques

```
birb http://example.com (to find hidden unlinked pages)
```

## What I learned
"Security through obscurity" isn't real security. A page being hidden from menus/navigation means nothing on its own — the only real fix is requiring proper authentication (login) before sensitive actions or data are accessible, regardless of whether the page is "found" or not.

## What I'd do differently next time
Nothing major for this room — it was a short, clear intro. Going forward, I want to start paying attention to *how* pages like this get discovered in the first place (e.g. directory brute-forcing, robots.txt, leaked links) since that's the next logical question this room raised for me.
