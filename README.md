# About Facebook-Zero-Hosts-Block_git_kowith337

[![Build Status](https://travis-ci.org/dead-hosts/Facebook-Zero-Hosts-Block_git_kowith337.svg?branch=master)](https://travis-ci.org/dead-hosts/Facebook-Zero-Hosts-Block_git_kowith337)

```
# [uMatrix 1.3.15.100]
# Title: Facebook Zero Hosts Block
# Author: kowith337
# Homepage: https://github.com/kowith337/PersonalFilterListCollection/tree/master/hosts
# Issues: https://github.com/kowith337/PersonalFilterListCollection/labels/Hosts%20File
# Credits: https://github.com/random-robbie/bugbounty-scans/raw/master/facebook.com/urls.txt
#        : https://github.com/CHEF-KOCH/CKs-FilterList/raw/master/HOSTS/CK's-Facebook-HOSTS-FilterList.txt

# Note: This aim to block non-formal hosts that serve all Facebook contents and resources from alternative "Free Basics" servers
#       that it happen when you're using on mobile data over the carrier that collaborate with Facebook to have THAT service!
#       Currently, all of big 3 carriers in my country are give up to Facebook to let it invade and interrupt usage experience.
#       I'm against to this services because it's show various of annoyance that likely Facebook trying to force me and all of
#       users to use THAT service, include showing balloon party cover, inject purple bar above, or even to prevent any videos
#       to play on mobile data, even many users in my country are use the unlimited data (but limited speed) plan!
#       Also...
#           MOST ANNOYING THAT IT REDIRECT TO "h.facebook.com" WITH "NON-HTTPS" CONNECTIONS! THIS POSSIBLY TO OPEN THE GATE FOR
#                                 MOBILE DATA PROVIDER AND FACEBOOK ITSELF TO KNOW THAT USERS USE OR CONNECT TO FACEBOOK WITH
#                                 THEIR NETWORKS, THEN THROW THE ZUCKESTIONS TO USE THAT SERVICES ABOVE, THE REDIRECT IS STILL IN
#                                 EFFECT, EITHER USERS DIDN'T REGISTERED FOR OR NOT INTENT TO OR DOESN'T WANT TO USE THAT SERVICE!
#           MOST ANNOYING THAT IT PREVENT ACCESSING "facebook.com" OR "www.facebook.com" AS THE PROPER WAY OF DESKTOP SITE.
#                                 INSTEAD, IT WILL REDIRECT TO "web.facebook.com" WITH UNCLEAR REASON ABOUT ANY RECOMMENDATIONS
#                                 FOR LANDING TO OTHER SUBDOMAIN!!
#           MOST ANNOYING THAT IT PREVENT ACCESSING "mbasic.facebook.com" OR "touch.facebook.com" IF FACEBOOK DETECTED THAT USERS
#                                 ARE USING MOBILE BROWSER, AND WILL TRY TO REDIRECT ALMOST EVERYTHING TO "mobile.facebook.com"
#                                 INSTEAD!!!
#       I will keep block those connections, no matter that it will break the functionality to using Facebook on mobile data plan
#       until they abandone this service and return all connections to the original favor, no redirects, no non-HTTPS, no nagging
#       or forcing to use that service, just let it should be normal like I'm using Facebook at home or via Proxy/VPN!

# Note 2: All rules below aren't check with any tools, I just duped and don't know how many "Free Basics" servers are existed?
```

--------------------------------------------------------------------------------

# About Dead-hosts

[Dead-Hosts](https://github.com/dead-hosts) is the replacement of the original idea behind [funilrys/dead-hosts](https://github.com/funilrys/dead-hosts).
Indeed, the idea was to test - with the help of PyFunceble and Travis CI - hosts file, list of domains or even bocklist to have a list of only active domains or IP.

Today, we provide our infrastructure for anybody who want it. [Just ask](https://github.com/dead-hosts/dev-center/issues/new?template=inclusion-request.md)!

--------------------------------------------------------------------------------

# About PyFunceble

PyFunceble is the tool that our infrastructure use to get the status (ACTIVE, INVALID, INACTIVE) of a given domain or IPv4.

Please find more information about it there:

* http://pyfunceble.github.io
* http://pyfunceble.readthedocs.io
* https://github.com/funilrys/PyFunceble

