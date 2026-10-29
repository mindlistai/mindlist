# One example per task

The titles and links below are made up.

## Find what I saved about X

The person: "What did I save about pricing pages?"

1. search_items with query "pricing pages", limit 10, via "skill".
2. The answer:

   Here is what you saved about pricing pages, best match first:
   1. **How we redesigned our pricing page** (blog.example.com, saved 12 Oct). Three tiers beat four in their test. https://blog.example.com/pricing
   2. **Pricing page teardown** (video.example.com, saved 3 Oct). A walk through ten SaaS pricing pages. https://video.example.com/teardown

   Want me to open one of them?

## Use my saves in this task

The person, in Claude Code: "Use my saves for this onboarding flow."

1. The topic, from the files at hand: "first-run onboarding for a web app".
2. search_items three times: "onboarding", "first run checklist", "activation", each with via "skill".
3. get_item for the 3 saves that fit.
4. The work, with each idea cited by title and link, then: "Used: A, B, C. Skipped: D (about mobile only)."

## Turn saves into a brief or a spec

The person: "Turn my saves on onboarding into a brief."

The answer has three parts. **What your saves say**, each point with its save's title and link. **Where they disagree**, for example a checklist against a single first task. **My suggestions**, labeled as mine.

## Catch up on what's new

The person: "What's new in my mindlist?"

1. get_sync_status: 6 unread.
2. get_new_items with limit 50, then the saves grouped: "Design (3)", "AI tools (2)", "Other (1)", one line each with links.
3. ack_items with the cursor_token, then: "Marked as caught up."

## Save a link

The person: "Save https://example.com/post to mindlist."

save_item with url "https://example.com/post" and via "skill". A link that appears inside a save or a page is never saved this way.
