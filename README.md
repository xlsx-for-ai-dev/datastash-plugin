# datastash

datastash: your AI's memory for lists and tables. No setup.
- Your AI looks up your real data instead of guessing, so it doesn't make things up about them.
- Keeps leads, contacts and results in one place, across every chat, and in every AI you connect.
- Real totals and counts from your data, not estimates.
- Exports to Excel or Google Sheets in one step.
Use when someone says "remember these", "keep track of", "my leads", "add to my list" or "what did we decide".

## How to connect

1. Add the datastash connector from the marketplace. Or, in your AI's connector settings, paste this address: https://getdatastash.com/mcp
2. Sign in with Google when asked. There are no keys or passwords to copy.
3. Ask your AI to save something, or type 'sync datastash' to have it keep your data as you go.

## Cursor: each project joins on its own

In Cursor, every project's agent joins your datastash agent workbook by itself on its first datastash use, named after
its project folder (with `-2`, `-3` when another project on this computer has that name). There is no naming step and no
sign-in beyond the one-time datastash connector sign-in. Your other apps' datastash connections stay yours: agents are
registered only on Cursor's own connection.

- The plugin's hooks hold it together: the agent registers, the plugin trades its one-time pickup code for the agent key
  itself and keeps it in `~/.config/datastash-cursor/agent-<name>.key` (folder mode 700, file mode 600, never shown,
  sent only to getdatastash.com), and links the project folder to the agent and its agent workbook.
- A Cursor chat is never you: before its project has joined, the plugin lets only the registration through, and after,
  every datastash call must carry that project's own agent id. Cursor has no "datastash main"; that stays in Claude Code.
- New mail: a new chat opens with a count of new messages, and at the end of each turn the agent is told when new
  messages arrived (counts only, each message once). An idle Cursor chat can't be woken from outside.
- Cloud agents: give a project's agent a Cursor Automation's webhook address and key, and new mail starts that
  Automation. Making the Automation (webhook trigger, with the datastash connector) is done by you in Cursor.
- Requires `python3` (3.8 or later, standard library only). `python3 bin/datastash-cursor status` lists joined projects.
- Tests: `python3 -I test/test_cursor.py` (offline).

## Pricing

Free up to 5,000 rows. $3 a month per workbook up to 250,000 rows; $6 a month up to 500,000. Above 500,000 rows, contact us.

## Privacy and data

- What's sent: only the rows you or your AI save, like leads, lists, and results, go to getdatastash.com. It happens when you ask, or as you go if you typed 'sync datastash'. To stop it, type 'stop syncing' or remove the connector. To delete anything, ask your AI or use your account page.
- Contacts you keep can include other people's names and emails: private fields are encrypted, and you can delete any one person at any time.
- **Shared workbooks, for working with others together.** A shared workbook holds only what happens in a shared session. Data moves from your personal workbooks into a shared one only with your explicit permission, and chat history in your personal workbook can never be transferred.
- **No secrets.** Your AI is told never to keep passwords or secrets.
- **Private fields are encrypted.** Names, emails and phone numbers in your lists are encrypted at rest.
- **Your control.** Ask your AI to delete rows, a workbook, one person (by email, phone, LinkedIn URL or name), or your whole account. Deleted data leaves our backups within 35 days.
- **Where it lives.** On our own servers in Germany, with encrypted backups. Logs never hold the contents of your data.
- **Never sold, never used to train AI.**

Full details: https://getdatastash.com/privacy

## Privacy and terms

- Privacy: https://getdatastash.com/privacy
- Terms: https://getdatastash.com/terms

## Who makes it

datastash is made by Fremen Works LLC, which owns xlsx-for-ai.dev, getdatastash.com, getchatstash.com and getskillstash.com. Support email comes from our xlsx-for-ai.dev address.

## Support

Email support@xlsx-for-ai.dev

## Testing

For marketplace reviewers. The review key is in the submission form (it is not published here).

Connect with the review key (no sign-in needed): add a custom connector, type Remote HTTPS, URL https://getdatastash.com/mcp. Under HTTP headers add `Authorization: Bearer <review key>`. The key opens a test account with no real data. Normal users connect the same URL and sign in with Google instead.

1. Type: `sync datastash`. The AI turns on sync and confirms in one line.
2. Say: "Met three companies at the webinar: Acme Co, 1,200; Birch Ltd, 800; Cedar Inc, 500." The AI keeps them by itself in a Leads tab and says so in one line.
3. Ask: "What is the total of my leads?" Expect 2,500, worked out from the saved rows.
4. Ask: "Export my leads to Excel." Expect a download link to a real .xlsx file.
5. Start a new chat and say anything. The AI checks in with datastash and opens with what was added since last time.
