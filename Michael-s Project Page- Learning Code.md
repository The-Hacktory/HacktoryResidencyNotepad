# Michael's Project Page: Learning Code

[lee t](/ep/profile/wVl2KVvy64z) [georgia@thehacktory.org](/ep/profile/xNudWl91SoT)

Lee and Georgia, 

I want to get moving on learning the soundwalk code. Is the best way to get started on this by diving into the Processing tutorials?

Also, I own the code that I had Punk Ave write. Should I get that from them? It was written in iOS, so I'm not sure what I would need to even read it. Can you advise?

And, just so you are both aware, I am out of town essentially the first two weeks of July. I might also have to go to The Walker sometime during the last two weeks of July.

This pad text is synchronized as you type, so that everyone viewing this page sees the same text.  This allows you to collaborate seamlessly on documents!

Hi Michael (Mike?)

I think yes you should get the code from Punk Ave, but I wonder how they might share it with you? Lee might have more insight into this than I do. If they share a code repository on GitHub with you, I think that would be a good move, or you could set up your repository and have them drop it in. I'm not as familiar with GitHub, but we can go over this next week.

As for learning the soundwalk code... I'm going to give a bit of a long-winded answer, and then get input from Lee or one of our other teachers about the best course for you. I think you might want to figure out if you want to continue making the soundwalks for Iphones only, or if you want to make it available for Android. I also know that you can make apps for the Iphone (and I think Android) using [OpenFrameworks](http://openframeworks.cc/) . OpenFrameworks is a little more robust than Processing, has a great community and forums, and may give you more tools to work with in the future. However, Processing is a good way to learn the basics of programming and see results quickly. If you're itching to start, Processing is good, and as I said, with more input from Lee or one or two of our teachers I think we can find a good language/framework (OpenFrameworks, or something else) for you soon.

Sounds great. I answer to Michael or Mike...I use Michael for my "professional work" because I think it looks and sounds better. I'll touch base with Punk Ave and see what they say about how to share it. I'm going through the processing tutorials, but they all seem to be about visuals. Just wondering if there is a more applicable place to start. I want my work to be available on as many platforms as possible, not just iOS.

Hey Mike, I'd highly recommend learning processing first because it will help you learn how to learn other programming languages. it's a good first programming language - probably the best for artists and musicians.  It's true it's not used for sound as much, but your learning there is still applicable to C++ (OpenFrameworks is built in C++ and is compatible with C++) and openFrameworks has a huge art/sound community built around it.  Punk Ave can transfer the code to you via disk or online. likely they wrote your code in Objective C or some variant.-lee

**Things to Watch and Do**

