---
layout: post
title: Astros Attendence since Minute Maid Park
---
## The Setup
I recently had a debate about true fans vs fair weather fans. Since I'm a Houston
Astros fan that lives way out in the desert of central New Mexico, where there is
no major professional sports, its crazy to me to see fans of all kinds here. "Why is
someone who was born and raised in central New Mexico a fan of the Cleveland Browns?"
is litterally a question I asked someone. Its interesting to see how devoted people
can be for a team that they don't ever see live. I was spoiled and I've see sports
on a professional level for Baseball (Astros), Football (Oilers and Texans), and
Baseketball (Rockets). This reminded me of how Bud Adams moved the Oilers to Tennessee
because he said the fan base wasn't strong enough in Houston. Granted, since the
return of the NFL to Houston with the Texans there hasn't been a non-sellout game.

So the following is looking is to look at the attendence and see if Houston Astros
fans are die hards or fair weather.  Do they still come out in droves when the 'Stros
are losing or do they run and hide when the team is losing?  Let's take a look at
what the data tells us.

## Stats 145
I'm currently taking a Stats class at the
[University of New Mexico - Valencia](https://valencia.unm.edu/) from Nicklos Lucas and
its a great class.  This isn't for a grade, but perhaps I'll get a bit of extra
credit for using what I've learned in class in real life. Let's look to see if there
is a real correlation between Attendence and Games back.

### Null Hypothesis
We expect there to be no real relationship between the average attendence
per year for Houston Astros fans and the amount of games back at the end of the year.
Any non-zero sample correlation is assumed to be soley due to random error/chance.

### Explination of the code
First we'll load all the attendence into the Pandas Dataframe, then look at the basic
descriptive statistics. It shows that out of the 1,452 games played at Minute Maid
Park the average game had a around 30,500 fans. That's not too shabby seeing that
the park sits about 41,000. Which puts the average at about 75% of capacity.

{% include Houston_Astros_fans.html %}

### Conclusion
*Since r(18) = +.65, p < .05; Reject Null Hypothesis.*

It appears that as the Games Back increases, there is a decrease in the average attendence
per year by Houston Astros fans. The obtained sample correlation (r = +.65) is not soley
due to random error/chance.


I hope that now afte we've won a World Series that the Astros fan base can stay strong no
matter the standings. Then again, perhaps this is not something that is just a Houston
thing. I wonder if this is a MLB wide correlation or perhaps its just a sports correlation.
I might have to add that analysis to my "To Do" list.

-dave.
