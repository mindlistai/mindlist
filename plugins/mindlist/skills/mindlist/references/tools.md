# The mindlist connector's commands

Every call made while following the skill also takes via: "skill". It changes nothing in the answer.

## Reading

| Command | Arguments | Gives |
| --- | --- | --- |
| search_items | query (1 to 200 characters), limit (1 to 100, default 20) | Saves that match the words, notes and meaning, best first |
| list_items | search (words, matched as words), tag (a tag's name), space_id, mindlist_id, content_type (for example article, video, image, note), since (ISO 8601 with its offset), include_archived, limit (1 to 100, default 50), next (the previous page's next) | A page of saves and a next for the page after it |
| get_item | id, include (any of transcription, metadata, media) | One save in full: its text, its linked_url, and what include asked for |
| get_organization | none | The person's spaces, mindlists and tags, with names, IDs and counts |

## Catching up

Each connection keeps a position. "New" means saved after it.

| Command | Arguments | Gives |
| --- | --- | --- |
| get_sync_status | none | How many saves are unread, the newest one, and the totals |
| get_new_items | limit (1 to 100, default 50) | The saves after the position, oldest first, with cursor_token and has_more. It does not move the position |
| ack_items | cursor_token (from get_new_items) | Moves the position past that page |
| set_cursor | to: "beginning", "now", or an ISO 8601 time with its offset | Moves the position there |

## Saving

| Command | Arguments | Gives |
| --- | --- | --- |
| save_item | url (the link), note (optional) | The new save. Only on connections with save access; on a read-only connection it is missing |

## The fields of a save

id, title, content_type, source, url (the link as shared; null for a note or an upload), source_domain, author, summary (by AI), highlights, notes (the person's own), tags (chosen by the person), ai_tags (chosen by AI), mindlists (id and name), space (id, name, emoji), status (active or archived), pinned, finished, created_at, updated_at.

has tells what get_item can add: text_chars (the captured text's length), transcript_chars (a video's transcript length), images, file.
