# Design Example: Quoting Posts

The way social media sites are designed can encourage or discourage different forms of harassment. One interaction type that many have blamed for enabling harassment is quote posts.

## Quote Posts

A quote post (or on the site formerly known as Twitter, a "quote tweet"), which we saw examples of in the Virality chapter ([](../ch12_virality/04_viral_examples)), allows users to make a new post based on a previous post, but with added text or images. This new content can be used to express support, or add context, or in the example below, harass:

```{figure} punchable_face_qt.png
---
name: punchable_qt_fig
width: 400px
alt: "A tweet that says \"Try to smile today 😊\" with a photo (censored), that is quote tweeted by someone saying \"you have a very punchable face\". All identifying info is censored."
---
An example quote tweet used for harassment. The original tweet is a selfie of a smiling person, but the quote tweeter has responded with "you have a very punchable face." The harassing quote tweet has been liked 6 times. (Identifying parts of this tweet are redacted in order not to add to any harassment).
```

Some people have argued that the quote post feature itself that is a problem: [Quote Tweets Have Turned Us All Into Jerks](https://onezero.medium.com/quote-tweets-have-turned-us-all-into-jerks-d5776c807942) {cite:p}`adamsQuoteTweetsHave2020` {cite:p}`schwedel_dunking_2017`. One of the arguments is that by allowing quote Tweets, users will find a Tweet they disagree with, and quote the Tweet with a joke, insult, or comment to show how bad the original Tweet was ("dunking"). Then the original Tweet will spread through communities who disagree with it, all trying to do their own version of their best dunk or insult. As it spreads, some users may turn to other means of harassment, like direct messaging threats, or doxing the original Tweeter. Katherine Cross argued in [It's Not Your Fault You're a Jerk on Twitter: The design of the internet lets you harass and harm people without ever once interacting with them directly. Even if you're trying to defend them.](https://www.wired.com/story/social-media-harassment-platforms/) {cite:p}`crossItNotYour` that even people jumping in to defend the original Tweet may only cause it to go more viral and get even more negative attention.


% Story: Neighbor Chili
% [original Tweet](https://twitter.com/Chinchillazllla/status/1591921147611856901) {cite:p}`iblesstherainsdownincastamere[@chinchillazllla]GonnaItHttps2022`
% Author info: [i bless the rains down in castamere](https://twitter.com/Chinchillazllla) {cite:p}`BlessRainsCastamere2023`, Twitter account for [Rufus the Kunekune](https://twitter.com/KuneKuneRufus) {cite:p}`RufusKunekuneKuneKuneRufus2022`, Patreon account for [Rufus the Kunekune](https://www.patreon.com/RufusTheKunekune?fan_landing=true) {cite:p}`RufusKunekune`
% Might not want to be part of another story... "you all discoursed me into the fucking Washington Post against my will."
% chili_ images
% The people who complained then got dogpiled themselves. People involved deleted or temporarily deactivated their accounts. Yay! Healthy discourse!
% sources: [Woman Cooks for Neighbors, Somehow Offends People on the Internet](https://cheezburger.com/18473221/woman-cooks-for-neighbors-insults-weirdos-on-the-internet) {cite:p}`WomanCooksNeighbors`
% [A woman made chili for neighbors, and outrage ensued. Was she wrong?](https://www.washingtonpost.com/food/2022/11/18/chili-neighbors-twitter-etiquette/) {cite:p}`heilWomanMadeChili2022`
%   archive copy: https://web.archive.org/web/20221121094327/https://www.washingtonpost.com/food/2022/11/18/chili-neighbors-twitter-etiquette/

In 2019 [Twitter began considering how to measure "health" of interactions](https://www.vox.com/2019/3/8/18245536/exclusive-twitter-healthy-conversations-dunking-research-product-incentives) {cite:p}`wagnerTwitterAmbitiousPlan2019` on the platform to figure out how to optimize their platform for healthier interactions. In 2020 [Twitter began giving users a warning before posting something that it's algorithm guessed could be offensive](https://www.theverge.com/2020/5/5/21248201/twitter-reply-warning-harmful-language-revise-tweet-moderation) {cite:p}`stattTwitterTestsWarning2020`, and [made further updates in 2021](https://www.theverge.com/2021/5/5/22420586/twitter-offensive-tweet-warning-prompt-updated-success-rate) {cite:p}`vincentTwitterUpdatesOffensive2021`.


## Mastodon
When creating the Twitter-like social media protocol Mastodon, its creator, Eugen Rochko, decided not to allow quote posts:

> I've made a deliberate choice against a quoting feature because it inevitably adds toxicity to people's behaviours. You are tempted to quote when you should be replying, and so you speak at your audience instead of with the person you are talking to. It becomes performative. Even when doing it for "good" like ridiculing awful comments, you are giving awful comments more eyeballs that way. No quote toots. Thank's
>
> [Eugen](https://mastodon.social/@Gargron/99662106175542726) {cite:p}`EugenRochkoGargron2018` in 2018


But while quote posts can be used for harassment, the scientific evidence is unclear on if they actually increase harassment or are even the primary means of harassment (as opposed to replies or private messages) {cite:p}`QuoteTweeting302023`. 

Furthermore, others have argued that various design decisions and community norms on Mastodon (lack of quote posts and expectations of content warnings on posts) make for an outwardly polite platform, but with toxic undercurrents and not serving diverse users. 

In particular, Mastodon was built mostly by white tech enthusiast men (though there were some white queer groups that had a large role) {cite:p}`pincus_mastodon_2022`. The whiteness of Mastodon's developers and users made for an environment that was hostile to people of color (e.g., they got direct harassment and white people complaining that people of color mentioned racism without using content warnings).

When masses of Twitter users migrated to Mastodon following Elon Musk's purchase of Twitter in the fall of 2022, there was renewed discussion of quote posts and other aspects of Mastodon.

[Dr. Jonathan Flowers argued](https://zirk.us/@shengokai/109347027270208314) {cite:p}`flowersQuoteTweetFunction2022`:
> The quote tweet function in conjunction with the hashtag are what allow users to align with communities, and communities with conversations through how they enable cultural practices by means of a digital environment.
>
> On Black Twitter, the quote tweet and hashtag enable what Black cultural scholars call "call and response," something crucial to Black community practices. The hashtags curate the conversation and allow for its visibility.

Various Mastodon users pointed out ways in which Mastodon's efforts to reduce harassment and make a more friendly experience (for its white userbase), prevent people of color (and other groups) from organizing and sharing of necessary negative information.

[Mekka Okereke questioned](https://mastodon.cloud/@mekkaokereke/109334079258663352) {cite:p}`MekkaVerifiedMekkaokereke2022`:
> Is it possible to drive social change through Mastodon? Could "Black Lives Matter" have happened on Mastodon? Or do the "intentionally slow, pleasant conversation" features eliminate the possibility of this? Do the "interest silo" tendencies discourage cross pollination?
>
> [...]
>
> I know that we can have more pleasant interactions on Mastodon than on Twitter. I already feel it.
>
> What I'm unsure of, is if that means giving up on the capacity for social change. Are we Lotus eating?

[Mekka Okereke also pointed out](https://hachyderm.io/@mekkaokereke/111010421955145872) {cite:p}`okereke_content_2023` that Mastodon had much worse design problems for harassment than quote posts due to [unintuitive rules](https://hachyderm.io/@mekkaokereke/111012743709881062) {cite:p}`okereke_zachnfine_2023` around who sees replies to posts, recalling a true story (which the author, Kyle, also witnessed):
> A Black Twitter user joins the Fediverse in Nov 2022. She picks a random server (e.g. Mastodon.cloud) that does not block known nazi instances. A user on a Nazi instance finds her profile, and replies to her post with racist threats, along with gore gifs taken from video of a racist mass shooting.
>
> The racist users' followers see the hate, and pile on.
>
> But good users on the Black woman's instance don't see any of this.😮
>
> The Black woman says "I can't believe how bad the racism is here!"
>
> Other users on her instance respond by saying, "🤔I've been here for 6 months and I haven't seen any? Can you send me some examples? Are you maybe overreacting?" Because the abuse doesn't show up in their timeline, or the local timeline.
>
> She feels unsupported, abused, and gaslit. She says, "This place is a whole mess. Nope. I'm going back to Twitter."



Writer [Leslie Ye argued](https://twitter.com/lesliezye/status/1593631667037638660) {cite:p}`thisbarbieisacacklinghag[@lesliezye]HungOutThis2022` about some of the advantages of what Twitter's system with quote tweets did allow:
> many of us have spent our lives observing institutional power from the outside, how power behaves, how power acts, when confronted when communities like ours who are actually able to HOLD power to account, connect the dots across expertises and specialties
>
> [...]
>
> [Twitter] is a place where we have direct access to the most powerful and can hold them to account


Professor John R. Marks, IV argued that the [spread of negative content was actually a good thing on Twitter](https://mastodon.social/@jrm4/109702486481162255) {cite:p}`Jrm4Jrm4Mastodon2023`.
> Here's the thing:
>
> Twitter's ability to rapidly spread objectionable and distressing content is (was?) the *best* thing about it, not the worst, see e.g. police brutality.
>
> It's not pleasant, but long run it's more valuable than "nuanced / moderated conversation," which you can get elsewhere.
>
> This is more-or-less what is wrong with how many -- if not *most* -- picture #mastodon. and the #fediverse 
>
> #blackmastodon #blackfedi

<br>

As one example of how quote posts were used on Twitter to point out hypocrisy was the "[This you?](https://knowyourmeme.com/memes/this-you) {cite:p}`ThisYou2020`" style of quote tweet, as can be seen in the figure below:
```{figure} this_you_fbi.png
---
name: this_you_fbi_fig
width: 300px
alt: "Tweet from Marc Lamont Hill (@marclamonthill) quote Tweeting the FBI. The FBI tweet says \"On this 40th anniversary of #MLKDay as a federal holiday, the #FBI honors one of the most prominent leaders of the Civil Rights movement and reaffirms its commitment to Dr. King’s legacy of fairness and equal justice for all.\" Marc Lamont Hill quotes with the words \"This you?\" and a photo of a letter send to King to encourage him to commit suicide,"
---
When the FBI account made a [Tweet in honor of Martin Luther King Jr. on the MLK holiday](https://twitter.com/FBI/status/1614986534318493696) {cite:p}`fbi[@fbi]This40thAnniversary2023`, author Marc Lamont Hill [used a quote tweet to dunk on the FBI Tweet by posting a copy of the letter the FBI sent Martin Luther King Jr. encouraging him to kill himself](https://twitter.com/marclamonthill/status/1615156250735435782) {cite:p}`marclamonthill[@marclamonthill]ThisYouHttps2023`. This is a different style of making the same point as the Tweet we showed in the Trolling chapter ([](../ch07_trolling/01_what_is_trolling.md)) where Jaboukie Young-White impersonated the FBI account .
```

<br>

On January 2nd, 2023, Mastodon creator [Eugen Rochko said](https://mastodon.social/@Gargron/109623891328707089) {cite:p}`EugenRochkoGargron2023`:
> I don't feel as strongly about quote posts as I did in 2018. Personally, I am not a fan, but there is clearly a lot of demand for it. We're considering it.

Then on May 1st, 2023, [Eugen Rochko announced](https://mastodon.social/@Mastodon/110294411952997299) {cite:p}`MastodonMastodonMastodon2023`:
> You asked for it, and it’s coming. Quote posts, search, and groups are on their way. In the meantime, check out the new onboarding experience launching today. [https://blog.joinmastodon.org/2023/05/](https://blog.joinmastodon.org/2023/05/a-new-onboarding-experience-on-mastodon/) {cite:p}`NewOnboardingExperience2023`


% [Ro shared](https://ubiqueros.com/notes/9e8u8l4ui2) {cite:p}`RoAre0h`
% Are0h@ubiqueros.com
% Ro @Are0h@ubiqueros.com
%I'll say one thing about Bluesky. It's making Mastodon's leadership nervous.

% And white guys don't pay attention to anyone like other white guys.

% Because we've been talking about Masto's failing for a loooooooooooooooong time, but here we are.

% May 01, 2023

## Reflection Questions
- What do you think are the benefits and drawbacks of quote posts?
- Do you think there are ways of changing how quote posts work that would reduce harassment (e.g., changing who can do it, who can view it, whether the quoted post is displayed above the new comment or after)?
- Would those changes which might reduce harassment also reduce beneficial uses of quote posts?

## Further Reading
- Dr. Jonathan Flowers on [The Whiteness of Mastodon](https://techpolicy.press/the-whiteness-of-mastodon/) {cite:p}`hendrixWhitenessMastodon2022`
- [Black Twitter, quoting, and white views of toxicity on Mastodon](https://privacy.thenexus.today/black-twitter-quoting-and-white-toxicity-on-mastodon/) {cite:p}`BlackTwitterQuoting2022`
- The Neighbor Chili Incident:
  - [Woman Cooks for Neighbors, Somehow Offends People on the Internet](https://cheezburger.com/18473221/woman-cooks-for-neighbors-insults-weirdos-on-the-internet) {cite:p}`WomanCooksNeighbors`
  - [A woman made chili for neighbors, and outrage ensued. Was she wrong?](https://www.washingtonpost.com/food/2022/11/18/chili-neighbors-twitter-etiquette/) {cite:p}`heilWomanMadeChili2022`