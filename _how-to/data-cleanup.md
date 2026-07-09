---
title: "Clean up intermediate data"
author: keiran_rowell
---

## 🧹 Please clean up!

Once your job has finished you can safely `Clear Intermediate Results` :)
This saves a _massive_ amount of space, 
{: .notice--success}

### Data Cleanup Tool

CryoSPARC has a very good `Data Cleanup Tool`. **Please use it.** Your storage admins (and your own allocation) will thank you!
![Data Cleanup Tool]({{ site.url }}{{ site.baseurl }}/assets/images/data-cleanup-tool.png)

Lots of polished datasets that went through multiple cycles only the first input and the last output in their history: the intermediate data steps in the middle can be re-built simply by `Restart`ing the job. 

Cryo-microscopy particles are _incredibly_ data intensive. While Discworld doesn't hold your data at all, things load faster onto Discworld when your data is slimmer.
Cryo-EM data is one of the largest users of analytical data storage on campus, so you're lowering the Uni's burden by using the `Data Cleanup Tool`. 
{: .notice--warning}

### Data Cleanup Guide

Structa Bio Inc. (the company behind CryoSPARC) have a good guide about data management. Please follow it here: [Guide---Data Cleanup](https://guide.cryosparc.com/setup-configuration-and-management/software-system-guides/guide-data-cleanup-v4.3)
