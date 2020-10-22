# OSCP Lab & Exam Review and Tips
Written September 2020

TL;DR: commit to preparation. Complete every OSCP-related resource and you will pass.

## Intro

So I want this to hopefully be a bit more than the obligatory 'I passed the OSCP' , and offer some advice for those who want to take the exam as well as give my opinions of the course. It's a lengthy post, with advice from beginning to end of an OSCP path.

The topics we're going to go through:

#### [OSCP preparation](#Pre -OSCP preparation)
#### Purchasing the OSCP
#### Coursework
#### Buffer Overflows
#### Lab Report
#### Labs themselves
#### Pre exam prep
#### Exam itself
#### Exam reporting
#### [Post exam](#And after the OSCP Exam?)


## Pre -OSCP preparation

Before you pay for the OSCP labs, I would recommend that you take up the following free (or cheap) resources:

* [Over the wire](https://overthewire.org/wargames/) - specifically Bandit and Natas. Don't worry about the others, as I found that they weren't as relevant for the OSCP
* [Under the wire](https://www.underthewire.tech) - these challenges are to get you more comfortable with using Windows Powershell. I had zero experience with Powershell, and these challenges really helped give me a basic understanding.
* The Cyber Mentor's Courses) - take every single course this man has to offer. His first Udemy class and his YouTube videos are brilliant courses for absolute beginners, and his privilege escalation courses were incredibly helpful in the OSCP labs. I didn't take Tib3rius' privilege escalation course ( I have taken some of his other things) but he is also a great resource that you should learn from
* Hack the Box (Specific machines) - HTB is the recommended resource to get some hacking practice before you fork over a significant amount of money for the OSCP course. What I will say is, a third of the machines on the list on the link are harder than what you'll find in the labs or the exam. Equally, there are four machines that have literally no place being on that list as they were too CTFy or difficult compared to what you'll find in your OSCP course. Take really detailed, thorough, methodical notes here. Practice creating detailed writeups so you'll be well-prepared for the reporting requirements for the OSCP. You can find my HTB writeups here if you're interested.
* Try Hack Me (https://tryhackme.com) - I don't have too much to say here other than if you're an absolute beginner, and you're struggling on Hack the Box, switch to Try Hack Me and do a couple of free machines. Try Hack Me comes with hints/answers as you go, and the hand-holding is nice....but you need to get away from this mentality as soon as possible as the OSCP does not hold your hand at all.
* Writeups - Perhaps conflicting somewhat with my previous statement, I really recommend reading writeups for machines. Sometimes if you're painfully stuck on a machine, read a writeup. Some people say you should stew and suffer, but honestly there were times in Hack the Box that if I didn't read the writeup I NEVER would have learned something. Moreover, once you've learned it you will never get stuck on that kind of obstacle again. Writeups - as long as you don't turn to them straight away - are an invaluable tool that teach you how others' approach a machine. There are of course IppSec's videos to learn from, which I recommend as he offers you a lesson in mentality as much as he offers you the answers.
* Vulnhub - just my subjective take on the matter, but I didn't find a single Vulnhub machine that I enjoyed. HTB or Try Hack Me are better choices for you to spend time on.
* Note Taking - I used Gitbook for my note taking on Hack the Box and the OSCP labs. It's like google docs, in that it 'backs up' externally to your computer so you don't lose any notes if your VM crashes (which will happen plenty). Gitbook also has a good search functionality, so if you see port 1433 in the OSCP labs and think that you encountered that before it's as simple as searching for it amidst your notes. I did find that Gitbook wasn't that reliable for images (it seemed like some of mine would disappear after a few days) so maybe export the notes as PDFs if you're attached to keeping your images.

## Purchasing OSCP

When you're ready to purchase your OSCP course, there are a number of options for what you can pay for. I'm not going to dwell on this for too long but what I will say is this: if you have children, intense work commitments, or an unforgiving significant other - choose the 90 day option. If you don't have children, if your workplace is understanding, and if your SO is forgiving - choose the 60 day option.

OffSec can take up to a fortnight to accept your payment and send you the course details, so please do keep this in mind when it comes to scheduling and timing. I didn't realise there would be such a gap in time, and ended up losing losing a week of time I had set aside for the course.

## OSCP Coursework

For the majority of the coursework, I was frustrated. It felt like 800 pages of content that was outdated and time-consuming. Looking back now, though, I see that OffSec weren't trying to teach me answers but were in fact trying to foster a mentality in how to approach tasks. The content isn't all bad either, as there was some techniques and tips that I was genuinely impressed with and used in the exams.

There may be some who say that completing the coursework is not worth the five points you receive towards the final exam. I say those people are either overconfident in their abilities or misunderstand simple math. As there's little we can do for the former, let's examine the latter: the OSCP Exam comes in the form of five machines, with two 25 point machines, two 20 point machines, and one ten point machine. One of those machines is a buffer overflow machine (which is a guaranteed 25 points). When you add up a combination of a handful of these machines, you can start to see how five points can be the difference between a pass and fail. Moreover, let's just say you pass with what you think is 73 points but OffSec deduct four points because of sloppy reporting. That's a fail. Whereas those extra five points you would have received from the coursework would have pushed you into a more comfortable passing mark.

In essence, the coursework is dull and painful for 90%. But the 10% of interesting stuff, plus the five points, makes it undeniably worth it. Please do the coursework. I would recommend banging out the course report as soon and quick as you can. I spent eight days, giving fifteen hours a day just burning through the course so I could get it out of the way. I will assume you're more intelligent than I am and will get through the coursework much faster than I did.

## OSCP Coursework: Buffer Overflow

The buffer overflow section in OffSec's course pdf is awful. It was my least favourite part of the whole course, and it kept coming up again and again throughout the 800 pages. They don't explain it well from the beginning and that confusion persists as you go through the BOF sections. It's the only part of the entire course that I was actually frustrated I had paid OffSec this much money.

Fortunately for me (and now for you) I had gathered some resources before starting the labs and had already perfected my BOF skills. I would recommend you first follow Heath Adams' Cyber Mentor BOF guide. He teaches the part-manual, part-automated method, and helps you understand some of the theory. Once you've completed this, then move onto Tib3rius' BOF practice room on Try Hack me. It teaches you the mostly automated method for a BOF, and it is the easiest, quickest way by far. Heath's guide is necessary, as he teaches you a middle-way that makes sure you wouldn't be lost if your automated tools stopped working. OffSec's method is maybe too manual. And I understand that they want to impart the lesson of doing things manually, but for a topic as confusing as BOF it's better to use Tib3rius' automated BOF methods that are allowed in the exam.

OffSec is gonna have you working those bad characters out manually, eyeballing each one in tiny font six. And you're gonna do it, as that's the requirement for passing the coursework. And you're gonna fuck up one of those characters and your exploit won't work, because human error is bound to kick in when you're doing with that many slashes, x's and 0s. All I can say is sigh deeply to yourself and do it OffSec's way for the coursework. Come exam time, Tib3rius' way is the way to go.

## OSCP Lab Report

The other requirement to get those five points is to complete ten machines in the OSCP lab, and ensure that you have documented these in a report. I don't have much to say about this either, as it's straightforward and you would be doing yourself a disservice if you didn't create ten writeups of machines you're going to hack anyway to get yourself points towards the exam.

For both the Lab report and Exam I used more of a 'boot to root' style of writeup. I found OffSec's example report to be too confusing to actually follow per machine. It makes sense in a real world engagement to produce a report that looks at things per vulnerablity (not per host). However this isn't the real world, so feel free to use a walkthrough style for your reporting too.

## OSCP Labs

The labs are around sixty vulnerable machines split across a handful of networks. You will have immediate access to around forty machines, with the remaining machines hidden in those secret networks. I completed every single machine, as I saw these as 'practice exams'. Therefore my logic was completing every practice exam meant I would be in better stead for the real deal.

I want to address two major criticisms I have about the OSCP labs.

First is to OffSec and it's about dependencies. Some of the machines require you to have rooted other machines, and stolen passwords or files from those. Now there's nothing wrong with that, but please do let people know that these are dependent machines. I shouldn’t have to go onto the forums - where spoilers are everywhere - just to try and workout if a machine I'd spent all day on has a dependency I don't know about. To me, it would be as easy as calling a host 'Topcat-Dpndt' so students know.

Second criticism are to the people who say not to bother with the secret networks in the labs, or bother with the Active Directory machines in the labs.. Their justification for this is that "SSH pivoting/Active Directory isn't relevant for the exam". Now this is true in part, your test will not feature dependent machines. But your exam may feature some things that require AD knowledge, or require you to forward an internal service from a machine back to your kali for privilege escalation. Moreover, the secret networks are where some of the really hard privilege escalations are. Everyone goes on about the 'Big Four' machines and okay those were hard, but man some of the techniques I learned in the secret networks were incredible. Some people have a goal of 'complete 30 machines, complete 55 machines' etc etc. I don't know what their motivation is to not do all the machines in the lab - maybe they have time constraints, or have confidence in their abilities - but all I know is that doing every single machine benefited me hugely during the exam.

I wanted to critique the Student Admins, who are on Helpdesk for any tech issues you're having as well as to give you pointers on machines. I only had two experiences with student admins, and whilst they were both nice people I think that English was not their first language and as a result their advice (and the conversation in general) was difficult. When someone is trying to give you a cryptic hint to a machine, and their command of English isn't that strong, it's not gonna go well for you. However I am reserving this as an actual thing OffSec should improve as I don't see how they could. They could hire student admins who have demonstrably high-level fluency in English, but maybe they do and I just got unlucky the two times I communicated with them? At any rate, I would gladly sign up to be a Student Admin as I would enjoy advising fellow students on hints and tips throughout their labs.

## Pre-Exam

Book your exam date as early as you can, as the slots fill up quickly. I know it's difficult to know what life will be like two or three months time, but it's necessary I'm afraid. You don't want to leave a big gap between finishing the labs and doing your exam.

A fortnight before your exam, email OffSec and ask for a test session for your equipment. As the exam is proctored (someone watches you via webcam and monitors the activity on your host OS' screen) you need to test and make sure all the software works. The last thing you want on exam day is for a tech problem to eat into your time or have your exam cancelled. My host OS was Kubuntu, and I used this camera which said it worked for Linux systems, so I definitely wanted to test my system and make sure it all worked well.

Please keep hardware requirements in mind too. I'd recommend you have at least 16gigs of ram, as you won't just be running your VM but you'll be running the proctoring software too. You'll also want good ram, and a computer that won't overheat, as you'll be running the machine for long periods of time and it will be doing intense work. The last thing you want is for your computer to die mid exam!

## Exam

I won't go into detail here, as the OSCP exams are not to be discussed at length.

My approach to the OSCP was a commitment to preparation. I wanted to make sure that no matter what was thrown at me, I had experience in it and wouldn't be faced with a service or configuration that I'd never seen. This paid off, as within four hours I had gained enough points to pass, and after eight hours I asked the proctor terminate my VPN connection.

I would strongly advise you take perfect screenshots and okay-ish notes whilst you're hacking the machines in the exam. This will make the reporting requirement easier.

Keep two copies of the Kali exam image, and use snapshots just in case. The last thing you want is for your VM to break and not restart.

## Post-Exam

After you've rooted your exam machines, you need to write your report and submit it to OffSec. Be meticulous here. Don't just screenshot what you did, but also include the commands you ran. I want you to write that report like your significant other, your grandma, your dog is gonna pick up that report and follow each page so they can re-create every step to root. This doesn't mean you're going to write the report like its a 'explain like I'm five'. Rather, you're going to write the report that is replicable and clear.

Once you've written your exam report, you're going to send that and your coursework and lab reports to OffSec. OffSec have a dedicated page for their exam guide, focus on section three. It is entirely possible to root every single machine, complete every single coursework and lab requirement, send off your reports and fail the exam. Why? Because OffSec's rules for exam submission are incredibly punitive, and require you to zip reports, password protect them, upload them, copy links and email them - it's a highly-choreographed dance that OffSec has us do post-exam, and they don't explain it well.

This is an area I am hugely critical of OffSec for. They don't need to fail a person who rooted every machine and completed all course tasks just because they sent 'exam report.pdf'. I understand they have thousands of students, and can't chase them all up to meet administrative requirements. But, OffSec, that IS all you'd be failing someone for: administrative requirements. In real life, I have not found that a client will refuse payment because of a report name, or will reject an entire report because they had trouble unlocking the password-protected file.

This is an area I would also like to OffSec improve on, as they have strict rules but do not explain it well. For example, does the coursework report and ten-machine-lab report get submitted in two separate reports, along with your exam report, or do you condense those two into one course/lab report and send that off with your exam report? I don't really know. I did the latter. It seemed to be okay for me as I passed, but greater clarity from OffSec would be even better.

## And after the OSCP Exam?

OffSec state it may take thirty days to get results, but from what I've seen most people get their results within five days. I imagine a weekend submission may take a little bit longer. I did my exam early in the weekday and received my results midday two days later. The certificate does seem to arrive a little bit more erratically, due to COVID 19, as I haven't worked out a pattern of who receives theirs and when. I passed less than a week ago, so I won't see mine for maybe a little bit more.

And that's it, that's everything I have for you. I hope that was informative. It was certainly cathartic to write, and I hope it can offer someone some guidance or reassurance. I'm always available for a chat, whether that's here in the comments, in a DM, or my [Twitter](https://twitter.com/Purp1eW0lf) .

I'm hungry for more certifications, and I'm hoping OffSec update their OSWP course soon so I can sink my teeth into that. I've got eighteen months left to complete my InfoSec doctorate, and I'm also looking for Junior Pen Tester positions in London, as I want that guidance and mentorship in the professional world.

Take care of yourselves my friends.
