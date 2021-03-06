---
layout: 2015_layout
title: Session Transcripts
subtitle: A live transcription team captured the SRCCON sessions that were most conducive to a written record—about half the sessions, in all.
section: docs
sub-section: interior
background: remote
---
# Switching CMSes

### Session facilitator(s): Liam Andrew, Pattie Reaves

### Day & Time: Friday, 11:45am-1pm

### Room: Thomas Swain

LIAM: Hello, everyone, thanks for coming to Switching CMSes. I think we all probably have some stories about switching CMSes, so we want to get into them. This might turn into more of a cry session.

PATTIE: All learning, Liam. I'm Pattie Reeves, I work at Alley Interactive. Before Alley, I've done my share of switching CMSes for small metro newsrooms in Maine, and also Alley, we are digital agency and we do a lot of work helping clients switch CMSes, and mostly work with WordPress, though not exclusively.

LIAM: And I am Liam Andrew, I'm a developer at the Texas Tribune of the and we're in the early days of a CMS switch. Early days, meaning it hasn't really happened. I would love some help, please. But yeah, a little bit about the tech, we're a Django shop, so we have a couple of different things going on. I'll talk a little bit more about that in a minute. But first, I want to -- so who here is -- would call themselves a developer, technologist? And who here is a writer, editor, reporter? Or and then who here does not feel like they fit into either category. Or all categories? Cool. So I want to start by unpacking the two terms, choosing and switching CMS. Talking about switching a CMS is not just hey, which one should we do, should we use WordPress, should we use Rails? It's also about the process of moving it from one to the oh, which is both a technical challenge and an organizational challenge. It seems like it fit right at home in a place like SRCCON. We also talked a lot about what a CMS is in this day and age, it feels like pretty --

PATTIE: You guys all know what CMS stands for, right?

LIAM: Can CMS is a content management system. There are a lot of types of CMSes, I think, and we are increasingly pretty vague about the way we talk about them, at least in our newsroom. We have our core website. Plenty of places have a print CMS that's separate from their core CMS. They might have a different CMS to enter data into various data applications or explorers, they might have a different CMS they use for covering live events, they might have a totally different CMS for producing their own events, sending emails like in MailChimp or special one-off projects. These are all in a very broad sense, loose sense, content management systems so we're talking about it in a pretty broad, holistic sense.

A little bit more background at the Texas Tribune, so in the beginning with the Texas Tribune, we got a big grant from the Knight Foundation to build what we call Armstrong, which is a toolset for building CMSes in Python Django. That happened about six or seven years ago. There was a lot of building and then the community support didn't really come, or didn't really stick around. And we ended up with a lot of different -- probably about 30 different repositories that we were maintaining by ourselves. So there was a lot of -- so this is about three years ago, so we started to really intensely scale back. We were like, OK, so we just built everything in house and now we need to start outsourcing some of it. So we started to look at things like event rate for managing our events and MailChimp for managing our emails, starting to peel back these layers and thinking that we only need to maintain the core, in what we do, publishing the articles. So that's what was going on for a couple of years. We just did a rescaling of our admin and CNS and now we're on to the next question. For those of you who were around for yesterday's talk about distributed platforms, there was a lot of talk about how HTML is for instance for your CMS, we have a lot of that. So that's sort of where we're at right now and I have a lot of questions.

PATTIE: I don't have a slide, but my experience in this, at -- in about 2010, 2009, when I was at a small paper in Lewiston, Maine, we had a content management system for our printing out of the newspaper every day and a separate content management system for managing a website and we undertook what seemed like a very daring task at the time of getting rid of both of them and trying to do it all with Drupal. I think the technology has come a long ways since then and I have a lot of feelings about the organizational challenges around that, that we're going to talk about later. Then later I went to the Bangor Daily News we went to do a whole newspaper off of WordPress and also publish a website off of WordPress.

