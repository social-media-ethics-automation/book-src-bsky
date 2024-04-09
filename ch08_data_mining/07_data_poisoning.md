# Data Poisoning
People working with data sets always have to deal with problems in their data, stemming from things like mistyped data entries, missing data, and the general problem of all data being a simplification of reality.

Sometimes a dataset has so many problems that it is effectively __poisoned__ or not feasible to work with.

## Unintentional Data Poisoning
Datasets can be poisoned unintentionally. For example, many scientists posted online surveys that people can get paid to take. Getting useful results depended on a wide range of people taking them. But when one TikToker's video about taking them went viral, the surveys got filled out with mostly one narrow demographic, preventing many of the datasets from being used as intended.

See more in
- [A teenager on TikTok disrupted thousands of scientific studies with a single video -- The Verge](https://www.theverge.com/2021/9/24/22688278/tiktok-science-study-survey-prolific) {cite:p}`letzterTeenagerTikTokDisrupted2021`

Additionally, spam and output from Large Language Models like ChatGPT can flood information spaces (e.g., email, Wikipedia) with nonsense, useless, or false content, making them hard to use or useless.

See more in
- [CNET Is Reviewing the Accuracy of All Its AI-Written Articles After Multiple Major Corrections](https://gizmodo.com/cnet-ai-chatgpt-news-robot-1849996151) {cite:p}`CNETReviewingAccuracy2023`
- [Why posting GPT and ChatGPT generated answers is not currently acceptable - StackOverflow](https://stackoverflow.com/help/gpt-policy) {cite:p}`WhyCanUse`


## Intentional Data Poisoning

Data can be poisoned intentionally as well. For example, in 2021, workers at Kellogg's were upset at their working conditions, so they agreed to go on strike, and not work until Kellogg's agreed to improve their work conditions. Kellogg's announced that they would hire new workers to replace the striking workers:

> Kellogg's proposed pay and benefits cuts while forcing workers to work severe overtime as long as 16-hour-days for seven days a week. Some workers stayed on the job for months without a single day off. The company refuses to meet the union’s proposals for better pay, hours, and benefits, so they went on strike. 
> 
> Earlier this week, the company announced it would permanently replace 1,400 striking workers.  
>
> - [People Are Spamming Kellogg’s Job Applications in Solidarity with Striking Workers -- Vice MotherBoard](https://www.vice.com/en/article/v7dvy9/spamming-kelloggs-job-applications-strike) {cite:p}`colePeopleAreSpamming2021`


People in the [antiwork subreddit](https://www.reddit.com/r/antiwork/) {cite:p}`AntiworkUnemploymentAll` found the website where Kellogg's posted their job listing to replace the workers. So those Redditors suggested they spam the site with fake applications, poisoning the job application data, so Kellogg's wouldn't be able to figure out which applications were legitimate or not (we could consider this a form of trolling). Then Kellogg's wouldn't be able to replace the striking workers, and they would have to agree to better working conditions.

Then Sean Black, a programmer on TikTok saw this and decided to contribute by creating a bot that would automatically log in and fill out applications with random user info, increasing the rate at which he (and others who used his code) could spam the Kellogg's job applications:

<blockquote class="tiktok-embed" cite="https://www.tiktok.com/@seandablack/video/7039823665294232878" data-video-id="7039823665294232878" style="max-width: 605px;min-width: 325px;" > <section> <a target="_blank" title="@seandablack" href="https://www.tiktok.com/@seandablack?refer=embed">@seandablack</a> Shortucut soon perhaps <a title="antiwork" target="_blank" href="https://www.tiktok.com/tag/antiwork?refer=embed">#antiwork</a> <a title="workersrights" target="_blank" href="https://www.tiktok.com/tag/workersrights?refer=embed">#workersrights</a> <a title="kelloggs" target="_blank" href="https://www.tiktok.com/tag/kelloggs?refer=embed">#kelloggs</a> <a title="strike" target="_blank" href="https://www.tiktok.com/tag/strike?refer=embed">#strike</a> <a title="unions" target="_blank" href="https://www.tiktok.com/tag/unions?refer=embed">#unions</a> <a title="leftist" target="_blank" href="https://www.tiktok.com/tag/leftist?refer=embed">#leftist</a> <a target="_blank" title="♬ original sound - Sean Black" href="https://www.tiktok.com/music/original-sound-7039823643236567854?refer=embed">♬ original sound - Sean Black</a> </section> </blockquote> <script async src="https://www.tiktok.com/embed.js"></script>


See also:
- [How to poison the data that Big Tech uses to surveil you -- MIT Technology Review](https://www.technologyreview.com/2021/03/05/1020376/resist-big-tech-surveillance-data/) {cite:p}`HowPoisonData`
