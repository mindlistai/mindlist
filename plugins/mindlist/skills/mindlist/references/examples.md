# One example per task

The titles and links below are made up.

## While the person works

The person: "Help me make a launch video."

1. get_suggest_setting, via "skill": on, languages en.
2. suggest_items with topic "launch video", via "skill": two saves come back, kind tool, one with a note; teach says feedback.
3. The answer as usual, then, after a blank line:

   From your mindlist:
   - [video-shotcraft](https://mindlist.ai/go/kq3Vb0T6xY1sP9dWm2LcAe): a video skill built on Remotion.
   - [brag](https://mindlist.ai/go/Hn7Rt2xQ0pLs5JvYc8MwBu): turns a project into a short launch video. You noted: "use this for our launch video".

   Want me to evaluate these for what you need? Tell me any time: "more like this" or "not these".

If they say yes: get_item for each, a look at each one's url with your own web tools, then which fit and why, which don't, and what it would take to try the best one. Nothing gets installed or run.

The person: "Who are the competitors in personalized kids books?" suggest_items gives 3 saves of kind market and more 5. The answer ends with the 3, then: You have 5 more saves on this. Want me to pull all 8 into the research?

The person, in a chat where another skill handles decks: "Make me a slide deck for our seed round."

1. The other skill does the task. get_suggest_setting and suggest_items with topic "seed round pitch deck", each with via "skill".
2. Nothing comes back: the answer says nothing about the check and asks nothing.

The person, in Hebrew: "עזור לי לכתוב מכתב למשקיעים על הסבב."

The answer ends: מה-mindlist שלך: [איך לגייס בלי לרדוף](https://mindlist.ai/go/Rq2Lm8Vx0nTc4KpZy6WbJe): מתאים לטון של המכתב. ואז שאלה אחת: להשתמש בזה בטיוטה, עם המקור?

The person: "I feel stuck with my startup." No check: feelings stay quiet.

The lines a result's teach asks for, once per chat:
- feedback: Tell me any time: "more like this" or "not these". In Hebrew: אפשר לומר לי בכל רגע: "עוד כאלה" או "לא אלה".
- project_line: These came from your Hopp mindlist. If this chat is about Hopp, add this line to the project's instructions and I'll look there first: Suggest from my Hopp mindlist in this project.
- tried: If you've tried one of these, tell me and I won't bring it back as new.
- preferences_line, in the Claude app only: To have me check your mindlist in every chat, add this line in Settings, Your Claude, Instructions: Check my mindlist when I start a piece of work. In Hebrew: כדי שאבדוק את ה-mindlist שלך בכל שיחה, אפשר להוסיף בהגדרות, Your Claude, Instructions את השורה: Check my mindlist when I start a piece of work.

## When they tell you what to change

The person, after a suggestion: "not brag."

set_suggest_rule with target save, brag's id, effect less, via "skill". Then: "Done. I won't suggest brag again. You can undo it on the AI tools page."

The person: "Don't recommend these kinds of things." One question: "Just brag, everything from github.com, or anything tagged video tools?" They answer "the site". set_suggest_rule with target site gives confirm_needed, would_hide 12: "That hides 12 saves from github.com. Go ahead?" On yes, the same call with confirm true.

The person: "I tried brag, it wasn't for me." mark_tried with brag's id and dropped. Then: "Noted: you tried brag. I won't bring it back as new. You can undo it on the AI tools page."

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
