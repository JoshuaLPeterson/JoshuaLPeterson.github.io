---
layout: post
title:  "GSoC - Calendar Pre Midterm"
date:   2014-06-23 11:06:38
categories: blog
---

Probably the most effective week of the project as I was taking desperate measures to pick up speed that lost in the past 2 weeks.

I spent the majority of the time this week reading about [scope](https://docs.angularjs.org/api/ng/type/$rootScope.Scope) and implementing $watch at various places in the Calendar.

As for enhancements, we now have :-

1. The various calendar views as in Arshaw FullCalendar are working with the ownClou calendar. The users can toggle between calendar daywise, weekly or month.
2. Reach to today's events from anywhere.
3. Removed the default fullcalendar buttons and synchronized the datepicker with the fullcalendar.
4. Implemented viewRender as in the master branch.
5. Bumped FullCalendar to the latest 2.0.1 and updated our changes to it.

Georg just updated the wiki for [Settings API](https://github.com/owncloud/calendar/wiki/Draft:-JSON-Settings-API) so I am busy writing controllers for the Settings. Post that, we will be working on the Subscriptions.

So, I am almost able to pick up the momentum I had lost last week due to satisfying my ego to fix one particular bug. Lets see, if we are able to get more stuff in the coming week.