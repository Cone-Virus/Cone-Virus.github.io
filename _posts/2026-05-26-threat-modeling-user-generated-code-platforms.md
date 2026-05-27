---
title: Threat Modeling User Generated Code Platforms
description: An introspective on the threat model for platforms such as roblox, github actions, and claude
author: Cone_Virus
date: 2026-05-26 16:00:00 +0800
categories: [Threat Modeling]
media_subpath: /assets/img/threat_modeling_user_generated_code_platforms/
pin: true
toc: true
image:
  path: place.png
---

# Introduction
 
Recently, during my job hunting, I was interviewed for a role that involved threat modeling. This topic interests me because, as a penetration tester, it is something that can easily be overlooked. It is a part of older styles of penetration testing in which the client would give you a "Pentest Doc" — essentially a collection of theoretical scenarios they want you to evaluate. In my career I have only seen this twice, and both times they never clicked until recently.
 
With that being said, I thought of current examples in which threat modeling exists for user-generated code, since a lot of computing is moving into the cloud and data centers, making running on your own hardware less common. This, in my opinion, opens up a lesser-thought-of threat: "What if the user code is malicious?" I know a lot of companies have thought of this and do have mitigations in place, so I thought it would be interesting to do a bit of a deep dive into how they actually pull it off.
 
# Case Studies
 
## Roblox
 
For those who are unaware, Roblox is an online game platform where users can submit games for others to play. It promotes playing games with others, creating games, and an overall sense of community. It appeals more to younger audiences due to its simplicity and the free access to its games, but the part I find most interesting is how Roblox manages the risk factors of potential bad actors uploading malicious games.
 
### Lua with an Extra U
 
First, it is important to understand what language Roblox uses for its games. Unlike platforms like Steam, it is an all-in-one platform, so there is no need to worry about compatibility or other potential issues that come with game distribution.
 
Roblox's approach is to use a language known as "Luau." This language is derived from the 5.1 version of Lua, released back in 2006. This may make you wonder: "Something so old should be full of holes like Swiss cheese." That was also my initial thought before digging into what actually makes this such an interesting choice from a security perspective.
 
Things such as:
 
- Removing the `io` and `package` libraries.
- Restricting the functionality of the `debug` and `os` libraries.
These decisions create a very strong sandboxed environment specifically for users of the platform, providing protections for users who casually click on one of the thousands of games available. That is not to say cheating doesn't exist — Roblox themselves recommend implementing your own version of anti-cheat. But as for whether a sandbox escape exists, I am personally unsure about what mitigating factors are in place.
 
Reference: <https://mobidev.github.io/luau/sandbox>
 
### Gambling for Kids
 
If anyone reading this has kids or plays Roblox, you will know what I am referring to when you look at some of the latest games. Loot boxes and season passes are everywhere, all designed to get as many Robux as possible and convert them back into real-world money.
 
You might initially ask, "How is this relevant?" while simultaneously thinking of ways criminals could leverage this, such as money laundering. Although that is an excellent thought, the conversion rate makes it impractical.
 
```
$10 USD = 800 Robux
800 / 10 = 80 Robux per USD
 
Inversely:
80 Robux = $0.30 USD
 
So this means:
$10 USD = 800 Robux (buying)
800 Robux = $3 USD (cashing out)
 
Resulting in a 70% cut to Roblox
```
 
For reference, I am using <https://rohire.dev/devex-calculator> to calculate developer earnings. But knowing this math shows that if you attempted to launder money through Roblox, you would lose a staggering 70% of what you put in.
 
Since money laundering is not a viable concern, the main issue that comes to mind is gambling. In countries like the UK, gambling for minors has become a growing issue, but in the US and other countries the regulation is far more lax. The problem is the degree to which Roblox actually regulates games that include gambling mechanics. Platforms like Minecraft have rules for servers that require items to display the percentage likelihood of being obtained. For a platform like Roblox, that is **much** harder to enforce.
 
Essentially, the issue is that a platform supporting a vulnerable population is exposing them to gambling within its games. As shown above, it is financially incentivized for game developers to encourage kids to spend more money so that the cash-out is a meaningful amount.
 
With all that being said, how is this relevant to a threat model? The impacts here are primarily regulatory and reputational. A platform that allows minors to gamble is one regulatory action away from losing a significant portion of its income.
 
## GitHub Actions
 
I will give a shout-out to this blog: <https://some-natalie.dev/blog/threat-modeling-actions/> it goes into much greater depth than I will here, so if you are a more advanced developer I encourage you to read it.
 
### The Ironic Twist
 