LIAM: So we were talking about what we want to change in a CMS when we're talking about switching a CMS, there's a lot of levels of engagement you could do with this, or levels of switching so you could just rescan your admin, you have the same model, same general structure for your data, but you need a new look. Maybe your users want a slightly popular admin, for instance. You might want to change your auxiliary content, stuff like your tagging, your taxonomy. It's not your core article stuff, but it's still all very crucial, maybe. You may have none-story content like events. Then there's the content editor, the text editor. A lot of us have horror stories about text editors so I called it a content editor so it would be a little more broad than that. And then the core, thinking about your models, the way that it gets presented to other platforms and the distribution model is another sort of layer where increasingly you're having to put your content on other platforms in other places, and to curate it, these are all -- all of these require different levels of switching, and they each require a different amount of lifting, both technically and organizationally.

PATTIE: So the challenges that we wanted to talk about today are technical in nature. When you're choosing a new CMS you're like, is this going to be a thing that people are talking about in three years? Am I going to be able to hire developers who could work on this? If I have the archive on a legacy system, how do I get it onto this new system?

There's the design, which we kind of are grouping like, does the way that content is stored in the system make sense for our organization and the types of stories or content that our organization is producing? You know, we highlighted that some big companies have created their on CMSes that fit like their specific kind of content and their content needs. And then there's like the organizational challenges around choosing a CMS. Does it make sense that you should -- you and your organization should develop and own and maintain that CMS, that your parent company should develop and own and maintain that CMS, that you should choose an open source project? That you should choose an external vendor to get a CMS from? There are pluses and minuses to both sides, and a final idea that we wanted to bring to the consciousness is how familiar is your choice going to be to your staff that's going to be using this CMS? Like, choosing something like WordPress can be very advantageous, because many people know how to use WordPress, whereas a CMS that is home ruled, you might be able to do like your own usability to fit it into your own workflow or doing something that might not be totally intended for the -- or developed for the problem you're solving, might make it more difficult for your users to use it.



LIAM: So going into the technical questions in a little bit more detail, some of the questions that we've had at the Tribune have been whether we want to continue to repair and upgrade our ship or jump out of the burning ship. It's not literally burning. It's OK. We could -- we also talk about whether -- yeah, whether we want to -- say we do want to jump ship completely, should we build our own thing or should we buy off the shelf?

We might want to do something different with our auxiliary content than we do with our core content and then there's also the question of user management and comments which is its own challenge, given a lot of the privacy and security issues you end up dealing with, for instance, and yeah, a lot of questions around your archive. This is a topic that's near and dear to my heart. Because it's been really painful recently. How do you retrofit your old content to new platforms or are there ways to keep your old stuff and maybe put in a freezer and move on with your new stuff and put it in your new place? Or are there ways to make it a little less painful to make sure that your archive content doesn't completely blow up when you try to put it on a new stack. There's also -- we have hundreds of articles with just iFrames and raw HTML everywhere and we don't know what's going to happen to them if we try to move to a new platform how to deal with them. Do we try to look for patterns to do it all at once? Or do we clean them all up? And I think there's a lot of questions around future-proofing your technology, too. how do you make sure that it's going to be supported, it's going to be maintained and that you're not going to need to do this same process next year.

There's also questions around once, you've chosen a stack, chosen a certain technology, there are still questions about how you might want to design your CMS, and this is probably newsroom-specific depending on what kind of content you make, but you can have one page that has all of the check boxes and form fields or whatever they need to publish a story or you can make it a pipeline. These are all continuums. It could be somewhere in between. But you might optimize for breaking news really quickly or you might optimize to make sure it is structured and validated and looks perfect.

You might want to optimize for making sure it conforms to your standards, it will be technically precise, or you might want to give some opportunities for some escape hatches so that people can do whatever they want, get a little creative and maybe break your CMS once in a while. There are questions around whether you want to optimize -- or not optimize, but do you have a focus, do you have a core canonical site that you are working exclusively on or are you just trying to push content out to other platforms or somewhere in between? And how does that all get managed?

And I guess it's kind of related but something that we've been talking about is how you bring analytics and sort of more data into your CMS from external sources, so for instance, should -- could your reporters be tweeting and managing their tweets directly from your CMS, or would you want to at least show them the tweet data? Did you want to give them the analytics, do you want to integrate with a third-party platform to do analytics or is that not something your CMS needs to handle or take care of at all. And I think every newsroom probably has a different answer to all of these questions.

