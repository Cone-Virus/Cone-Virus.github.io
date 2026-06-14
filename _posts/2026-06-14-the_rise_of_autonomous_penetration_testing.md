---
title: The Rise of Autonomous Penetration Testing
description: Another introspection on how pentesting is changing due to AI
author: Cone_Virus
date: 2026-06-14 16:00:00 +0800
categories: [AI,Pentesting]
media_subpath: /assets/img/pentesting_and_ai_pentesting/
pin: true
toc: true
image:
  path: place.png
---

# Introduction
As I have been interviewing with different companies I have noticed a coincidental trend. That a lot of companies want to offer continuous penetration testing and that they want to do it through AI. Although I will not list any of the companies I am currently interviewing with I will however indirectly thank all three of them for the great blog post idea.

Personally I really like this progression. I think it is a good way for AI to enter the security space and the natural evolution of penetration testers. Additionally I am biased since I do enjoy programming, troubleshooting, and automation so its a win win for me.  

# Why this is happening?
You can honestly blame things like Mythos (Anthropic's frontier AI model currently limited to select organizations) and how it is trying to fill a niche while everyone else is trying to fill it with AI but that really isn't the case. Back in 2015 when OpenAI started and even farther before that when IBM had Watson there was always a push for having machines do more. 

It is easy to say the reason for this is to "take jobs" and honestly there is some truth to it. Companies already try to hire in less developed countries to cut costs so AI is the natural next step. There are way too many issues with this and I am sidetracking too much so I will get to the point on why AI in pentesting is happening.

In my opinion it is a "minimum quality" approach. A lot of companies need pentests for compliance or for just maintaining a minimum level of security on their platform. For this they have to deal with a company who has a slew of testers with varying skills. Trust me I am using "varying" in a liberal way. I have done tests the year after and questioned if the tester actually took the time to test the application. So by using AI you are guaranteed a minimum rather than gambling with varying quality from reputable companies.

# Man vs Machine
So what is the big argument here? Is AI taking our jobs? Can man out-perform AI as some companies claim they can? No one really has any definitive answer to these questions but there have been some interesting things to come up in this classic question.

One really interesting case and company to mention is the programming language `ZIG`. `ZIG` is a programming language that in short offers a new approach on how to debug applications and metaprogramming. The reason I bring this company up is what the founder said an interviewer.

"Invariably Garbage" is what he referred to AI as. With a policy of not allowing or using AI in his company. This is a pretty bold and almost cocky statement to make but I do believe this is the divide in tech that will further grow. In which those will oppose using AI fully with the belief that they can do it better and faster while others will depend on AI for every day to day task with of course those who fall in the middle that utilize AI a part of their workflow.

So it is impossible to answer whether AI or tried and true engineers are superior. Evidence as of late has suggested that engineers without AI perform better and that AI leads to more people pushing to prod without testing code. But on the flip side this has always been an issue without AI so I struggle to side with either extreme. This section is more of a food for thought since this divide will become more polarized as time passes.

ZIG Website: <a href="https://ziglang.org/">https://ziglang.org/</a>
ZIG Founder Interview: <a href="https://www.youtube.com/watch?v=iqddnwKF8HQ">https://www.youtube.com/watch?v=iqddnwKF8HQ</a>


## Pro's
### Faster and Smarter!
I'm sure anyone who is reading this has ChatGPT'd something niche and 9/10 times it was pretty accurate. Not only that but the time it generally takes to do this is incredibly fast. Not even including other companies such as Claude who seems to have a much more robust and capable agent that is just as fast. With this in mind, it signals the fact that AI really is smarter and faster than most people are. The amount of time it takes some people to look over thousands of nmap results can take an agent a few seconds.

Of course I am not going into the issues of this in this section but it goes to show the accuracy of AI as a whole. Not only that but the improvement of AI is coming in incredibly fast. Benjamin Todd has an amazing blog on this but the main thing I want to point out is this graph he references.

![AI Curve](1.jpeg)

It shows that AI is just becoming more capable. It's not just that but the sheer speed of how it's becoming more and more capable. It's less of a "When will we use AI" and more of a "When can we start". 

Benjamin's Todd Blogpost: <a href="https://benjamintodd.substack.com/p/the-most-important-graph-in-ai-right">https://benjamintodd.substack.com/p/the-most-important-graph-in-ai-right</a>

## Con's
### Errors o plenty
This goes without saying but AI is not perfect. It is getting oddly close to and oddly proficient but it will always need user validation to work in a commercial setting. I do also realize it is ironic that I am mentioning the error rate when I previously also mentioned how it is so smart and fast but please stay with me on this.

Think of AI more like that annoying HS friend some people had in which they were incredibly smart with academics but absolutely failed in any social setting because they failed to read the room. That is exactly the issue with AI in which it fails to read the overall context of a finding. 

Even recently in an interview I had I was tasked with reviewing how an agent rated an IDOR finding with very limited information. This exercise was rather fun not only because I like yapping about hypotheticals but it was an exercise to see if I am able to fully understand the context of what an AI is looking for. In some cases an IDOR can be a super dangerous finding that exposes user information but it can also appear as the normal indexing functionality of user profile pictures. So the failure to read general context is something AI is still struggling with at the time of writing this but it is getting better as time goes on and models improve.

### Actually Cheaper?
This is genuinely a tough question to answer. If you are running an AI model locally vs buying tokens vs just paying a dev. There have been some recent articles such as Nvidia's VP saying "The cost of compute is far beyond the costs of the employees".

Additionally, looking at the latest trends of higher power models like Fable 5 and Mythos(I assume Mythos will be public at some point) the cost of tokens are getting much higher. It is to the point where you have AI native companies spending half of their seed money because they don't understand how to moderate token costs or prevent token burn. These problems we will most likely see grow more and more as time goes on. Especially as we see traditional pentest firms trying to convert to a more AI fueled pentest firm.

Overall in most cases when trying to utilize AI in a commercial sense it is always going to be a balancing act on whether using high-end models is better and cheaper than hiring a full team. 

Nvidia Article: <a href="https://fortune.com/2026/04/28/nvidia-executive-cost-of-ai-is-greater-than-cost-of-employees/">https://fortune.com/2026/04/28/nvidia-executive-cost-of-ai-is-greater-than-cost-of-employees/</a>

### Where is the data going?
This is always something people will overlook. A lot of these companies really are just wrappers for ChatGPT or Claude. This also means all the data going through these "wrapper" companies are going to these huge AI companies. It causes an additional level of security risk in that the company has the client data and now the company and an AI company both have the client data. 

I know all of this sounds like I am crying wolf but based on the latest vulnerabilities as of writing this, it is a genuine concern. What if an AI company gets compromised? If there is a malicious employee that is being underpaid? It really is impossible to say but it is foolish to not consider these issues when handling customer data.

# Conclusion
With this all being said will AI actually take away penetration testing jobs? Most likely. Will it be as fast as people are making it out to be? Not in the slightest. If you have gotten through reading this short blog then you will most likely come to the same conclusion as me. AI really is the future of security but it is not a future in which jobs will go away immediately. AI still needs human validation and still needs humans to grow those testing capabilities.