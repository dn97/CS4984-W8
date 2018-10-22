# Project 8 - Pentesting Live Targets

Time spent: **3** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: SQL Injection (SQLi)
We can see that the single-quotes aren't being sanitized causing an database query failure. Double single-quotes work fine because we're closing our own query and making it blank
![](https://github.com/dn97/CS4984-W8/blob/master/blue_sqli.gif)
Vulnerability #2: Session Hijacking/Fixation 
We can change the php_session id from another browser and change ours so that we're able to access the main admin page
![](https://github.com/dn97/CS4984-W8/blob/master/blue_session.gif)


## Green

Vulnerability #1: Cross-Site Scripting (XSS)
Feedback form allows for XSS and we can cause a pop-up to appear to the admin that checks the feedback
![](https://github.com/dn97/CS4984-W8/blob/master/green_xss.gif)
Vulnerability #2: Username Enumeration
Upon logging in with an invalid password for a correct username, the error is returned bold but an incorrect username results in a non bold error
![](https://github.com/dn97/CS4984-W8/blob/master/green_user.gif)

## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR)
The ID values can be changed to look at the non-viewable persons linked on the PUBLIC 'Find a Salespersons' page
![](https://github.com/dn97/CS4984-W8/blob/master/red_idor.gif)

Vulnerability #2: Cross-Site Request Forgery (CSRF)
The red site doesn't validate the CSRF token while the other site do
![](https://github.com/dn97/CS4984-W8/blob/master/red_csrf.gif)


## Notes
The 
Describe any challenges encountered while doing the work
