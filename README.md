# Awesome Bug Bounty Tips [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
A curated list of amazingly bug bounty tips from security researchers around the world.

## Why?
It is hard to look for Bug Bounty Tips from different social media websites. This repo helps to keep all these scattered tips at one place.

## Contents
- [Website](#website)
- [Mobile](#mobile)
- [Tools](#tools)
- [Others](#others)

### Website

> Look for GitLab instances on targets or belonging to the target. When you stumble across the GitLab login panel (/users/sign_in), navigate to `/explore`. Once you get in, use the search function to find passwords, keys, etc. - [@EdOverflow](https://twitter.com/EdOverflow/status/986214497965740032)

> If you have found an authenticated stored XSS vulnerability that requires specific permissions to exploit — say administrator-level access — always check to see if the POST request that transmitts the payload is vulnerable to CSRF or an IDOR. This will increase the impact, since as an attacker you no longer need an account with certain permissions to exploit the issue. - [@EdOverflow](https://twitter.com/EdOverflow/)

> If you are in heroku, try calling /app/Procfile to get the installation instructions that a dev had when deploying to heroku. If that loads and you know what stack it uses, you should be able to find the source code of the app in /app directory. For example if it is rails, you can pull routes.rb by calling /app/config/routes.rb. The app folder is the main directory where all deployed code is stored. - [@uraniumhacker](https://twitter.com/uraniumhacker/status/1105681791958966272)

> most java web apps allow bypassing common LFI filtering rules by doing the following: http://domain.tld/page.jsp?include=..;/..;/sensitive.txt - [@zer0pwn](https://twitter.com/zer0pwn/status/1093365823106965504)

> If you find jsp page with no parameters. You can actually add path parameters using semicolon. Like this example.com/test.jsp;');alert(1)// & perform XSS. Apache tomcat support this. - [@akshukatkar](https://twitter.com/akshukatkar/status/1074744556036382720)

> When you have a SSRF vulnerability on a Google Cloud server, the fastest way to grab all internal metadata is this "All in one" payload: http://metadata.google.internal/computeMetadata/v1beta1/?recursive=true - [@adrien_jeanneau](https://twitter.com/adrien_jeanneau/status/1062460475387076608)

> Always do printenv to see if your inside a container when you have a RCE you can escalate it further if you break outside the container. - [@Random_Robbie](https://twitter.com/Random_Robbie/status/1057185407367086080)

### Mobile

> Struggling with SSL Pinning or root detection on Android or iOS? Use [Objection] (https://github.com/sensepost/objection) to easily bypass them. - [@skeltavik](https://twitter.com/intigriti/status/1075749882462433280)

> Dont just statically analyze apps. Dynamic analysis is where I find 90% of my mobile bugs. Look at old and new versions of apps. Sometimes you can derive API keys from the older apps that still work! - [@nullenc0de](https://twitter.com/nullenc0de/status/1061636754757861377)

### Tools

> Use commoncrawl for finding subdomains and endpoints. Sometimes you find endpoints that can't directly be visited from the UI but has been indexed from other sites. **curl -sX GET "http://index.commoncrawl.org/CC-MAIN-2018-22-index?url=*.$1&output=json" | jq -r .url | sort -u** - [@streaak](https://twitter.com/streaak/status/1015236009993203712)

> Add to scope all your target subdomains on @Burp_Suite "Target" tab >> "Scope" >> "Use advanced scope control" checkbox >> "Add" button >> Set Protocol: Any - Host/IP range: .*\.domain\.com$ >> Enjoy! - [@_gonzacabrera](https://twitter.com/_gonzacabrera/status/1105340391514099712)

> Threatcrowd is able to list domains registered by a specific email address: https://www.threatcrowd.org/email.php?email=domain@teslamotors.com Very handy for open-scope. - [MrTuxracer](https://twitter.com/MrTuxracer/status/1103913275786354689)

> Need to bypass a firewall? Use securitytrails.com to find the originating server IP. (https://github.com/vincentcox/bypass-firewalls-by-DNS-history) - [@vincentcox_be](https://twitter.com/intigriti/status/1073184104630378501)

> You can enumerate directories in some buckets with Wfuzz. Rule for Wfuzz: http(s)://<bucket-address-here>/FUZZ/ Successful: 200 Status code without content - [@Wh11teW0lf](https://twitter.com/Wh11teW0lf/status/1096009061206761473)

> Want to find some internal code of companies or some sample codes of new features? Checkout with: site:repl.it intext:<companydomain>. In companydomain, if you know the internal domain it is even better. [@uraniumhacker](https://twitter.com/uraniumhacker/status/1061992982847533059)

> To find vulnerable domains and subdomains that is currently pointed to GitHub due to misconfiguration. Try searching the following syntax on publicwww. "There isn't a Github Pages site here". It will return thousands of pages containing domains and subdomains that could be vulnerable to Subdomain Takeover. - [@ajdumanhug](

### Others

> Look for hackathon-related assets. Companies sometimes run hackathons and give attendees special access to certain API endpoints or temporary credentials. I have found GIT repositories that were set up for hackathons full of sensitive information. - [@EdOverflow](https://twitter.com/EdOverflow/status/986316960303591424)

> If you submit a report and want the triage team to quickly triage your report, include your test credenetials in the report. This is especially useful if user permissions and roles are involved. - [@EdOverflow](https://twitter.com/EdOverflow/)

> Do not just inspect source code, check GIT logs for information too. Here are some simple tricks that you can add to your reconnaissance workflow: https://gist.github.com/EdOverflow/a9aad69a690d97a8da20cd4194ca6596 - [@EdOverflow](https://twitter.com/EdOverflow/status/986991389178253318)

> Look for hackathon-related assets. Companies sometimes run hackathons and give attendees special access to certain API endpoints or temporary credentials. I have found GIT repositories that were set up for hackathons full of sensitive information. - [@EdOverflow](https://twitter.com/EdOverflow/status/986316960303591424)

> As a hacker you will come across many different pieces of software that you haven’t used before. It often pays off to take the time to install / use it to 1) create a sandbox to test particular scenarios and 2) understand the software better to find more vulns faster. - [@jobertabma](https://twitter.com/jobertabma/status/1039771086370598912)

> Always check an e-mail's headers and body. They often contain valuable information and endpoints! - [@honoki](https://twitter.com/intigriti/status/1103705724826411009)

> If a bounty target offers premium features, buy them and test the new endpoints. Most of the times, it's worth the investment! - [@vdeschutter](https://twitter.com/intigriti/status/1088471152148787200)

> Follow the marketing guys (e.g., Director or Manager) of the product you're targeting for #BugBounty. These guys are awesome in telling you all the new features that are in pipeline or just released. You will be the first to get your hands dirty. - [@soaj1664ashar](https://twitter.com/soaj1664ashar/status/1085118841359872000)

> Did you know that the character '_' acts like the regex character '.' in SQL queries. https://www.w3resource.com/sql/wildcards-like-operator/wildcards-underscore.php - [@gwendallecoguic](https://twitter.com/gwendallecoguic/status/1076081365777551364)

> If a website does not verify email, try signing up with <whatev>@domain.com (the company email). Sometimes this gives you higher privilege like deleting/viewing any other user's profiles etc. [@uraniumhacker](https://twitter.com/uraniumhacker/status/1066483686655221761)
  