Some challenges with migrating: You might want to just do it gradually to help either your users or your developers not throw a fit. Or you might need to do it all at once. There might be technical reasons, that for instance, that you have to say, hey, like we're doing this, it's going to be totally different tomorrow, get used to it.

Then there's plenty of organizational questions that Pattie was unpacking earlier. Yeah.

PATTIE: Um --

LIAM: Especially on documentation, I think that's a big question. Especially, so one challenge that we have for instance, we have a whole CMS user guide for our reporters and editors, so when we retool our CMS, we're also going to have to retool the documentation and there might be old pages somewhere that are still giving people the wrong information about how to use T I think also one advantage potentially to the training aspect is that can often build a rapport between reporters, editors and engineers in your newsroom. If you handle the training well and you show them that you're on their side and that we're all trying to get through this together, it can be really good.

PATTIE: Right, yeah, like as a developer, your job is working on the CMS, but on the other side, the editors and the reporters, their job is working on the CMS. So bringing the job along, especially to help reporters and editors to figure out why things are a certain way or finding out their pain points or how it could be better, could be really, really good in having a productive relationship as you go through your mission.

LIAM: Another thing is thinking about how your CMS fits into publishing on your website. I think when we think of our users as a group, we're often thinking about our readers, but in terms of CMS you're thinking about your reporters and people inside the newsroom. So if you're doing a sort of user-focused technical organization, I think that breaking out the CMS and thinking about that as its own set of components or its own set of users that you can go talk to all the time if you need to is a big opportunity.

So we -- you all have post-it notes, I think, at your tables. And we were going to just put --

PATTIE: We actually have questions. Let's go to the etherpad. It's that link, the goo.gl/rBLpRG. So what we'd like you to do is take a few moments, take the post-it notes and the pens on your table, and working alone, come up with your thoughts about the things that you love about your CMS, the things that you wish your CMS could do, and also like where you think, what do you think we'll be talking about in return -- in terms of CMSes five years from now. And we'll give you guys 10 minutes.

[group activity]

So it's been about five minutes. If you haven't started sharing with your group already, feel free to share with the rest of your group and see what common themes are coming up.

LIAM: If you're ready yet.

PATTIE: Yes, when you're ready. ...

PATTIE: I'd like to have us all come back together and talk about our ideas around these themes, and the themes that you came up with at your table. So why don't we start at the left. What do you love about your CMS?

AUDIENCE: With the caveat that most of the stable works at Vox Media so we're mostly talking about our CMS. The new CMS that we've been working on for the past two or so years has auto save and multilevel versioning. Which is really grit. We save a lot of metadata. We store data as JSON, which means we're very flexible to go to different platforms, we do a lot of user research to support the decisions that we're making. We've also had an open beta this entire time so that folks have been invited to be part of this process, the editors and writers have been part of this process and have had continuous documentation, training and communications to support all of these frequent releases. And I don't want to talk so much, so those are the big ones.

LIAM: That's great. I want to hear more about the user research, in particular. Yes?

AUDIENCE: I work at the daily beast and we just rolled out a new CMS and we built it in house. It's very, very simple and it works on mobile. The flip side is it's very, very simple and not very sophisticated for our bigger pieces.

LIAM: Anyone else love things about their CMS or is that all the love there is?

AUDIENCE: We're at NPR and yeah, we're excited about it. We're less excited that it's not done and there are still five other CMSes that we have either acquired or had failed migrations to, and we have no properties that -- literally almost all of them are on different CMS, and even the ones that are technically on WordPress are on different custom fields and you can't treat the data the same and [inaudible] sorry, sorry, I got distracted but the new CMS, yes, structured data.

PATTIE: Sorry, I missed where you're from.

LIAM: NPR.

AUDIENCE: Yeah, we're really excited about that. Daily losses mitigated as much as humanly possible or digitally possible.

LIAM: Is that like multiuser editing between newsrooms or --

AUDIENCE: Both. So we depend a lot on sharing content between our own public properties and the NPR part of it -- we import a lot of content from National Public Radio and yes, eventually we would like to have a real-time collaborative editing that we can support, so like all the frameworks we've chosen are -- that won't ship for probably a couple of years, but the idea is that when we get everything else done, that needs to cover sort of our base sort of table stakes. CMS has a platform that we can grow.

