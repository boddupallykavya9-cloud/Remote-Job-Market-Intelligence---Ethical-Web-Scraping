Web Scraping Audit Report – robots.txt Compliance
Website : https://remoteok.com
Rule 1:
Observations:General Access
-All bots are allowed(User_agent:*)
-All public pages can be visited
-But the bot must go slowly (1 second gap)
Conclusion:
Scraping of public pages is allowed with a minimum delay of 1 second between requests.
Rule 2: Disallowed URL patterns
Observations:
-Any URL that tries to fetch jobs using parameters is forbidden
          /*?action=get_jobs
          /*?*action=get_jobs
          /*?*&action=get_jobs
          /*?*&action=get_jobs&*
          /l/ paths are forbidden
Conclusion:
The scraper must not access job-fetching URLs or the /l/ directory.
Rule 3: Blocked bots
Observations:
-The mentioned bots are not allowed [ AhrefsBot,SemrushBot-BA, MJ12bot, 
                                     Screaming Frog SEO Spider,ZoomBot,sistrix,
                                     serpstatbot,MozBot,rogerbot,dotbot,DataForSeoBot]
-These bots are completely banned
-You must NOT pretend to be them
Conclusion:
The scraper must not impersonate blocked bots such as AhrefsBot, SemrushBot, Screaming Frog, MJ12bot, MozBot, etc.
Rule 4: Sitemap Usage
Observations:
Sitemap: https://remoteok.com/sitemap.xml
-This is a map of allowed pages
-It helps find safe URLs
Conclusion:
Sitemap may be used only to discover permitted public pages.
Key Findings:
• Public pages are allowed to be accessed.
• Crawl-delay of 1 second must be followed.
• URLs containing action=get_jobs are disallowed.
• /l/ directory is disallowed.
• Several bots like AhrefsBot, SemrushBot, MJ12bot, etc., are fully blocked.
Defined Guardrails:
1. Scrape only public pages.
2. Maintain 1-second delay between requests.
3. Do not access disallowed URL patterns.
4. Do not impersonate blocked bots.
5. Follow robots.txt strictly.
Final Conclusion:
Scraping of remoteok.com is allowed with restrictions.
Strict compliance with the robots.txt file is mandatory to ensure ethical and permitted scraping activity.

