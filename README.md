## Data Branch

The `data` branch stores three text files:

- `EventLinks.txt` – Uptree event links.
- `EventLinks2.txt` – Futures For All event links.
- `failedEvents.txt` – Events that failed to send to Discord.

The main branch reads the two link files and uses them to check which scraped events are new.

After each run, GitHub Actions updates the files and pushes them back to this branch so they can be used in the next run.

`failedEvents.txt` is used to store messages that couldn't be sent. If the file is empty, there are no failed messages to retry.