AUDIENCE: So one of the things I really like about our CMS is that it's a system, you know, it's decoupled, there's several different pieces to it. It's API-driven so our reporters can write one story and that goes out to the various different platforms. WBUR public radio in Boston. And I also had one of the things I didn't like that was decoupled, but it has its downfall, but generally it's a good thing.

LIAM: Any other pro-CMS folks?

AUDIENCE: So my personal site is built using a very strange bespoke PHP and markdown CMS. I like that it runs off markdown, that it's a bunch of files in a database and the whole site is centrally dynamically page loaded. It has strange templates that are not compatible with anything else, which are probably true with most CMSes, I can edit it from command line, but at the same time, I wish it had arbitrary metadata. I wish it had pages. I can insert whatever HTML I want, but there's also like no way to do that in markdown. I wish I had a media manager instead of me just uploading files at my site. I wish it had excerpts. And some days, I wish it had a database.

[laughter]

LIAM: But they when you make the database, you'd wish it didn't have a database.

AUDIENCE: Exactly.

LIAM: Anything else?

AUDIENCE: I mean I've used a basic WordPress so I'm kind of in an unusual circumstance, I'm not working for a company or anything like that, I'm sort of freelancing, I have tons I hate about my current website but it's user friendly and there's potential so it's not horribly bad.

LIAM: It's not horribly bad. That's the best we can do.

AUDIENCE: So I run a website Selaria Books and this is a part-time endeavor for those of you who run it. It's kind after love thing but we publish every day and I built it on a platform called web hook. It allowed me to do a lot of interface building and cool things, but they kind of end of lifed it, because of the people that worked on it, which had a little bit of funding went off to do other things. So they built it exactly right and I love it, but it's slowly dying, because all of the platforms that it was built upon are being upgraded and so it's slowly dying and I'm having to come up with a new solution.

AUDIENCE: What I like most about our CMS is image and promotional media management. There are some downsides to it but you don't see people on the website with the tops of their heads cut off for the most part and there's a lot of powerful tools for selecting the way of building an asset.

AUDIENCE: I'm also with Alley Interactive so we're an agency, not a publication, and other people have mentioned WordPress. Just to add one thing that I think is particularly compelling about WordPress is it is an open source platform. It has a really large developer community, and that means you have a lot of options. If you don't like your current developers or they leave or something happens, you can find out if people who, in theory, can take over and continue to work, because the open standard is known by a wide variety of people and there is a lot of community work that can be used by you and leveraged to accomplish certain things that you have to do from scratch, in exchange to which you ought to contribute, as well, but there's a lot of prior artwork out there that you can use.

AUDIENCE: I also work for a public radio station and what I like about our CMS is that we built it in house, so if there's something broken or if we need new features, then we can build it and because of this -- another thing is that it has very specific features that really kind of support the workflow of our specific newsroom in terms of like online web media and like audio and radio.

LIAM: And another thing about the in-house CMS that I'll bring up is one thing I love about our in-house CMS is that when a reporter has a problem they can just come up and ask us, rather than having [inaudible] coming up and I think related to that it helps them see the work that goes into this sort of thing. Is there any more pluses?

PATTIE: Who wants to talk about what they hate?

LIAM: I noticed a lot of people moved into what they hate already. Here we go.

AUDIENCE: I'd like corker Marie to come over and join the what we hate group. What we had done is dependence oy on our legacy API. We're still dependent on our kind of 10-year-old model of the grills app for displaying that data which can cause a lot of friction. I don't think our breaking news support is quite what it could be. Our permissions system is totally fucked, and we could probably handle video content better than we do.

AUDIENCE: Can I run up and add to that? So I'm the person who has done a lot of the communication with our editorial staff about like new features and all this process that we're doing and the first thing that I worked on is permissions. I think our asset management system could be better. I also think that one of the things that's hard for us to do right now that I hope we could do in a more robust way in the future is giving people a high-level view of what's happening on their site and making sure that they -- whether they're like in EIC or an individual contributor, you can see, like, this is what's in progress, this is about what's been published, I think we all have that dream of having that high-level view and right now that's like, here's a bunch of stories! Have fun! I hope that means something to you! So I'd like to see us do more of that.

