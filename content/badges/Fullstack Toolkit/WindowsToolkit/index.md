---
title: "Fullstack Setup On A Windows Machine"
date: 2019-11-18T23:53:00+01:00
draft: false
hideLastModified: false
summary: "A list and setup instruction for common fullstack tools and installs for Windows based machines"
summaryImage: "images/0-Live_v3.png"
tags: ["Windows", "Toolkit"]
pinned: true
weight: 5
series: "notfeatured"
---

November 2020

# Background

Each of the three most common operating system flavors macOs, Windows, and Linux will install technologies differently. While macOs and Linux share some common methods, Windows, in general, will have it own flavor. This post includes common fullstack tools with brief overviews and the steps for install on Windows machines (and only Windows machines). 

# Prerequisites

-A Windows Machine (with admin privledges )


##### <span style="color:red">Disclaimer:<span>

You will be installing software as administrator so things can go wrong. While this is not expected, please have backups of your life and your machine before going crazy here. Sometimes things with software/hardware can and will go wrong.


## Step 1: Chocolatey For Package Management

There are many places you can buy a domain, the web address for your website. Namecheap has worked well for us and the namecheap platform allows use to reference our domain names where we need to.  Domain are priced annually. You can generally find affordable domains and have your own domain is an excellent investment in yourself. Also, you will have the rights of your domain name moving forward as long as you choose to renew your domain name each year.

Log-in, or create account at  [namecheap.com](https://www.namecheap.com/) to search for and buy domain name you would like to use for your website. Ideally this would be something like "yourname.com".


#### Pricing Hints

Domain pricing is yearly cost is based on how common the words are in your domain search. More words are more valuable and will be priced higher. With some creativity you can often get the pricing down to $12 or less.

For example, "howdyitsjenny,com" might be available and inexpensive in cases where  "www.jennysmith.com" is not available or or is priced > $12

Another example: fullstackjimmy" might help you here if  "jimmyandre.com" is already taken or has a high price tag
 
<center>{{< imageToClick imagePath = "./images/namecheap.png" Capition = "Name Cheap Name Search"  width ="50%">}}</center>


## Step 2: Getting Git Setup

If you don't have a github account you will need one. You can sign up for free https://github.com/.

Github is the technology platform but you also need to install git, the technoloyg, on your personal machine.

https://git-scm.com/book/en/v2/Getting-Started-Installing-Git/

## Step 3: Install Hugo

https://gohugo.io/getting-started/installing/

## Step 2: Create Your Personal Website


Start by retrieving our fullstack-portfolio-refresh theme.

**Step 1:** Go to fullstackproblemsolvers.com and get to the fullstack-portfolio-refresh Github repo

**Step 2:** Follow the directions in the Readme

**Step 3:** Go back to your command line and do a:


{{< code language="term" >}}
$ sudo bash -c 'echo 0 > /proc/sys/kernel/randomize_va_space'
{{< /code >}}


```
git add -A
```
4. Then do a:
```
git commit -m “Initial commit of personal website for [Insert your website name]”
```
5. Go to Github
6. Create a new repository
7. The repository name should be the same as what you named it on your local computer
8. Leave all the initialization options as default, and Click “create repository”
9. Use the “push an existing repository directions”
10. Now go to Netlify
11. Log-in or create account and then log in
12. New site from Git
13. Click on the Github tab
14. Enter your github login info to connect netlify with your github account
15. Select your new repository you just created
16. For the build command put in hugo
17. For publish directory put in public
18. Click on Advanced
19. In the key put hugo_version
20. In the value put 0.58.3
21. Click on Deploy Site
22. Once the production deploys status changes to Published, move on to the next step
23. Now lets setup your custom domain
24. Click on add a custom domain
25. Type in the domain name you purchased from namecheap
26. Click on verify
27. Click on the options click setup Netlify DNS
28. Click continue
29. Take the IP addresses provide and go back to namecheap
30. Under my account  and click on manage domain
31. Under name servers change to CUstom DNS
32. Add the IP address (provided by Netlify) one by one
33. Then go back to Nelify and click Done
34. Allow 24 hours to complete step 3 of securing your site with  HTTPS

And just like that you now have your personal website!

Now the last step to earning your personal website badge is to complete the Website Inspiration post that you we had you pre-load when you created your website. This post can be as detailed or broad as you want it to be, it just needs to talk about why you created your website. 

Once you complete the final step feel free to _____(NOT SURE WHAT TO PUT HERE????)

Congrats! You have officially earned your Personal Website Badge!

