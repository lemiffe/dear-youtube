Dear YouTube,

You have done so much to enable creators to make and share exciting videos, whether that be mini series, cooking shows, films, music videos, news, podcasts, top 10s, documentaries, you name it.

Many communities have spawned around channels and topics, with comment sections ranging from support, to fully-blown drama. And whilst there is quite a lot of trolling, the positive and supportive comments far outweigh the negativity.

However, many of us viewers are frustrated. Those of us who spend hours watching content (and ads) have been receiving videos with worse content during the past year, more clickbait, less meat, more in-video ads, and fillers due to the 10 minute mark for mid-roll ads.

Additionally, too many creators are making videos complaining about YouTube's policies and demonetisation, even on channels that didn't use to post regularly about that (e.g. PewDiePie, h3h3, Casey Neistat, Philip DeFranco, MrBeast, Jörg Sprave, and a myriad of other creators). A quick search for "demonetized" on YouTube returns around 369,000 videos. That's a lot of angry creators.

This means that these YouTubers are derailing from creating the content they are known and loved for, and instead they resort to making videos talking about the platform's problems that are directly affecting them, and in turn this means we, as viewers, receive less of the content we actually want to watch.

The way we see it is that there are three groups of problems currently plaguing the platform: monetisation, content rules/flagging, and UX issues.

### 1. Problems regarding monetisation:

After demonetisation was introduced over a year ago, a lot of creators were concerned, and after the first few high-profile cases started coming in, users and news outlets started calling it the "Adpocalypse".

One solution that is increasingly being used by creators is to use Patreon, and in some cases that works really well, for example: musicians, artists, writers, cartoonists, animators, etc. But it is still an extra action (and account) a viewer has to make on a 3rd party website, which means a lot of potential contributors will be alienated. This would be solved with channel-based subscriptions similar to Twitch. We know you are experimenting with (and currently rolling out) a paid subscription system for channels, which is a good solution on paper, but in our opinion this is not the best solution.

An option to consider instead might be to establish a pot for monthly payouts. For example, a user might decide to contribute $5, $10, or $20 per month, with a similar model to Spotify or Netflix. The amount then gets divided at the end of the month between YouTubers with a percentage-per-creator calculated by an algorithm based on subscriptions, likes/dislikes, time viewed per channel, amongst other parameters.

In return, viewers are rewarded with fewer ads depending on how much they contribute per month. Google naturally takes a cut from these proceeds.

Furthermore, this can work without disrupting the business model of YouTube Red. If we contribute $25 or more per month, why not offer the option to subscribe to YouTube Red, but instead of keeping the $10, your revenue would depend on viewing habits, keeping $5-10 a month depending on the amount of time viewing regular YouTube, versus YouTube Red series.

### 2. Problems regarding content rules and bots:

One of the issues here has been communication in the past regarding changes. Recently Susan Wojcicki has stated you will be making changes in 2018 regarding how you communicate with creators. However, the wording seems to favour giving a "heads up" instead of proactively holding discussion of changes that will create major repercussions for creators.

However, that is only one part of the problem. One common complaint is that content decisions regarding monetisation, and the automatic "category / subcategory" the video falls under is not transparent enough. Some people even figured out how to enumerate the category IDs for sensitive content. Interestingly enough, that document also dives into the case of systematically suppressing demonetised videos from "suggested videos". By making this information visible to creators, they will be able to make decisions that will influence the direction in which they wish to take their channel.

Rules also have to be made explicit, and reasons for flagging, or why videos were categorised in a certain way should be easily viewable in the Creator Studio, along with any additional information that could help the creator understand where he went wrong and how to improve / fix it. Timestamps of infringing content (the same as those applied to copyrighted content) are also a big plus.

Dude Perfect and PewDiePie's subscribers have also mentioned a couple of instances where X-rated ads were shown on some of his videos, as their videos were placed in categories meant for mature audiences, whereas clearly their viewers have a wide age range.

### 3. UX and notification issues:

Videos we have viewed before (or almost finished watching and then switched to another video) constantly reappear in the suggestions. These should be excluded by the suggestions filter as few people would want to watch the same video twice (music videos being an exception).

