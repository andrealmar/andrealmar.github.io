---
title: "SRE/DevOps skills that companies want"
description: SRE/DevOps skills that companies want
header: SRE/DevOps skills that companies want
---

What skills do companies really want when they are looking for DevOps / SRE professionals? I've analysed 50 job postings to tell you what companies want when they are hiring for DevOps and SRE (Site Reliability Engineer) positions.

_P.S - In this post, I am going to treat DevOps and Site Reliability Engineering as the SAME thing._

Most of the time companies don't really know what they want and they just go with the flow. Meaning: "if Google invents a new term (SRE) and says that an SRE must do this, this and that, this probably should be a good thing and my company need this kind of person. So let's open a position, call it SRE and put the same requirements everybody is asking for."

Let me explain how I did this experiment:

I've searched for the job positions on these sites:

- LinkedIn
- Company website
- Random Google search (just typing the position name)

The way it works is:

I've read the entire job description and its requirements. I took notes on which requirement regarding the position was mentioned most.

For example:

If a job posting says it requires Python programming OR Java OR Go I will give one point for each mention.

If another job posting only says Python as a requirement I'll give one point for the Python mention leaving Python with 2 points (2 mentions), Go with 1 point (1 mention) and Java with 1 point (1 mention). Very simple huh?

You got the point. 1 mention, 1 point.

I separated the requirements in some subjects :

- PROGRAMMING LANGUAGES
- AUTOMATION
- CLOUD
- CONTAINERIZATION
- MONITORING
- LOGGING
- CI / CD (Continuous Integration / Continuous Deployment)
- OPERATING SYSTEM(S)

Here are the results:

## Programming Languages

![](/img/sre_devops_programming_lang.png "SRE/DevOps Programming Languages")

We can see that on this subject there is a BIG winner: **Python**.
Since Python is a multi purpose language and it’s very easy to read I’m not surprised it is the number one choice for companies that want their DevOps / SRE future employees to know. Linux comes with Python out-of-the-box and it’s much more fun to write scripts in Python than it is in Shell Script. Although, notice that Shell Script is still kinda relevant for these positions. So it’s better to know a bit. There is a lot of legacy scripts written in Shell Script and you for sure will give maintenance in one of those during your SRE / DevOps career.
If I were an Infrastructure Engineer or Technical Support guy/gal wanting to go the DevOps / SRE way I would start to learn Python ASAP.
Another interesting thing is the rise of Go as a language for DevOps / SRE purposes. Docker was written in Go and the language has a focus for what is called systems programming. We should expect Go rising more and more on the DevOps / SRE space. Better keep an eye on it…

## Cloud

![](/img/sre_devops_cloud.png "SRE/DevOps Cloud")

Another _BIG_ winner here: **Amazon AWS** ecosystem.
A lot of companies run their services on AWS and they want people capable of dealing with that. So better learn the AWS ecosystem as well. It’s the top pick for companies that run their systems on the cloud.

## Automation

![](/img/sre_devops_automation.png "SRE/DevOps Automation")

Regarding automation, IMHO any tool you learn will be good. There are different tools for automation but most of them do the same type of job. The winner in this case is **Ansible** followed closely by Puppet.

## Containerization

![](/img/sre_devops_containerization.png "SRE/DevOps Containerization")

Another major winner(s) here. The duo **Docker + Kubernetes** is always mentioned on the skills requirements that companies want for a DevOps / SRE role.
It’s almost like container is a synonym of Docker. And of course, you need something to manage your myriad of containers. Here it comes Kubernetes to help you with that.

## CI / CD — Continuous Integration / Continuous Deployment

![](/img/sre_devops_ci_cd.png "SRE/DevOps CI/CD")

Continuing with the big winners here is another one: **Jenkins**
When it comes to CI / CD this is THE guy. It’s the leading Open Source automation server and provides hundreds of plugins to support building, deploying and automating any project. I prefer to use GitLab CI solution but the good thing is that on CI/CD space you have a bunch of options to choose.

## Monitoring

![](/img/sre_devops_monitoring.png "SRE/DevOps Monitoring")

On the monitoring field, I was a little bit surprised on **Nagios** becoming the most requested tool. But I didn’t work with Nagios for a long time so maybe I was expecting a new player to stand out. Maybe this new player is New Relic or Datadog. My conclusion is: if you become proficient in one of those monitoring tools you will be good to go and apply for any DevOps / SRE job. If the company uses another tool you should be able to learn faster because they are very similar.

## Logging

![](/img/sre_devops_logging.png "SRE/DevOps Logging")

Not many job descriptions mention logging tools. Those who mention points out **Splunk** or **ELK (ElasticSearch, Logstash, Kibana)**. I think if you choose either one you will be well served.

## Databases

It was very interesting to discover that most of the companies don’t really specify which database you have to know. Some of them (very few) point out to **PostgreSQL** or **MySQL** when talking about relational databases and some of them point out to **MongoDB** when they are talking about NoSQL databases.

## Operating Systems

No graph here because the choice is _ALMOST_ unanimous. **Linux** is THE operating system you must know. And not in a superficial way. Most of the jobs demand that you know deep system (Linux) internals. So push yourself beyond the simple commands. Learn how to use Linux tools like _tcpdump, netstat, iptables, uptime, dmesg, perf, ss, strace_ and so on…

## Other (Generic) Skills

I decided to call it “generic” because they don’t fit in any of the categories above. It doesn’t mean they are dispensable. No way. They are a MUST have.

Distributed Systems
- Microservices
- Concurrency
- Multi-threading
- Large scale storage systems
- Caching and its tools like Memcache, Varnish, Redis

You need to have all of those concepts above inside your brain. You will use them daily.

## Conclusion

This may be a very simple research but it shows (at least for me) a pattern when companies want to hire some DevOps / SRE. I decided to do this to help me focus on which technologies I must learn in order to improve my DevOps / SRE skills. It’s very easy to lose focus when you are trying to learn something. There is a LOT of information on the internet and people telling you to do this or do that. You can get so saturated with so much information and be paralysed. Occasionally I struggle with that. Please be careful. Analysis Paralysis is a very bad “disease”. If you want to follow these same patterns and learn what companies are demanding to feel free to do that. I hope this simple research help you to move on and choose what is best for you to learn or start learning.
