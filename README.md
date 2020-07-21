# wagtail_disable_revisions
Looking to disable Revisions n Wagtail


When looking at using Wagtail for a future project one thing that has been mentioned as a down point is that our project doesn't need to have revisions.  

I raised this topic on Slack here -> https://wagtailcms.slack.com/archives/C81FGJR2S/p1595242243421800

Previously I'd tried to see if it could be limited through the Page class .  These attempts were. 

1. To unset the value of 'live_revisions' -  This doesn't do anything

2. To hack the function 'save_revisions'.  Still saves a revision but it'd be empty. 

Therefore it seems that it isn't as simple as using something in the Page class and I would need to extend the the PageRevision class. 

After giving it some thought this would seem like the best idea.  

1. A new App with a Admin point to select if you want to turn revisions off. 
2. Switches Revisions off. 
