# RPI Ambulance's Slack integrations
There are a number of integrations included in this Node.js file, intended to ease logistics and information-sharing of RPI Ambulance members. Read on to find out more.

## AmIResponding?

This integration was the origin on this entire project. AIR [IamResponding](https://iamresponding.com/v3/Pages/Default.aspx)-type functionality for free and within a Slack team. It utilizes Slack's [bot users API](https://api.slack.com/bot-users) to post an [interactive message](https://api.slack.com/interactive-messages) when a call is dispatched.

This interactive message posts some information about the call and queries channel members if they're responding or not. It the posts for the channel to see each person's status.

Here's how a dispatch looks in Slack—with a few people who responded to the call:
<img src="https://i.imgur.com/qAL5Szl.pnghttps://i.imgur.com/qAL5Szl.png" width="400">

---

## `/whoson` slash command
This integration provides the RPI Ambulance crew schedule for:
* The current crew, between 1800 and 0600 hours
* The previous night's crew and tonight's crew, between 0600 and 0900 hours
* Tonight's crew, between 0900 and 1800 hours

These differences provide a logical and grammatically accurate description of the status of night crews. The time between 0600 and 0900 hours was specifically selected because that crew will often still respond to emergency calls—even after their "shift" ended.

___

## RPI*Alert*
The RPI*ALert* system provides audible, SMS, and email notifications to the RPI campus during high-priority, critical, rapidly changing events. Several systems have been set up to work with RPI*Alert*, including [Concerto Emergency](https://github.com/concerto-addons/concerto_emergency), most of which utilize RPI*Alert*'s public RSS feed.

This Slack integration uses the RSS feed, as well, and forwards the alert to everybody on the #alerts channel, a specific channel intended to never be muted.


---

### Credits

#### Developers
* [Dan Bruce](http://github.com/ddbruce)
* [David Sparkman](http://github.com/David-Sparky)

#### License
RPIA's Slack integrations are licensed under the MIT license.
