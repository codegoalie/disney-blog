+++
title = "Introducing DVC Reverse Search"
description = "Find potential upgrades using your existing points"
date = 2021-01-05T05:59:07-05:00
categories = ["DVC"]
tags = ["announcement", "products"]
draft = true
type = "post"
image = "/images/dvc-search-announcement/mockup.png"
author = "Chris Marshall"
+++

Tired of scouring the points charts and creating complicated spreadsheets trying
to figure out where to stay and how many points your next DVC stay will cost?
Want to branch out to new resorts but don't think you can afford them? Would
borrowing a few points get you into an upgraded room type?

<!--more-->

I'm happy to formally announce the launch of our latest product the [__DVC
Reverse Points Search__](https://dvcsearch.lineleader.io?utm_source=announcement-blog-post)!
Quickly and easily find hidden room upgrades for your next stay using your
existing points. Simply enter the number of points you have and the expected dates of
your stay to instantly see the list of ___all___ rooms across all DVC properties. You can find
booking opportunities for larger rooms or longer stays using all of your
existing points.

### {{<underline-link text="Try it now!" href="https://dvcsearch.lineleader.io?utm_source=announcement-blog-post" >}}  
Or read on to find out more.

The sheer volume of resorts, "point seasons" and weekday vs weekend point
amounts in DVC is just staggering. On the one hand, it creates a great value
and variety for owners. You can stay in new resorts and new room types with
each trip. On the other hand, it creates a massive planning task. I knew there
must be a better way.

We purchased our DVC contract in November 2019. At the time, we already had a
non-DVC trip booked for May 2020 (I know, I know). While purchasing, they were
able to refund the cash reservation and rebook with points at the same resort
(Polynesian) and similar view. So, trip #1 (or what I thought was going to be
trip #1) was all sorted.

As any respectable Disney addict would do, I immediately started thinking about
our *next* trip. It felt like a whole new world had opened up to us: new
resorts, new room types. So many possibilities. But I also felt like I had no
idea how even to approach planning a DVC trip. I had so many questions. Are
there best times to use my points? Are there room types that aren't worth the
points? Are there great values hidden in the point charts that only a seasoned
DVC member would know about? I couldn't possibly memorize all the points
charts. I started using a spreadsheet, but found tweaking my options really
cumbersome. I'd look up some dates at certain resorts, but then adding a day or
shifting back a week required me to re-look up the point chart. It was all
pretty labor intensive.

I knew I had my annual allotment of points and I knew near about some dates
that we'd be able to go, but I didn't have an easy way to see what was
available to me or to quickly make changes and see what my new options were.

Enter the [__DVC Reverse Points
Search__](https://dvcsearch.lineleader.io?utm_source=announcement-blog-post).

I'm a software engineer by day so I could build the exact thing I needed. There
were a few challenges to overcome to get the tool I wanted to use. First, I
needed to pull the info from the PDF point charts into a database. Then, query
that data by points and dates. Lastly, display the results in a useful and
compelling way.

Getting the raw data out of the point chart PDFs took a few steps. I could have
simply manually entered all the data. But, what fun is that? In the end, I ran
a text extractor over the PDFs and got text files with the contents of the
PDFs. This included all the text including the legal notices and the formatting
wasn't great. I did some light formatting on the text files, then was able to
write a custom parser to pull the data and insert it into a database. Further,
I can do these same steps in the future to add new point charts each year
fairly easily.

Next, I created the website for me (us) to input point amounts and dates. The
front-end sends the requests to a simple API server which queries the database
and returns the results. These results are then displayed in the cards on the
website.

Overall, I'm pretty happy with the end result. I'm also open to making
enhancements and improvements. Feel free to comment below or send me an email
with your thoughts.

Thanks for checking out LineLeader and our reverse points search. Here's to
finding our best *Welcome Homes*!

-------

Cover image courtesy of [ShotSnapp](https://shotsnapp.com)
