---
title: Dialogflow + Dashbot at Intuit Hackathon
date: 2017-11-13T14:30:00.385Z
---
What innovations can we come up with that help small businesses save time or money? That was what Intuit's Small Business Hackathon was trying to solve. So our team, which consisted of three other developers I met there, looked internally and saw a common problem when working with smaller businesses: documentation.

Small technical companies lack the manpower or data to create the perfect documentation for their customers. Developer-written documentation, which is most common for startups, usually turn out horrible because the developers understand their product too well. They are unable to strip away the inadvertent assumptions an internal developer can make and take the user’s point of view. Our team believes integrating a chatbot into the documentation process can bridge developers writing the documentation and the users that navigate it.

A documentation chatbot powered by actionable analytics is what we needed to create in 24 hours. We used DialogFlow and a custom webhook to build a natural and rich conversational experiences. Next, we integrated our DialogFlow chatbot with Dashbot, a platform that provides actionable bot analytics. Dashbot became the center of our solution because of the data we were able to extract from it. Data such as conversational flow and top intents highlight how users are interacting with our documentation. In the example below, our bot served a lot more customers with the intent of using our Slack documentation instead of Facebook. In addition, users hit the found_bug intent 11 times. By setting up an intent that recognizes when user is talking about a bug in the documentation process, we can take action and fix it.

<img src="/img/blog/dashbot.png" width="100" height="100">

So how do we fix it? Dashbot, staying true to their motto of 'actionable analytics', has a nifty feature called intent funnel. Intent funnel, in the photo below, shows us what was the interaction prior and after the intent was triggered. In the example below, we see that 11 users triggered the found_bug intent in our chatbot when the chatbot serves a piece of documentation about accessing an API key. Thus, giving small businesses the chance to fix that piece of information in their documentation and improve their customers' experience. Last little feature we found to be awesome for small businesses is the alert function. Alert can send a webhook, email, or text whenever an event is triggered. So we setup a email alert whenever our found_bug intent was triggered, giving us instant data when a customer needs help.

<img src="/img/blog/intent-funnel.png" width="100" height="100">

We call our solution DocuBot. Serving customers easy-to-use documentation and providing companies data to improve on their documentation. We see this sort of documentation chatbot applicable to non-technical companies as well. Ikea, for example, can see where customers are struggling when following their manuals. Then, they can take action and improve on specific parts of the manual where a this_photo_doesnt_tell_me_anything_and_all_the_screws_look_the_same intent is triggered.

If you want to understand the custom DialogFlow webhook, feel free to check out [DocuBot Github](https://github.com/kc657/DocumentationDashbot). We hosted our webhook function on Firebase. I'll write an post that dives deeper into creating a chatbot with intents, entities, and webhooks since it deserves its own post. And did we win and take home $5000? Sadly we didn't win. But it was awesome to see 31 teams work on solutions to help small businesses. Huge shout out to Intuit, Google, Dashbot, and my awesome teammates for making this amazing weekend possible.

<img src="/img/blog/team.jpeg" width="100" height="100">
