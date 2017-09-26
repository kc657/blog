---
title: React.js with IBM Watson
date: 2017-09-25T22:48:54.385Z
---
#### I am proud to present [Articulat.in](https://articulatin.herokuapp.com)! Here is the story behind this application:

For my final project at General Assembly’s developer bootcamp, I decided to create an ambitious application that merged IBM Watson capabilities with React functionality. I mentioned in my previous [blog post](https://kevinchen.netlify.com/post/first/) that I attended a few IBM meetups/hackathon. Having learned a lot in these events, a big goal for the final project was to demonstrate my ability to merge skills and technology I learned on my own with in-class material. The vessel to deliver my goal was an app that analyzed text differential of a written transcript and a user's voice recording. By doing so, algorithms could provide insight on how well the user memorized the original transcript prior to a big presentation.

The first challenge was to teach myself the ins and outs of Watson's [Speech-to-Text](https://www.ibm.com/watson/services/speech-to-text/) service. I built the first feasibility test using without React.js to avoid wrestling two things at once. By doing so, I spent a lot less thing debugging and got the API to translate user speech into text within a day. I then moved and refactored this functionality into a React.js component. By doing so, the component could be reused in future projects if I built it out correctly. This is a huge benefit of React.js components. For example, I reused and refactored the Sign In and Sign Up components from a previous group project because we took the time to make sure it was reusable and self-contained. The biggest issue when porting the code into React.js was difficulity dealing with the [watson-developer-cloud](https://www.npmjs.com/package/watson-developer-cloud) pacakge. Thus, I took some time to explore concise [watson-speech](https://www.npmjs.com/package/watson-speech) package that resolved my microphone stream issue. With that solved, I overcame my first challenge and my project had it's first core functionality!





Example 1: 
```
  this.setState({voiceInput: //
```






