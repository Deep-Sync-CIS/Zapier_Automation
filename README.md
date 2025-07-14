# Zapier_Automation

### Overview/Pipeline
Used Zapier to create agents that access and scrape all contents of T-Mobile's Supplier Policy Webpage, and all nested links/PDFs, and copy all contents to a newly created Google Document with today's date. 

Made one agent that tries to copy all text from each PDF, but this has a higher chance of cutting a PDF short. Second agent pulls only the "publish date" or "Updated" date, effectively checking if the policy was recently modified without having to pull all contents from the PDF. If there is no date, the Zap will pull all the text and append to the Google Doc. This agent was far more consistent/accurate. 

Once Google Document has been created with that day's contract information, manual step is required; user must input yesterday's and today's contract document into a custom GPT that parses and compared the documents. A one paragraph summary summarizing the policy changes, or lack thereof, is outputted. 

### Context and Links
T-Mobile initial website to be scraped: https://www.t-mobile.com/our-story/working-together/suppliers/supplier-code-of-conduct

##### Link to Zapier Agents (3 as part of date pulling process)

Document Creator: https://agents.zapier.com/copy/8c7128fe-a032-4cc4-a1ab-89329ed7ee13
Text Appender: https://agents.zapier.com/copy/c934cc58-f57f-450f-aeb6-bb2c1110d090
Text Appender: https://agents.zapier.com/copy/da74ac90-6595-49d3-b3b1-6002d80e9ff7

###### Link to solo agent (pulls all text)
https://agents.zapier.com/copy/5613a2a2-14e3-41da-a060-074ad66e5af4

##### Link to Custom GPT
[REPLACE WITH NEW LINK]

### Problems and Next Steps
As this was just to show the potential of agents, as these services undoubtedly improve, we can iterate on prompting to eliminate inconsistencies with scraping. Also, soon we should be able to have the Zap compare yesterday's and today's document internally, fully consolidating the process to one, autonomous platform. 

Once custom GPT step is eliminated, the pipeline becomes fully agentic. Can likely even email result summary to you every morning.
