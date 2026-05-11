---
title: Developing the Perfect CTF Challenge
description: A blog condensed of both my experience and views on how to develop the perfect CTF challenge.
author: Cone_Virus
date: 2026-05-10 16:00:00 +0800
categories: [CTF]
media_subpath: /assets/img/developing_the_perfect_ctf_challenge/
pin: true
toc: true
image:
  path: place.png
---

# Introduction:
This blog is just a mash of what I have learned about what it takes to make the perfect CTF challenge. This includes how to develop a CTF challenge, the type of events CTF challenges are used for, and how developing them can be beneficial to those looking to level up your skills. 

That being said I will go over each part in this blog. So do feel free to skip to any parts you feel are relevant. I do personally (unbiasedly) think that each part of this blog is important to read but I am not one to tell others what to do.

# The Many Factors
When developing a challenge there are way more factors then you may initially think of. When you go to a conference they aren't going to make challenges that are taking 5+ days to do. But at the same time if you do a CTF such as the google CTF then they expect you to dig for days on end. This all just shows it is important to understand not only your audience but also the event the CTF will be used at.

## The Types of Events

### Online CTF
This is the most common type. Generally it is run by a group of volunteers for a convention or they just like making CTF's. This also includes companies such as HackTheBox who do CTF's pretty regularly and often.

These tend to be the most competitive and the hardest to place well in since there is no location issues involved with them. That being said it should not deter you from actually doing one since you will learn regardless of if you win or not.

### In-Person Conference
Lots of people and lots of fun. I enjoy these the most since they are the few times I leave my apartment to do anything outside. They are a great way to network, chat with people in the community, gain new perspectives, and communicate directly face to face instead of just a screen.

The only big issue for these events is internet connectivity. Usually they suck and there is no actually reliable way for a conference to host good internet due to cost and number of guests. Sometimes it isn't so bad and some people bring their own hot spots but I will say this is the only drawback to these types of CTF's.

### College CTF
These can be either very fun or very unfun. They are generally catered to beginners within the field in college and if you are a college kid then I highly recommend considering doing ones run by other university clubs. Additionally there are CTF's such as NCAE Cybergames that does CTF competitions specifically for colleges.

But the downside of this of these are they are as good as the people running them. This can be said about any CTF but I find that the ones run by college clubs are either very well organized and well made or poorly organized and poorly made. I am yet to see a in-between for them.

### Job-Based CTF

#### Pre-Interview
These are by far the weirdest and tend to be much easier then what the company actually expects from you. I have done one of these (I will not name the company) and it led into a 7 part interview process. I didn't make it past that first interview but in my defense I was still depressed from losing my dream job due to economic downturns. 

I would recommend to avoid them unless you are needing a foot in the door or you are in college looking for that first job. Even then you are better off just mass applying to numerous other jobs for a better and faster interview experience.

#### Interview
From personal experience I am seeing these go a bit of the way of the dodo due to AI. When they were more popular (Some companies still use them) they tend to be pretty geared to you being aligned with understanding the challenge and reporting on it.

I say this from experience since if you have to do the challenges/challenge then you better understand what you actually did. I have done a few and have noticed a lot of the time a company will want you to struggle to a degree to see where you go and how you try to understand the issue.

Although I am not a fan of a company telling you to "Write a report" without telling you how they want it formatted but I assume that is also apart of the interview. When it comes to interviews you will most usually be fine as long as you are applying to something you can actually do.

## The Types of Competitors
When running a CTF an important factor for that CTF is "What type of people will do it". A lot of times this can be overlooked but it can really make/break any good competition. Things such as having a support channel, active admins who have access to the solutions to help troubleshoot, and having a way to make announcements to everyone all help both make an even playing field but also make the competition more fun for everyone. All of these things are common for a CTF but thinking of the types of people who will do the CTF will help things as a whole.

