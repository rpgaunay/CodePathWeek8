# CodePathWeek8 - Globitek Assignment
# Ryan Gaunay - CSC 143V - Hofstra
# Mirror 1 - https://35.184.88.154/
# Time Spent: 5 hours

# Objective: Identify vulnerabilities in 3 different versions of the Globitek site.

# Blue Target

1) SQL Injection (SQLi)
* Could not get.

2) Session Hijacking Attack
* In Firefox, I logged into the blue site using our pperson logon. After logging on, I
went to the change_session_id php file and copied the session ID. I then opened a
different browser and navigated to the site. I opened up the change_session_id php
file in this browser and changed the session ID to that of the logged in browser. This
successfully authenticates me without needing to log in, as seen in the GIF.

# Green Target

1) Enumeration Attack
* Could not get.

2) Stored XSS Attack
* As an admin on this site, you have the ability to view user submitted feedback. On
this site, the large text field for feedback is unsanitized, so users can submit harmful
XSS that will affect admins upon viewing. By inputting "<script>alert("Ryan found
the XSS!");</script>", I can log in as the admin and this popup will occur in the
feedback section. Unfortunately, it seems someone else in this course wrote a
script to reroute to Youtube so my popup is not seen (shown in GIF).

# Red Target

1) IDOR Attack
* When you click "Find a salesperson" you are shown a list of people to contact. Upon
clicking one of them, you can see the ID field in the URL. By testing different numbers
you can try to access IDs that are not accessible through the salesperson page. I tried
1-9, and eventually reached 10 where you reach a non-public salesperson.

2) CSRF Attack
* Could not get.