The ironic twist is that the framework for this blog Chirpy (<https://chirpy.cotes.page/>) uses GitHub Actions to compile the application. Could this be abused to use my GitHub repository to host malware, or could a malicious push from the Chirpy developers compromise my private repositories? Absolutely. But that is the reality of open source.
 
This is relevant to companies as a whole, since many large organizations love using open-source software they can just plug in and use. Rarely do they actually read the code. If you want a quick example of how bad this can get, look over this article on an older CVE for SSH that turned out to be malicious: <https://www.kaspersky.com/blog/cve-2024-6387-regresshion-researcher-attack/51646/>. The real threat here is less about GitHub Actions specifically and more about how people will run whatever they see. GitHub Actions are capable of stealing repository secrets, tokens, and cloud credentials — and with those keys to the kingdom, an attacker can do whatever they please with your repositories.
 
### Pipelines Aplenty
 
As of late May 2026, there has been a surge in NPM and dependency exploitation rather than targeting companies or services directly. There is currently a notable supply chain attack called `Mini Shai-Hulud` that is impacting a significant number of NPM packages.
 
It demonstrates that when threat modeling from an application perspective, you really cannot just use any dependency anymore. You need to understand why you are using it and consider your options: build your own version (not ideal in a production setting due to time constraints), freeze dependencies and hope there are no vulnerabilities in the older version, or review all the code for that dependency which can sometimes take longer than building it yourself.
 
The point is that exploits like `Mini Shai-Hulud` are not going away. CI/CD pipeline attacks are not new. But what makes `Mini Shai-Hulud` particularly interesting is its use of GitHub Actions as part of its attack flow:
 
1. **Theft:** Once infected, the malware steals GitHub tokens, NPM tokens, and other private or secret tokens.
2. **Persistence:** It writes payloads to `.vscode/tasks.json` and `.claude/settings.json` to plant backdoors on victim machines.
3. **Propagation:** It uses the `preinstall` hook to propagate to other NPM packages that depend on the infected one.
Reference: <https://www.aikido.dev/blog/mini-shai-hulud-antv-npm-supply-chain-attack>
 
## AI Agents
 
When I say Claude, I am not singling it out specifically — it serves as a case study for a much broader problem: the rapid rise of AI with everyone racing to be "first and best." Even now, numerous companies are competing to build effective AI hacking tools and prove they have the best in the business. The issue is that many of these companies are prioritizing innovation over security.
 
### The Clouds in the Sky
 
One interesting aspect of the AI integration hype is the data aspect — where your data is actually going. Anyone who uses AI for anything, from filing taxes to finding new recipes to conducting a penetration test, needs to understand the implications.
 
This becomes a gray area in penetration testing. External testing is, as the name implies, external. So if a company were to point an AI agent at a group of public-facing domains and discover impactful vulnerabilities, that could be acceptable to a degree since the targets are already public. The issue arises with client relationships a customer likely does not want it known that their public-facing websites are vulnerable, even if that information is technically public.
 
The real danger zone is internal and non-external penetration testing — engagements the public would never have access to, requiring VPN access or credentials to perform. Any data the tester provides to an AI agent is still being sent to a third party that may or may not use or sell that data. It introduces an additional layer of trust: not only must you trust the penetration tester and the client company to handle your sensitive information responsibly, but also the unnamed third-party AI the tester happened to be using.
 
I realize this is somewhat of a losing battle to argue. We are not at a point in history where every company can run their own AI models locally without leaning on data centers. But it is a risk nonetheless.
 
### What Can't AI Do?
 
With all of that said, what else can go wrong?
 
Let's look at one of the earliest publicly accessible AI innovations that demonstrated this risk: `OpenClaw`. For those unfamiliar, it is an open-source AI assistant capable of performing a wide range of tasks autonomously. It has a robust system whereby if it encounters a function it cannot perform, it will attempt to fetch a YAML definition for that functionality and execute it. It can run 24/7, check your email and texts, book flights, buy groceries, and pretty much anything else you can think of.
 
The issue with this innovation is who adopted it and how. For the most part, early adopters were less technically savvy, which led to some notable pitfalls.
 
The first major class of issues arose from `Skills`. As mentioned above, if `OpenClaw` cannot do something, it will try to acquire the ability to do so  and that is where attackers stepped in. By publishing Skills with malicious payloads, attackers were able to gain access to users' machines and install cryptominers or steal cryptocurrency wallet credentials. To learn more, I recommend this article: <https://www.trendmicro.com/en_us/research/26/b/openclaw-skills-used-to-distribute-atomic-macos-stealer.html>
 
The second class of issues is that `OpenClaw` and AI agents that ingest social media more broadly — can be manipulated through prompt injection. If the AI is ingesting social media posts or comments, an attacker who words a post correctly can cause the agent to treat it as a legitimate instruction, allowing a third party to interact with your AI agent, trigger actions, or exfiltrate secrets. More on this can be found here: <https://thehackernews.com/2026/03/openclaw-ai-agent-flaws-could-enable.html>
 
As a whole, you can see that we are not at a point where we can let AI act autonomously without human oversight. I do think that will gradually shift — to the point where human approval becomes a simple "yes or no" decision — but we are not there yet, regardless of how many safeguards are in place.
 
# Conclusion
 
The common thread across all three case studies is that the threat surface expanded the moment user-submitted content or third-party code was allowed to execute on the platform. Roblox solved it at the language level. GitHub Actions pushes the responsibility onto the developer. AI agents have not solved it yet. That gap is where the next wave of incidents will come from.
 
Thank you for taking the time to read this. I am not the most knowledgeable when it comes to threat modeling, although penetration testing is a complementary skill, I am more accustomed to reactive security than proactive security. If you are in the penetration testing space like me, I encourage you to take some time and read about your favorite games or platforms that accept user-submitted content, and what they do to proactively mitigate the risks.