### The Veterans
These are the people that have done numerous CTF's. They understand they may/maynot be the best at the competition but will definitely let you know when something is broken. When encountering people like this you need to make a firm stance on not giving hints. I know this sounds odd these type of people will try to get any little bit of information out of you to get a leg up. Is this cheating? Kind of ya. But is it in the nature of someone who is doing hacker-like things to do something like that? 100% ya. 

As a personal note I have learned these people hate doing any sort of "misc" or "Steganography" challenges. They are deemed as "dumb" and "ctfy" which is a semi-slur when it comes to CTF developers. If you know the competition will be less beginners and more people who have a few competitions under their belt. Then I HIGHLY recommend refining your categories to be as realistic as possible and the least amount of guess work.

### The Genius's
These will most likely finish the entire CTF before you can release the rest of the challenges. Straight up they will pop a redbull right after finishing all 50 challenges within the first 4 hours of a 24 hour CTF.

As much as it is easy to hate these people they are incredibly fun to interact with. They tend to chat more and ask about intended solutions, they write blogs on challenges helping with overall exposure, they will even point out any issue with your challenge in a professional format.

Overall you will see these people the most and they will usually land in the top five. Usually they are really cordial people (Unless it is a Steganography challenge) but overall an important part of the community since they tend to contribute.

### The Beginner's
These are also common to see. They are generally trying to get their feet wet in the community and trying to see if this is something they are interested in doing. They can also be people who have been in tech for a long time looking to pivot.

If you ever and I mean <b>ever</b> encounter anyone like this in the community it is your job to be nice, helpful, and respectful to them. I have seen a lot of gate-keeping in my day to know when people hate to see new people succeed but the reality of it is we are all here to learn. Not to drag each other down.

Beginner's don't usually place well or even land on the leaderboard. But it just takes one positive experience to get them to do their next CTF until they end up placing top 5 or give some of the more well known CTF teams a run for their money.

### The "Instant Gratification" Competitors
These are pretty common in this day and age. They want to compete to do well but they don't actually want to try. They sometimes suffer from impostor syndrome and may get angry and blame you or the challenge if they can't solve it within 10 minutes.

When dealing with these types of people you <b>always</b> want to approach them as calmly as possible. They sometimes cannot control their anger due to dopamine dependency so always give it a rational approach as if it is any other competitor.

Most importantly they aren't usually at the competition to learn but just to win. They sometimes can be incredibly smart or not. One thing I do recommend if they approach you is to try to convince them that they should dig further or try harder (Do not literally say "Try Harder"). Nudges for people like this given the right motivation can actually help them out immensely and show them how struggling is a sign of improvement.

## The Types of Challenges

### Web
This is the bread and butter of most pen-testing, CTF's, and overall a big part of security. It is to the point that when you get far enough into your career you are expected to be good at web AND another niche discipline like cloud or AD.

The things that make a good web challenge are as follows:
1. Is it realistic?
	- This question always makes me pull my hair out a bit. When making a challenge you always believe there is a certain amount of realism to it which is good but there is a difference between reality and what you believe. What makes a web challenge realistic is if the vulnerability in the challenge can actually be found. Not that you made it vulnerable (ik sounds weird) but something that if you went onto google right now you would see a website with a similar function that is <b>hopefully</b> not designed in a vulnerable sense.
2. Is it robust?
	- This is another part of what makes a good CTF but for web it is a <b>huge</b> part. Will the challenge crash? What happens if 1000 players exploit it at the same time? Do you have a way to reset it? These are all things to consider but it is most importantly a good idea to assume someone will find a way to break the challenge. With this mindset you must be ready to reset, hot fix, or even announce issues. Now I am talking about this drastically and can say this has only happened 5% of the time in all the CTF's I have seen and been apart of but its still good to consider.
