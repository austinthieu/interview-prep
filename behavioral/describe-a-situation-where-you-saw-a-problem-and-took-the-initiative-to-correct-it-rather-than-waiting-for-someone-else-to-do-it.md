# Describe a situation where you saw a problem and took the initiative to correct it rather then waiting for someone else to do it

**Situation:** While working on a corporate intranet environment at CNRL, a coworker mentioned an ongoing issue where outdated or broken links were appearing across internal pages. These dead links created a poor user experience and made it difficult for teams to find accurate information, especially in documentation hosted on SharePoint and internal portals.

**Task:** Although this wasn’t directly assigned to me, I saw an opportunity to help improve the process. The goal was to create a way to identify broken links efficiently and reduce the manual effort required to notify content owners.

**Action:** I worked with my coworker to understand the scope of the problem and how frequently these issues occurred. I then built a small automation tool in C# that could crawl selected intranet pages, validate URLs, and flag broken or unreachable links. The tool generated a simple report mapping each invalid link to its source page. From there, I added a notification step to help identify the content owner so they could be informed for updates. I tested the tool on a subset of intranet pages first to ensure it didn’t miss valid links or produce false positives, then iterated based on feedback.

**Result:** The automation significantly reduced the manual effort required to identify and report broken links. What previously required manual checking was replaced with a repeatable process that could be run regularly. This helped improve the overall quality of the intranet content and made it easier for teams to keep documentation up to date. It also reinforced the value of automation and proactive problem-solving in improving internal systems.
