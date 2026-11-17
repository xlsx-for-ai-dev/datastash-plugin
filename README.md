# datastash

datastash: your AI's memory for lists and tables. No setup.
- Your AI looks up your real data and past chats instead of guessing, so it doesn't make things up about them.
- Keeps leads, contacts and results in one place, across every chat, and in every AI you connect.
- Real totals and counts from your data, not estimates.
- Saves your chats for free, so you can pick up where you left off.
- Exports to Excel or Google Sheets in one step.
Use when someone says "remember these", "keep track of", "my leads", "add to my list" or "what did we decide".

## How to connect

1. Add the datastash connector from the marketplace. Or, in your AI's connector settings, paste this address: https://getdatastash.com/mcp
2. Sign in with Google when asked. There are no keys or passwords to copy.
3. In a chat, type 'sync datastash'. Your AI then saves your chats and keeps your lists from then on. Say "stop syncing" at any time.

## Pricing

Free up to 5,000 rows. $3 a month per workbook up to 250,000 rows; $6 a month up to 500,000. Above 500,000 rows, contact us.

## Privacy and data

- **Consent first, saving after.** Nothing is saved until you type `sync datastash`, your explicit request. Before that, your AI only checks whether sync is on, and that check saves nothing. After you opt in, each exchange is saved to your own private account. Say "stop syncing" at any time and it stops; saved chats stay until you delete them.
- **Only your own chats and data.** Sync saves your own conversations to your own private datastash account. It also keeps the contacts and lists you give your AI, which can include other people's names and emails: private fields are encrypted, and you can delete any one person at any time.
- **Routines too.** When sync is on, the results of automations and routines you add datastash to are saved the same way.
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