3. Is it too hard?
	- Ranking a web challenge is probably one of the hardest and funniest things to do. Something that is easy for you could be insane for a hardened CTF vet. So it is always a good idea to have a good QA who understands difficulties and to even play the challenge itself. It never hurts to throw a few hints in a challenge.

With all this said, it does apply to many other categories of challenges. Yes there is a lot of overlap, and yes I do know I could of formatted this blog better. But I still consider it important to understand each part and perspective to better refine your skills and understanding.

An example of a web challenge I made would be this : <a href="https://app.hackthebox.com/challenges/neonify">Neonify</a>

### Hardware
I personally do not have much experience in hardware exploitation other then some UART exploitation and pogo pin firmware ripping.

For these I consider this to be more of a "in person" event for a conference but I am sure you can upload firmware for people to exploit.

I would recommend checking out the electronic badges at defcon for a bit of inspiration which you can see here: <a href="https://github.com/Professor-plum/DefCon26_Badge_Solution">https://github.com/Professor-plum/DefCon26_Badge_Solution</a>

Another good one is 5n4ck3y which is really cool vending machine which I HIGHLY recommend starting early <a href="https://forum.defcon.org/node/245451">https://forum.defcon.org/node/245451</a>

Below I will include more resources that may help with hardware hacking but as a whole it takes a different type of researcher to pull it off well.

### Crypto
You have to be some sort of math wizard to do these sort of challenges. A lot of it comes down to what is cryptography and at what level of difficulty do you want to make the challenge?

Is the goal to make a custom algorithm and have people crack it? Is it to use a known vulnerable algorithm and for people to exploit it? or is the goal to have people confused on some Steganography challenges and get upset since why did you make a stego challenge in 2026?

I do not have any experience developing them but doing them I do think making custom algorithms is the best approach to making these challenges. They tend to be the most complex and fun while at the same time getting people to actually think about challenges from a different perspective.

### Reverse Engineering/Pwn
I have some experience on this but not enough to speak to it on a high level. The one time I got close was reading the 10+ page writeup of a challenge someone made for the RTV CTF at defcon in like 2024 I think?

But ya my point is a good reverse challenge isn't exactly hard to make its more so how much time you want to pour into it and how challenging you want to make it. Since you can always take away debugging symbols or use godot which is known to be harder to reverse.

Ultimately I do recommend learning a bit about it and seeing how it clocks with you. The challenges are hard to make but more so harder to make difficult yet fun.

I would recommend looking up pwn college since they have overall excellent resources on learning this. <a href="pwn.college">pwn.college</a>

### Game Hacking
This category is oddly similar to Reverse Engineering. It is mostly trying to figure out why a game is doing what it is doing and finding a way to exploit the logic in the code. 

Some games can be online/multiplayer but the dev time for these do require a bit more oomph to them as well as figuring out a reliable way to host it. I have personally created a game in Godot for a challenge that was hosted and will say its pretty fun to setup a server with clients.

Here are some engines I recommend you should learn if you want to dive more into game hacking:
- <a href="https://godotengine.org/">Godot</a>
- <a href="https://www.unrealengine.com/">Unreal</a>
- <a href="https://unity.com/">Unity</a>

I do realize these are the big ones but they are also the best ones to use.

But to learn game hacking I personally recommend this <a href="https://guidedhacking.com/">https://guidedhacking.com/</a>

I will say make sure to read the rules and you are not aloud to use a VPN. The owner is more then willing to ban and block people who do not follow the rules.

### Programming
I am personally a huge fan of these but a lot of people tend to hate them. Although AI has ruined this category a bit since you can just have chatGPT solve the challenge for you.

The concept of a programming challenge is as follows:
1. The player connects to your service.
2. The service sends the player a challenge/problem to solve.
	- think like "2+2" or "Solve this maze".
3. The player sends back the solution.
4. Assuming the solution is correct it repeats a lot
	- Think any amount that is humanly possible to do by hand.
5. Once they solve all 1000 or so problems in 10 seconds they get the flag.