*   Do an introduction to code [here ](http://code.org/learn)using Angry Birds.  Click on the one with Mark Zuckerberg's head on it. Get bored by this tutorial? Stop and proceed to next step.
*   Do the 1-hour [tutorial](http://hello.processing.org/) of learning to program in Processing! This is my favorite coding tutorial ever!
*   Show and Tell! Take a screenshot of something you've created in Processing (even during the tutorial). How to take a screenshot? Press Command + Shift + 3 and then release all keys. It will save the file to your desktop. Add that image to your project page on hackpad. Copy and paste your code for that image below the screenshot.

![](https://hackpad-attachments.s3.amazonaws.com/hackpad.com_KJ4Jcdsi0qX_p.188777_1403117865604_Screen Shot 2014-06-18 at 2.55.41 PM.png)

Code for above image. I know I could do the small circles with an array, but can't remember how.

float circleX;

float circleY;

float peacock1;

void setup() {

  size (1400, 800);

  background (#67177E);

}

void draw() {

  circleX = random(width);

  circleY = random(height);

  peacock1 = random(200);

  println("hey");

  circleX = circleX + random(-2, 2);

  peacock1 = peacock1 + .1;

  circleY = circleY - 1;

  fill(0, circleX, circleY);

  stroke(200, peacock1, 50);

  ellipse (circleX, 180, 24, 24);

  rect(circleY, circleX, circleX, circleX);

  fill(255, circleX, circleY);

  ellipse(peacock1, circleX, circleY, 200);

  fill(peacock1, circleX, circleY);

  ellipse(200, 200, 10, 10);

  ellipse(400, 400, 10, 10);

  ellipse(300, 300, 10, 10);

  ellipse(500, 500, 10, 10);

  ellipse(600, 600, 10, 10);

}

void mousePressed() {

  background (240, 40, 180);

}

*   OPTIONAL: 40 minute [video](http://vimeo.com/45851523) of a talk by Casey Reas (one of the inventors of Processing) talking about making art with code and chance operations. It's sort of a talk about the artistic lineage to creating an artist's programming language.

**Questions To Ponder**

*   Was this easy/hard?

easy-ish. I mostly used existing code, so I feel like I didn't really made anything, just remixed it.

*   What was the point of the Angry Birds code tutorial?

To show that there is a way to simplify coding in a way that everyone can understand.

*   Were you surprised by how quickly you made something in Processing?

yes

*   What do you like about coding in Processing?  How it gets me thinking about new possibilites.

What do you find difficult? Remembering syntax for certain functions.

*   **Make a list of questions and/or things you want to learn!**

*   How to use sound files with Processing. Minim? 
*   How to make Processing do what I want it to do. Right now I am making random things happen.
*   Better understanding of variables, if-then statements, arrays

**NEW GOALS**

*   Learn objective c, at least check it out

*   Blog post to Lee by next week

*   [](http://fo.am/bicrophonic-research-institute/)http://fo.am/bicrophonic-research-institute/ check out this GPS tech used in a bike ride.

[](http://sound-art-text.com/post/89104827083/bonns-sound-art-treasure-hunt)http://sound-art-text.com/post/89104827083/bonns-sound-art-treasure-hunt Interested in GPS usage not related to a phone or personal device. Very interested to learn more about this.

**UPDATE July 21:**

I have finished "Getting Started with Processing" by Reas and Fry. Such a good way to learn it. I have since successfully altered the Many Doorbells code to include an array, and am altering it to make it more beautiful. Right now I am stuck on adding my own sound to the sketch. I'm getting an error with minim that I don't understand yet. Hopefully have that solved soon.

Very encouraged when [lee t](/ep/profile/wVl2KVvy64z) pointed out that getting a sketch to realize that a mouse is inside an ellipse and have that cause a sound to trigger is essentially the same as getting a program to realize that a person is standing at a certain location. The way that code plays with scale in that way is very new to my brain, and has me thinking differently about everything.

Today is day 1 at The Walker with Faye Driscoll. While sitting on the plane on the way out here she mentioned she is interested in exploring hand held instruments that light up. If she had said that to me a month ago I would have told her she needed someone else. But now I actually think that is something I could make eventually. Arduino here I come.

That's awesome Mike! So glad to hear it, yeah I think you are closer than you think to building something like that!

I wanted to follow up on your question to Robert Spahr on Monday about cultivating an audience. I thought your question was great, but I don't think Robert is the person to have good insight into it. No offense to him but he's up for tenure, so I don't think he's thinking about how to make a living by creating things or experiences his audience might buy. I think his answer bore that out.

I wanted to point out an article that is relevant, in case you haven't heard of it, called "1000 true fans"

[](http://kk.org/thetechnium/2008/03/1000-true-fans/)http://kk.org/thetechnium/2008/03/1000-true-fans/

It talks about a model for content producers like artists to think of the feasible size of an audience they could cultivate of "true fans." True fans would buy ever single thing you create as an artist, they would drive 200 miles to see you perform, they have a google alert set to your name, etc. If you created content they consistently spent ~$100/year from, then the article is arguing this could come up to a decent salary for an artist of $100,000 (though costs are not included in that).

This article builds on the concept of the "long tail" which has become popular in entrepreneurship/startup lingo recently:

[](http://www.longtail.com/about.html)http://www.longtail.com/about.html

The long tail describes a graph of popularity on the x-axis, and products on the y-axis. This concept argues that our culture and markets are moving away from selling just a few "hits" which would be all the way on the left at high popularity, and moving towards selling smaller quantities of niche products more consistently. 

I should add that further study didn't yield many artists actually doing this successfully:

[](http://kk.org/thetechnium/2008/04/the-case-agains/)http://kk.org/thetechnium/2008/04/the-case-agains/

But there's another blog that is tracking artists who say they are doing it (I think this is a more recent trend too).

[](http://cyberprmusic.com/category/blog/1000-true-fans/)http://cyberprmusic.com/category/blog/1000-true-fans/

And then there's the trend of youtube stars becoming quite successful

[](http://harvardpolitics.com/covers/rise-youtube-star/)http://harvardpolitics.com/covers/rise-youtube-star/

These concepts and trends are interesting to me as they are informing how I think about how to make The Hacktory sustainable to some degree. I'd be very interested in finding ways among our group to talk about distribution models that we could try, or ways to cultivate the audiences of all of you artists, if there's an interest. I think this topic is pretty advanced for where we are at right now in the residency, but down the road I could definitely set up some workshops or speakers, so let me know if you're interested!

Thanks Georgia, yes, I'm kind of obsessed with making something sustainable. This membership model idea was proposed to me by Brian McTear who runs Weathervane Music. They have been growing a pretty substantial membership base over the last several years, and he is asking me what my version of that would look like. Again, I get held up on the fact that a membership service needs to provide a steady stream of content to offer to it's base, which is why this idea of self generating art is appealing to me. I already don't have enough time to make the things I want to make, and my output seems to be slowing down as of late (mostly to me learning a whole bunch of new skills). Here are some questions that I am asking myself:

Does a membership model have to be related to content? Can it be related to a community of like minded individuals? How can you give these individuals agency over something run/curated by someone else (myself)? Can this become a new kind of art form?

I will check out the links you sent. The youtube phenomenon really speaks to what I am trying to get at. That is content based on content, so the hardest part of the generative process (the writing of a song that connects with a large group of people) is already accomplished. This isn't a kind of form I am interested in, and I think contributes to the homogenization of music. It propels the idea that things that sound like things we have heard before are good.

And yes, while Rob and his work are truly inspiring, he is not thinking from the POV of a starving artist. It was clear to me that he works in academia before you mentioned it to me. If there is something I would love to talk to him about, it would be to humbly point out that he is not considering his audience, or how his work is consumed (or rather, that this is not embedded in his work). I would be interested to see what he would make if he considered a context for his work before he conceptualized the meat of it. He's interested in stirring the pot in a great way, but doesn't seem concerned with HOW someone is made aware of that.

I echo all the sentiments you have above.

In terms of getting paying fans, check out [Patreon](http://www.patreon.com/). I was really skeptical of it at first but it seems to really work for some people. Essentially, you get your fans to commit to paying a certain amount each month or (more often) for each "release" however you define that. For example, some musicians release music . Some game designers release a game.  Etc etc. Each time they post, they collect a donation from everyone that's committed.  Each of their backers choose they amount individually that they are comfortable contributing. And they can set a maximum amount to support. This seems to be generating some real income for some of the DIY videogame artists that i know, and some writers. Would be interested in seeing how this could work for musician/composers, and for further iterations of this website concept to be built.

Woah, Patreon kind of made me sick to my stomach. It is butting up against that issue I have where it seems like it is propelling mostly cover songs and other forms of regurgitation of existing content. This does not seem like a good model for someone who's goal as an artist is anything other than connecting with the most people possible. While I would love for there to be a huge audience for my work, it centers around finding new ways for people to hear and experience music, which has an inevitable learning curve built into it on the part of the audience. I guess my hope is that that learning curve gives audience a way to stay with my career, and follow it through exposure to new things. Not watch me do something millions of other musicians can do. Perhaps Patreon is a model for this, but just looking at the home page, I don't want to relate my work to that dribble that is up there at all. Does that make sense? Am I just being difficult? Sometimes I wonder....

Also, had a pretty good beginning conversation with Rob about letting how people will experience the work be an early process concern, with the goal of having that experience influence the content. Ended up talking about both soundwalks, and how I believe the conceptual ideas around it changed what I wrote, and influenced the whole into a cohesive experience of content and context.

I love this conversation and the issues we're touching on!

In response to your questions about membership and content Mike, in my view the answer is a qualified yes. I think what members would pay for in supporting an artist is content, but I don't think it has to be as polished as you think. Content in that case could be just basic insight into your point of view as an artist. 

There's a saying on the internet that "content is king." Apparently Bill Gates first presented this idea, that the future of the internet and the PC revolution was the opportunity for personal publishing.

I like the spin that "Conversation is king," from the writer Cory Doctorow:

[](http://blog.maestroconference.com/tag/cory-doctorow/)http://blog.maestroconference.com/tag/cory-doctorow/

The book _Here Comes Everybody_ that delves into this idea is great, I highly recommend it.

For example, your thoughts on Patreon - that's content! The access you give your supporters to thoughts like that and how you manage that access to make them feel special and an "insider" and the invitation to engage with you is what members could pay for. This kind of content creation may involve a larger ego; which is something I struggle with myself, but a lot of people are making this work. 

Putting stuff out there on instagram, a blog, twitter, etc, is a way to build your point of view or values and conversation with followers, and that can lead to other opportunities. For someone like me it would most likely be speaking opportunities, or invitations to participate on projects. For someone like you I imagine it could involve those things, but also performing opportunities, or the option to release/sell polished content to your members directly.

I also like the idea about having a community generate content that is curated. Sometime in the future if enough people affiliated with The Hacktory were making content or objects and sharing them that would be awesome. For now, I think just giving people access to our plans, opinions and decisions counts.

A kind of open source model for creating artistic content is another idea. I have a vague understanding of what Weathervane is doing, and I know they are making it work, but I'm not sure if that's similar to what I'm talking about.

You may also be interested in one other essay from the early days of the internet and open source: The Cathedral and the Bazaar, which explains why open source works better for building things and problem-solving.

[](http://www.catb.org/esr/writings/cathedral-bazaar/cathedral-bazaar/)http://www.catb.org/esr/writings/cathedral-bazaar/cathedral-bazaar/

BOOM! Weathervane in a nutshell:

[](http://www.philly.com/philly/entertainment/TEDxPhiladelphia_Your_content_is_worthless_Brian_McTear.html)http://www.philly.com/philly/entertainment/TEDxPhiladelphia_Your_content_is_worthless_Brian_McTear.html

This is the problem I have with Brian's thinking...he says your content is worthless, but he would not have a community without it.

As a separate thought....How can I create more and more content when i don't have enough time or resources to do the things I already want to do? This membership model seems like ANOTHER full time job, when I already have three. This is why I'm interested in the self generative stuff...

**<u>August:</u>**

Wil Lindsay seems to be my mentor/advisor. I am learning Corona, an SDK which uses Lua as its coding language. This week I am taking care of a bunch of registration points that need to happen. Wil is asking me to put together a schedule/timeline for the rest of the res. [lee t](/ep/profile/wVl2KVvy64z) would you be able to help me with that? Either tonight of Thursday.

**<u>Sept. Update:</u>**

I made an app! It's on my phone! you touch stuff and it plays sounds! I'm very pumped. Show you all tomorrow. (Damn, that rabbit hole was deep)

_-mike, that sounds awesome. can't wait to see it.-lee_

**October Update:**

Just used this code to retrieve my longitude and latitude for sitting at a desk at DM+D. Used and if/else that if those numbers are true, play a sound, and it worked. Will look into looping and fading audio and changing locations next. Found some code for how to register location as per a defined time increment as well.

display.setStatusBar( display.HiddenStatusBar )--hides status bar

--load sounds into table

soundTable = {

mySound1 = audio.loadSound( "dingdong1.aif" ),

mySound2 = audio.loadSound( "dingdong2.aif" ),

mySound3 = audio.loadSound( "dingdong3.aif" ),

mySound4 = audio.loadSound( "dingdong4.aif" ),

mySound5 = audio.loadSound( "dingdong5.aif" ),

}

--finds users location

local myMap = native.newMapView( 0, 0, 320, 480 )

myMap.x = display.contentCenterX

myMap.y = display.contentCenterY

local locationTable  = myMap:getUserLocation()

local locationtxt = display.newText( "My location is: ", 100, 100, native.systemFont, 16 )

if ( locationTable.errorCode ) then

    locationtxt.text = locationtxt.text .. locationTable.errorMessage

else

    locationtxt.text = locationtxt.text .. locationTable.latitude .. ", " ..locationTable.longitude

end

--if/else statement to play sound at specific location

if locationTable.latitude == 37 and locationTable.longitude == -122 then

        audio.play( soundTable ["mySound1"] )

end--]]

**<u>FINAL PROJECT/NEW THOUGHTS</u>**

I found this GUI called TSPS (Toolkit for Sensing People in Spaces) [](http://www.tsps.cc/)http://www.tsps.cc/   that easily sends data to Processing. It allows you to interface with video input from a camera (I'm using a Kinect, but you can use your webcam) and detect people's position in space. I would like to use this to locate people inside of given coordinates to trigger a sound for two pieces:

The first will be a dance piece between two people wearing bluetooth speakers, turning them into movable sound sources. I'd like to have a grid with 10 sections that they can stand in to trigger sounds. Not sure what the content would be, but would be musical or noise based.

The second piece would be to remap my old house inside of the gallery in some way, and trigger Simon talking about each room as you enter it. This would be a headphone piece. 

I still would like to make a soundwalk, but am finding the area around Crane Arts to be pretty uninspiring for that piece...Going to go there on Monday or Tuesday and see if I get inspired.

*   Figure out how TSPS send OSC data to Processing so that I can call it.

-Mike, you will have a lot of people in the gallery, as well as images on other moving screens. Make sure you test whether those other people/screens won't accidentally trigger TSPS.

*   Learn how to trigger a sound based on a persons location from TSPS in Processing