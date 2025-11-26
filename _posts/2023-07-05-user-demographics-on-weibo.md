---
title: Who uses Weibo?
author: Ole Hexel
date: 2023-07-05
---

This post accompanies our recent publication: "Demographic inequalities in
digital spaces in China: The case of Weibo" (open access:
https://doi.org/10.36190/2023.01).

> Qian, Wenqing, Ole Hexel, Emilio Zagheni, Ridhi Kashyap, and Ingmar Weber.
“Demographic Inequalities in Digital Spaces in China: The Case of Weibo.” In
Workshop Proceedings of the 17th International AAAI Conference on Web and Social
Media. Palo Alto, CA: Association for the Advancement of Artificial
Intelligence, 2023. https://doi.org/10.36190/2023.01.

## The Short Version

Weibo is the largest micro-blogging service in the world. This was true even
before recent changes at Twitter. For different reasons, we thought it would be
helpful to know more about the age, sex, and place of residence of its user 
population. We queried Weibo to know what they themselves thought were the 
counts of users in different locations according to age and sex and we matched
this information with socio-economic data on the same locations. This paper
describes what we found. 

The very short summary is that the greatest contingent of Weibo users are young
(15-29) women (in urban areas). Most of Weibo's users live in heavily urbanized
areas. The share of the population using Weibo varies between 0 and 20% of a
prefecture's population. It is higher in more urbanized, more educated, and more
prosperous areas. There are few users above 40.

The code to produce the results and figures in our paper can be found here:

The data underlying the article is not currently available. During the course of
this project, China has introduced new rules regarding the transfer of data
outside of the country (see, for example, [this summary](https://www.whitecase.com/insight-alert/new-requirements-outbound-data-transfers-china)).
This is not limited to businesses but also concerns academic resources, like the
CNKI database
([FT](https://www.ft.com/content/93051bff-5af8-4841-8e1f-8c9ab0cbd3fe),
[VoA](https://www.voanews.com/a/china-to-limit-access-to-largest-academic-database-/7029581.html)).
We would like to make our data available as soon as possible, but we are waiting
for clarification of the current rules.

## The Not-so-short Version
If you've made it this far, than you're interested in more than a very short
summary, so allow me to start again, with more detail.

### Why and how

Despite recurrent debates around the positive or negative effects of social
media, we (English-speaking European or Five Eyes researchers/residents) know
little about the users of platforms other than the usual suspects
Facebook/Twitter/LinkedIn/... There are some good and some not-so-good reasons
for this. Luckily, there is more and more research on populations residing
outside of this handful of countries and how they use social media and on social
media platforms that do not belong to the small group above (see, for example:
). China is a particular and particularly interesting case, because of the
combination of a large population, widespread mobile phone/internet use, and
strong domestic social media platforms.

Weibo may be the biggest micro-blogging platform in the world (and in China),
but it is not the biggest Chinese social media platform. First place belongs to
Wechat, a sort of everything platform (messenger, blogging, news, payments) that
is incredibly popular. Weibo is fairly comparable to Twitter: it is mostly
text-based, although you can share media and you can follow other users or
"topics" which are a mix of hashtags and subreddits. Our reasons for picking
Weibo were: it is a meaningful addition to our collective knowledge about social
media platforms and user populations, it is big, and it is accessible.

We collected user counts via Weibo advertisement platform. On this platform, 
Weibo reports user counts according to configurable criteria, like age, sex,
location, web or mobile phone access, mobile phone OS, and many more. Varying
these characteristics in a systematic and exhaustive way gives us an aggregate
view of the user population. We (partially) automated this and you can find the
Python script in our code package.

We also collected publicly available information on the locations in which users
where located. The reporting of public statistics becomes quite heterogeneous
below the provincial level ([Wikipedia on China's administrative hierarchy](https://en.wikipedia.org/wiki/Administrative_divisions_of_China)). We
settled on collecting data at the prefecture level, because this gave us a good
chance of having comparable and near-complete data. Wenqing put in many hours
and much effort in tracking down information from different national and 
regional statistical offices. 

### What
As mentioned above, the largest group among Weibo users are young women (15-29
years). Most of Weibo's users also live in areas that are highly urbanized
(share of subunits that are "urban" according to the national statistical
office) and where the resident population is on average more educated (mean
years of schooling) and has higher income (mean disposable household income per
capita).

The predominance of women of Weibo is quite striking: there are close to two
women per one man among all users; the ratio declines from ~5:1 for user 15-19
to around 2:1 for users 25-29. The reverse is true in the general population (though
not in the same proportions): there are more men than women (103:100), especially
among the <30-year olds (110:100). On other social media platforms, it is most
often men who are overrepresented. The magnitude of the skew is also notable, at
least for a "generalist" social media platform. More niche platforms like Douyu
(or Twitch) or Xiaohongshu (or Pinterest) have even more extreme imbalances.

Of course, you may ask "why?" Why do some people use Weibo and others don't? In
some places but not others? At some ages but not others? Differently by sex?
Why is there such a gender difference? or fewer people use Weibo in different
locations or age groups? We looked at a variety of socio-economic indicators.
Because we do not have individual-level data, these are ecological correlations!
Unsurprisingly, use of Weibo is more widespread in more urbanized areas with
more educated populations and higher GDP/capita and mean income/capita. More
interestingly, women are overrepresented to the same degree regardless of how
urbanized, educated, or prosperous a prefecture is.


### So what?

There are plenty of opportunities to dig deeper. 

First, prefecture populations range from 90 thousand to 26 million. Weibo data is available at the district level too. But data on education, income, etc. at this level are reported only incompletely and inconsistently. Collecting and opening up complete and harmonized socio-economic data at the district level would be a great contribution to the research community in and of itself.

Second, we only scratched the surface in exploring socio-economic correlations. Education is worth looking into: it seems to have a higher slope than more "material" factors, esp. above 9y of mean education (=duration of compulsory education). Contrasting "collective" factors, e.g. GDP/capita, with "individual" factors, e.g. mean income/capita, could also be interesting. Given high levels of mobile phone ownership and good cellular network coverage, individual economic barriers to access seem unlikely but more "infrastructural" factors may make network effects more or less potent.

Lastly, we take Weibo user counts at face value and we look at ecological correlations. Checking the validity of user counts using other methods than audience estimates and checking for ecological fallacies.

Education could be important because Weibo is a mostly text-based platform (in contrast to e.g. Douyin/TikTok). If one looks at the slope below and above a mean of 9 years of schooling, it is flat before and steep after. Yes, 9 years is the duration of compulsory education. If you find some neat variation in schooling policies and implementation (e.g. during the 2000s push), it might help untangle the age-period-cohort patterns of Weibo use.