These challenges are great for college/high school competitors since it forces them to learn automation and troubleshooting for a challenge. I also enjoy the fact it can be done by anyone who knows a little code no matter the level of cybersec expertise they have.

### Forensics/Malware
Forensics are fun to make. They tend to be a lot of clues and artifacts that you package together in an environment/file that a user can take apart.

One thing I have learned is to never make the flag plaintext for these challenges. It needs to be obscured to a degree since most of the time a challenge can be defeated with a single grep or strings oneliner.

Additionally malware challenges are super fun to make. They are a way to combine reversing, counter-hacking, and forensics into one challenge. The challenge I made was based on <a href="https://en.wikipedia.org/wiki/Rensenware">rensenware</a> but with a anime twist to it. I got a lot of praise for it and I do recommend making it to learn how to develop malware as a whole.

Aforementioned Challenge: <a href="https://0xdf.gitlab.io/2022/02/07/funware-cactuscon-2022-ctf.html">https://0xdf.gitlab.io/2022/02/07/funware-cactuscon-2022-ctf.html</a>

### Misc
This is by far the silliest category but at the same time can be the easiest or hardest category in a CTF. Usually this category you put challenges in that you don't have enough challenges for to make their own category such as OSINT, cloud, etc.

Usually you can make a "rules" flag that can only be found of you read the rules. Additionally putting up challenges that are more beginner friendly in this category is ideal for beginners to boost their ego a little by getting "some" points.

That is not to say you cant drop some cicada level of tomfoolery as a challenge in this category. But it is a good idea to keep in mind when you make challenges that have no other place to go in a competition.

## The Cycles of Development

### Getting the Idea

#### Brainstorming
Getting the actual idea for something is actually and by far the hardest part of all this. Not only what the challenge is but how to build it and even how to theme it.

For this part it is very hard to actually give any advice or words of wisdom. This is always a struggle for me and I generally take even longer to come up with a few ideas then to make a single challenge.

I will say looking at current events, past events, memes, and anything that could be turned into a challenge and writing it down does help. I had a interest in malware so I developed a malware challenge which even got reviewed by someone big in the community. So if I had any advice to give it would be to write down whatever comes to mind.

#### Logistics
There are a few things to think of for this such as:
- Is the challenge hosted?
- Is the challenge a file?
	- How will it be hosted?
	- Where will it be hosted?

These are important factors to consider. If your team does not have a way to host actual challenges then you may need to focus more on file based challenges while at the same time you may want to focus more on network based challenges such as web since downloading large files can take hours on limited networks for in-person events (Defcon).

#### Theme
The theme of a competition is generally what you want to follow for a challenge. If the competition is a spooky theme or a retro n64 theme then you should theme a challenge off of it. If that isn't possible that is <b>honestly</b> ok. There are numerous times I got so tunnel visioned on the theme rather then just making a challenge it ended up taking 3x as long to make a single challenge. Basically just keep an open mind while trying to align with the competition you are making the challenge for.

### Putting Code to Metaphorical Paper
This part is will either be the easiest part or the hardest part. It is pretty hard to say and it depends on how well you are at development.

A few pieces of advices and why I made this a section is as follows:
1. Comment your code
	- Yes I know we all hate to do it and some of us do it too much to the point it impacts the file size in a meaningful way but it is 100% the best way to write code to help you understand what you need to do, what that section is for, and to just keep track of where you are.
2. Debug in chunks
	- This is more common sense to some then you would think. You need to ensure that each section of code works as intended and trying to debug 800+ lines of code at once is horrid compared to breaking it into 100 lines and seeing what broke and what still works.
3. Modularity is key
	- It is hard to consider this for a challenge because why would you put extra work into some code? Well sometimes you can re-use code for other challenges. For example I made 10+ programming challenges using the same base code because it worked well and it was easy to swap the challenge part. So this is more of a "Save time in the long run" thing.