LIAM: And it's interesting that working with analytics tools, we use parsing and similar things, but, yeah.

PATTIE: I have something I love. Will built this really cool tool apartment the daily news where it integrated -- like it wasn't analytics, it was like your own home row tracker, maybe you can talk about it. But it would show like the story count of the people who looked at the story overall and who did in the last hour and there was a way that you could queue stories on the first page so you could see something that was flowing up and get a better visualization. Which was really cool.

AUDIENCE: Yeah, I don't have much more than that, but part of the goal was to be able to track the trajectory of this story.

PATTIE: Yeah, and if not, what's the problem.

AUDIENCE: And what's the life cycle of a story.

LIAM: And I'm curious, what made -- since there are available tools for that, I mean, I guess you have to pay for them, so that might be one reason to do it all in house, but are there other advantages to integrating that straight CMS, rather than having the separate windows that showing different performance and --

AUDIENCE: Yeah, I think the biggest thing was switching context -- at this point it's really difficult to putting some sort of idea into why something's performing poorly, you think it's important that people are -- see that story, then you can [inaudible] but so having to go from the screen where you're thinking about the story and how it's framed and the decisions they're making in the way things are ranked and put it in a different spot. Rather than do a lot of content switching. Being efficient at it.

AUDIENCE: A WordPress thing and kind of the dark side to what you were saying earlier about hey, there's a huge developer community and WordPress is pretty easy to work with. And this isn't just for WordPress. It's super-easy to build something that works and then when you try to scale it, it doesn't. Or is like a horrible idea, even from -- maybe from a security standpoint or something. Like is it super-easy to build something out or to hire something out and you build something, and it does what you want it to, but maybe it doesn't do it at a level that you need it to scalewise.

LIAM: And you think that's a problem with WordPress in particular because there are so many people out there that write WordPress?

AUDIENCE: I only see it that way because I see a lot of WordPress code and solutions and the ubiquity of it makes it something that people build systems for it, but building something that scales that way, is not easy no matter what you're doing, honestly.

AUDIENCE: I'll add something else that was said about WordPress is that syndication is really painful in WordPress. Syndication and managing syndicated content and yeah, I've tried to help work on a plugin that's related to that and it's just really terrible.

PATTIE: What do you mean by syndication?

AUDIENCE: Syndication meaning so if you are a publisher with like 40 newspapers or a radio station that has 60 different stations and you want to syndicate a piece of content to, you know, your LA station to all the regional stations it's really hard to track what's been syndicated, how to push updates across all of them, you know, to send it over a draft status and they can publish it and tracking all that. It's just painful.

AUDIENCE: I feel like all the WordPress people are piling on WordPress here. There are many things I love about it.

AUDIENCE: I have lots of WordPress friends.

AUDIENCE: Yeah. I'm jealous at CMSes that store body content in a structured way. Lots of CMSes don't, including WordPress, but I know Vox's does and I think that's one cool thing about that.

AUDIENCE: The thing that I both love and hate about our CMS at the New York Times is that we use the same editing text for both print and digital which is great because we're not shuffling back and forth between two systems and dealing with the information loss that occurs. The down side it that it makes rolling out changes a little bit slower because you have to make sure you're not messing up publishing and print editions with the changes you make. The other thing I like about our CMS is the degree to which our CMS is really oriented for a production tool for like content producers where all the content came in from different places, the story was and the image assets were in a and the video came from a separate system and sort of designed to slam things together at the end of the process. As opposed to thinking about what are the tools if you're starting out to write a story, especially now with the wide array with formats that you use for text, is it video, audio, so forth, how do you actually structure a CMS and what's a great idea for content creators.

LIAM: That's another important question, is are you building for a producer or a creator from scratch?

AUDIENCE: The new CMS we're building because we have like a dozen sort of primary sites that are all decently different in their workflows and user, like authoring phases. Lowest common denominator is already starting to creep in again and it's kind of painful to watch what works really well for one group, really hamstring another one. You know, even starting from scratch and we're not there. I want us to be there. I hope we will be but we're just not even close to providing a great experience for everyone across the --

