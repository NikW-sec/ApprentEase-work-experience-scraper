#Data Branch

The data branch stores three text files:

EventLinks.txt — Uptree links collected during the most recent run.

EventLinks2.txt — Futures For All links collected during the most recent run.

failedEvents.txt — Details of Discord messages that failed to send.

The application in the main branch reads the two event-history files and compares their links against newly scraped opportunities to identify new events.

After each run, GitHub Actions updates the files and automatically commits and pushes the changes back to this branch.

failedEvents.txt stores messages that still require delivery. If the file is empty, there are currently no recorded failed messages awaiting recovery.