### QA Cycles and Why
You may think of a challenge and go "This is perfect so lets use it". But because of that personal bias it may not actually be the actual case.

A 2nd party can help you point out confusion, test if the challenge is reliable and will not break, and will test if it actually solvable. They can always use a solver but the issue with that is "Well of course it is going to work. it is designed to solve the challenge". 

These are just things to consider. They help in general software development and they help with designing CTF challenges. Of course if you are by yourself and unable to get QA then you can always run through the challenge from the intended perspective. It is not ideal at all but it is better then nothing.

### Supporting an Event
For this it seems more like common sense reading it then actually doing it but there is always 2 things you need when it comes to supporting documentation.

1. Solver/Solution
- Simply some way for the challenge to be automatically solved and documented reasoning on why it is solved that way. Both are important so if another person running the event helps someone they have the resources and knowledge necessary to know if the challenge is broken and to even nudge the person into the correct direction.
2. Backup Files/Self-Repair
- Files break, downloads break, servers break, a steel rod will break if you let enough people poke and prod at it. It is always important to have a backup plan for the challenge. Even if it is a centralized place to download the challenge files, a way to rate limit for web challenges, and to reset servers after a certain amount of time or if files are missing. All of these things help an event run smoothly and reduce the amount of work needed to be done during an event.

## Why make/do a CTF 

### Mindset

#### Making
You will spend weeks on end thinking, creating, and QAing challenges for a specific deadline. You will align every challenge for that event knowing there is a good chance that challenge may never get used again. It must always be approached like a sand mandala.

#### Doing
You will constantly search online for a CTF to compete in and carve out time in your and other people's schedules. You need to coordinate to a degree on what challenges you can do and others. Importantly making sure everyone actually has fun. 

### Reward

#### Making
You can easily make a name for yourself in the community and even make some cash doing it. I have made challenges in both situations and I can definitely say they are both equally rewarding.

Additionally when you work on a team you get to learn from others and the challenges they make. It helps build on collaboration, communication, and inter-personal skills that will help you no matter where you end up.

For those interested in making a little cash I do recommend HTB:<br>
<a href="https://www.hackthebox.com/">https://www.hackthebox.com/</a>

They can be a bit rigorous on their requirements but it is def worth it. You can always network with companies who are looking for CTF content development. 

#### Doing
From this it really is a "How much you put in is how much you get out of it" sort of routine. If you are fully willing to accept losing numerous times in competitions, spending numerous hours on 1-2 challenges, and consuming large quantities of caffeine. Then ya this is the exact thing you want to do. 

You will get a bigger boost of dopamine capturing a flag to an insanely hard challenge compared to any video game achievement there is. You will network and make a name yourself that matters more then any gaming leaderboard.

For me, This is how I got involved in CTF dev. It is how I met a lot of the friends I still semi-chat with till this day. I personally recommend everyone in Cybersecurity to do a CTF every once in a while. Even if it is just a HTB challenge or burp suite lesson. It is a rewarding experience. 

### Resume Padding
I am not going to do categories for this since they are roughly the same. In my opinion they are both equally beneficial to those from early career to late career. For those later in their career, it could be just a note on linkedin or talking point. But for those just getting out of college it is something that will set you apart from the hordes of others.

# Conclusion
I hope after reading this you have a bit of an idea on why CTF's are so important and all the nuances to CTF challenge creation, Learning why some competitions are more widely known then others, and why it is important to always stay curious on learning more.

Overall I would not be where I am today if it was not for me taking the leap freshman year of college and actually doing competitions, Pivoting into CTF Development, and then networking into my first internship. I wish for everyone in this field to have the same chances that I have had and to try pushing yourself even if bed rotting on tiktok is more appealing then anything in life.

I also want to say thank you for taking the time to read or at least skim this blog. I know this may have not been the most organized or best read but I do appreciate you being apart of my journey into finding a new job.