PATTIE: What do you mean by lowest common denominator experience?

THE COURT: I guess what to me lowest common denominator -- it's actually highest demon denominator, like some, you know, what marketplace needs versus what prairie home companion uses to actually name names, is very, very different. Marketplace has lots of shows, if you count in their flagship shows and the weekend and the morning report and all the other like small podcasts that they do, and you stitch all that together, and their needs for how to represent different shows together on one site with lots of different ways to get at the audio and the other storytelling around those shows, is so different from Prairie Home Companion, which is a show that focuses on a season and the episodes produced in that season and the episodes that get re-aired throughout the season. How you present that, it's just a very different set of needs, even hope at the base level they're both talking about shows and episodes.

PATTIE: So is what happens is you just provide a general experience that doesn't really give structure to Marketplace?

AUDIENCE: That's the challenge right now, is how do we not throw in a bunch of things that Prairie Home will find annoying, or friction, and also giving marketplace the editorial controls it needs, right? 

AUDIENCE: What I don't like about our content editor is that it's monolithic so it does a lot of things well but it creates a problem when we need to onboard developers and there's just so much code to look through and people are scared of making changes and we're currently in the middle of a site redesign, which is its own problem, because it shouldn't touch the CMS code, but it does. And part of that is also our data structure is very highly coupled to the CMS so if you just go into the database and look at the content, you have no idea what the structure is like, and I know eventually when there's a migration, there's going to be a lot of one-off scripts to rebuild an article or a story to the way that a reader expects it to be. And the last thing I don't like is I guess the part we didn't build is where you can see the editor very easily and it has its own very strong opinions about what kinds of content should go in there, and there's always a lot of struggle because it wants really well formed HTML. But I think it's ridiculous to expect reporters and editors to know how to do well formed HTML and if it's not well formed, it does weird things that look like bugs.

AUDIENCE: Can we all agree as a group that WYSIWYG editing is a blowup, no matter what you do or how you do it?

[laughter]

AUDIENCE: Something that I liked about the Bangor Daily News CMS is that it was very simplistic. It actually used Google docs, the barrier to entry was really, really low. Most people who came in had used Google docs before and training didn't really have to happen. One of the things I don't like about the CMS is it's all entirely custom. We're getting better about this, but there's still a ton of user experience patterns that we break people, in addition to learning, the organization and the workflow and the peculiar ways in which we write and edit things also have to learn the peculiar ways in which we have structured our CMS, a lot of which are not going to be immediately apparent to users, so I think that's a huge hurdle that we're giving to our users when they come.

LIAM: Some things that you wish your CMS could do?

AUDIENCE: I have a wish. So WordPress shipped a REST API in the core last year and that means every WordPress has a REST API, which is awesome. So I'm working with that, I began to wish that every CMS had an API in it, and what's more, that all of those APIs spoke in an interoperable kind of way. So I would love to be able to go to any content site and go to a certain end point that I've seen what it was, and get the right kind of structured data out. So maybe we could all agree one day on this.

LIAM: Like a certain end point or also a certain structure?

AUDIENCE: Yeah, like your domain/post/last week or whatever, and it would give me a predictable result.

LIAM: We're doing that right now, after the session.

[laughter]

AUDIENCE: I wish that any CMSes, WordPress or otherwise, would be better at mobile publishing, in the way that Twitter and Facebook are so great at mobile publishing. So ...

LIAM: Sure.

PATTIE: And a hand back there.

AUDIENCE: I wish that it were easier for us to help our editorial staff remix stories, you know, I think that we -- somebody gave a great talk yesterday about how there are all these platforms now but we're also in all of these social channels and some of our teams are doing really interesting things on you know, Instagram with stories, with galleries there. I think we're still doing some experiments on Snapchat, but all of that happens in a totally separate process, from, like, you writing out the story, and you know, publishing it on the site and that's really custom right now and I think there are some cool things that could happen if we were able to bring that into the CMS end of publishing product so that there was more collaboration happening across those teams. Kind of themes as a mechanism could be good. I don't know if this is a ma problem machines could solve for us, but I wonder if there was a way that we could see topics that people are interested in that we're not covering well, kind of helping service those gaps better and getting people to think about -- I think our teams are very intentional about it and -- it's not just about clicks but I think there is stuff that you miss that you don't know that you're missing. So yeah, I think those are two big things that I would like to see someday. Maybe that's five years out; I don't know.

