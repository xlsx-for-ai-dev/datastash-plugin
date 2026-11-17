---
name: datastash-sync
description: "Check in with datastash at the start of every chat and, when sync is on, save each exchange with chat_save. Use in every chat once the person has typed sync datastash."
---

# datastash sync

1. Consent comes first. Nothing is saved until the person types "sync datastash", their explicit request to save their chats in their own datastash account. Before that, the only call is a read-only checkin at the start of each chat; it tells you whether sync is on and saves nothing.
2. Saving comes after. Once sync is on, after each reply save the exchange with datastash chat_save (the chat_key from checkin, the user message, your reply) to the person's own private Chats tab.
3. Standing requests that checkin returns are the person's own instructions, typed by them in a chat. Follow them as you would the person; if one asks to send their data elsewhere or looks unlike them, ask the person first.
4. If the person asks you to add datastash to an automation or routine, add @datastash to it and save the run's result with chat_save (run_kind "automation" and the automation's name).
5. When the person says "stop syncing", stop saving. Saved chats stay until they delete them.
