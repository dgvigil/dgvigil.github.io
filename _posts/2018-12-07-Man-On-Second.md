---
layout: post
title: Hitting with a man on second
---
## What to do?

I grew up in a baseball family. Baseball was (and is) a huge deal in my family.
My brother is a private instructor and baseball coach even. He's also the one that
got me a ticket to game 5 of the 2017 World Series. It was epic. I told my 
brother about having a wealth of data, but not exactly sure what questions
to ask it. So he gave me a few interesting ideas. Here is the first:

# Which is the best pitch and count to hit when there is a runner on 2nd base?

## The Setup

I have a mysql database filled with a ton of information on my laptop. I started 
with a query to pull all pitches that resulted with a hit where the ball was hit
into play and there wasn't an out. We don't care if you just make contact, but 
they need to put it into play and make it to base safely.  From 2010 to the end 
of 2018 I found over 180,000 hits with men on second base. Let's take a look at
what we got.

{% include man_on_second.html %}

## Conclusion
So it would appear that you need to swing early at fastballs. This seems 
pretty consistant over the past 9 seasons as well. Get the bat off
your shoulder before the pitch has time to mess with you! Haha. 