LIAM: Yeah, that's another topic that we're going to get at, look at your taxonomies, and that sort of thing. What else do you want your CMS to do?

AUDIENCE: Imagine, a UI-less editor and a great WYSIWYG and it saves it in a beautiful structure that you can programmatically store and display to the user. Coming to you in five years!

[laughter]

AUDIENCE: This is kind of random, but on Marie's thing about kind of a CMS that tells you what to write about, timing. A few years ago, I think they just prototyped this, but built a system that looked at feeds of press releases that looked at Twitter, that looked at different sources to say like, people are talking about this, maybe you want to write about this, and would go so far, this freaked me out honestly to prepopulate a story with images and tags and you just have to fill in the title and the body. So do we want that? I don't know. I don't know if we want that!

[laughter]

AUDIENCE: One thing I'd like to see more of in the future is a content management system that helps the reporter-writer understand where the content went and its impact and a lot of times you publish and you go look at a chart and I, like, I have a very difficult time tying those two together. You know, the chart is usually independent of the content management system. Trying to tie that all back to like, why did I publish this? Where did it go? Who responded? Why did they react? Trying to connect, bring more personal connection to what you publish.

AUDIENCE: Five years from now, it would be really cool for a CMS to be really accessibility-conscious but not only in the way that it would be like, you know, translated, you know, into like screenreaders and things like that, but also into different languages, and even possibly into, you know, automated reading and, you know, ways that whatever method of media absorption you prefer, you could have that. I know that we already have like video transcription services that are automated, but just a lot more of that. Any more?

AUDIENCE: Kind of building off the accessibility thing, just being able to have different versions of a story, so you have English versions and Spanish version, but you could also have like the -- kind of like what Axios is doing, where you have a short and a long story. If you don't care about the minutia, you can just say oh, this is what's happened. If you want to read the longer version of the story, then you can read it if you want to. But maybe, you know, you charge extra for the longer version of the story.

AUDIENCE: Another cool thing could be like a CMS that's aware of like, just in time sort of notifications, so when you create a story, you could maybe, especially if it's a how-to story or something like that, you could geo tag the location, where if you're a reader, enter a certain location that story appeared from, because it was relevant at that point in time. Or you know, if a TV show was about to play in their time zone, so you could theoretically just put that information into your CMS and then the delivery system could figure it out.

LIAM: Was everyone at the breaking news talk yesterday where that came up? Cool. Any others?

AUDIENCE: Anyone think about wearables?

LIAM: Werewolves? That's what I heard.

AUDIENCE: Does your CMS understand werewolves?

PATTIE: Think about like where we were five years ago in like 2012, Obama was just elected for a second term, WordPress was still mostly a blog software. now I think more newspapers have been using it.

LIAM: Yeah, this topic is so interesting to us, because so often the technology industry is a fashion industry and there is some truth to that, that you don't want to get stuck on the wrong horse when you're switching.

PATTIE: Stuck on your own horse.

LIAM: Yeah, build your own horse. So that means ...

PATTIE: Well, thank you all for coming and thank you for sharing.

[applause]

AUDIENCE: Can I ask a question. Maybe I missed this at the beginning. Did we ask how many people are on homegrown? How many homegrown?

PATTIE: There's a lot of you.

AUDIENCE: What we got for WordPress?

PATTIE: I want to know from the people who are on homegrown grown CMS, how much has it evolved from like first commit to this point in time.

AUDIENCE: Unrecognizable.

AUDIENCE: Infinity.

AUDIENCE: Drupal users? Is that still a thing?

AUDIENCE: How many people here are creating CMSs? And how many people are.

PATTIE: Raise your hands for creating a CMS. Raise your hands for making a CMS you have better? And the rest of you are just living with it.

AUDIENCE: I mean people using CMS on a daily basis.

LIAM: Like in publishing? I'm also curious about I want to hear more from people who have been doing user research on their homegrown CMSes and their processes for that, because that's coming up for us.

[applause]