The bell / subscribe system is broken and has been mentioned by both viewers and creators. You have denied this vehemently in the past. However, recently a video on one of your own channels you mentioned the issue happened to you and mentioned this would be escalated. In this specific issue it might just have been an MQ (message queue) issue with sending out announcements (or your email service provider experienced downtime).

A mitigation strategy here would be to implement better monitoring of users that requested notifications VS users that received notifications and emails. Most push notification services, as well as email services provide receipts of reception, and also give statistics on the percentage of emails marked as spam. You should graph this (using DataDog for example) and make it visible on a monitor at all times in the HQ; this will allow you to see the actual problem, and formulate strategies to improve notifications.

As a UX bonus, if a creator uploads something new and a user is currently on YouTube, display a toast message mentioning "{CREATOR} just uploaded a new video titled {TITLE}", you can do this easily with WebSockets or a service such as Pubnub or Pusher. The whole feature would probably only be 20-30 story points (excluding mobile).

### What have been the consequences on the current policies and problems?

Jörg Sprave started The YouTubers Union movement recently, where he has 15K+ followers on his Facebook Group. He plans to take direct action such as strikes, and communicate constantly with you to try to convince you to make changes that will improve the lives of content creators.

PewDiePie has been talking about the issues for more than a year, to the point he changed his entire delivery style accordingly. Casey Neistat interviewed YouTube's head of business (which was a great start, as mentioned in the comments of the video), however, much is left to be done.

As viewers, we don't really want to meddle with the politics of what is happening at YouTube, nor with the frustrations of the creators. Instead, we want quality content. Many of us don't watch Netflix, Hulu, Amazon Prime; instead, we rely on Youtube for our daily dose of entertainment. But something is really wrong when a lot of the content we watch includes long segments with complaints or rants about demonetisation, and the other issues mentioned in this article.

### Our proposal:

We know the issue of figuring out a compromise between ads, paid subscriptions, and YouTube Red is a complicated one, potentially involving everyone from your legal team, accounting, engineering, product, designers, and project manager.

An intermediary step may be: While you figure out subscriptions (and please make it easy to pay), then you should at least cover part of the salary of the creators that get millions of views, but are heavily demonetised, maybe based on the amount of views and likes per video.

Afterwards, we would like to offer a few strategies on how to develop and implement the changes. We've written these down in the following section.

We would also like to re-iterate the demands posted on Jörg Sprave's union website, which we have split per section. These give a good idea on some of the major complaints the community of creators has:

- Monetisation:
  - Monetise everyone: Bring back monetisation for smaller channels
  - Disable the (auto-flagging/demonetising) bots. Add a voting system aided by AI (see Valve's VACnet)
  - Pay for the views
  - Stop demonetisation as a whole
  - Pay according to delivered value
- Content / Rules:
  - Transparent content decisions
  - Equal treatment for all partners
  - Clarify the rules

You can read the extended version of the union's demands on their website.

### How can you implement this?

Set up three fireteams, one dedicated to the monetisation issues, each one dedicated to one of the topics mentioned above.

These teams should be nimble and be able to act with few constraints and red tape. I'd suggest the following structure:

- Each team has 1 senior backend engineer, 1 medior frontend developer, 1 senior frontend developer, 1 QA engineer, and 1 team leader who is also experienced with the code base and can help with code reviews and basic project management. Some teams might require additional backend developers depending on the complexity of the issue.
- Each team should start the project with a kick-off, determining all milestones from the start. One strategy might be to hold a 1-day meeting with several senior product managers, designers, backend engineers and infrastructure/devops, a compartmentalised list should be brought and each topic should be discussed, either accepted or rejected, and difficulty determined via planning poker.
- 1 additional project manager who oversees all 3 teams, reports status directly to Susan, and attends daily stand-ups for all 3 teams.
- 1-2 Infrastructure/devops engineers ensure that CI/CD are setup, test/production clusters are ready, and can immediately help with any needs (subdomains, socket.io, anything that needs to be deployed) during the whole part of the process.
- This approach, with a positive attitude towards change, and a healthy dose of open-mindedness, may ultimately not only save YouTube whilst feeding content creators, but it may also establish a forward-thinking platform which could outlive us all.

Signed,
The viewers.

PS. Big props to Dear Github for the inspiration for the style and wording of this post.

PPS. You have our permission to re-upload and modify this post as you see fit.
