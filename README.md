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

Indeed, the idea was to test - with the help of PyFunceble and Travis CI - hosts file, list of domains or even bocklist in order to have a list of active domains.

As [funilrys/dead-hosts](https://github.com/funilrys/dead-hosts) grew up it became impossible to have all those lists into one repository, that's why we use the GitHub organization system in order to create different repository for each list that has to be tested.

--------------------------------------------------------------------------------

# About PyFunceble

PyFunceble is A tool to check domains or IP availability by returning 3 possible [status](https://pyfunceble.readthedocs.io/en/dev/colomns.html#status): ACTIVE, INACTIVE or INVALID.

It also has been described by one of its most active user as:

> [An] excellent script for checking ACTIVE, INACTIVE and EXPIRED domain names.

If you need further informations about PyFunceble or Funceble please report to our [Wiki page](https://github.com/funilrys/PyFunceble/wiki) and/or if you don't find any answer feel free to create an issue into one of the [Dead Hosts](https://github.com/search?q=user%3Adead-hosts&type=Repositories&utf8=%E2%9C%93)'s or [Py-Funceble](https://github.com/search?utf8=%E2%9C%93&q=funceble+user%3Afunilrys&type=)'s repositories.

## About the status returned by PyFunceble

For an up to date version of this part please report to the [Status](https://pyfunceble.readthedocs.io/en/dev/colomns.html#status) section of our Wiki.

### ACTIVE

This status is returned when **one of the following cases** is met:

- We can extract the expiration date from `Lookup().whois()`.

  - _Please note that we don't check if the date is in the past._

- `Lookup().nslookup()` don't return `server can't find domain-name.me: NXDOMAIN`.

- `HTTPCode().get()` return one the following code `[100, 101, 200, 201, 202, 203, 204, 205, 206]`.

### INACTIVE

This status is returned when **all the following cases** are met:

- We can't extract the expiration date from `Lookup().whois()`.
- `Lookup().nslookup()` return `server can't find domain-name.me: NXDOMAIN`.

### INVALID

This status is returned when **the following case** is met:

- Domain extension has an invalid format or is unregistered in **[IANA](https://www.iana.org/domains/root/db) Root Zone Database**.

  - Understand by this that the extension **is not present into the `iana-domains-db.json` file**.
