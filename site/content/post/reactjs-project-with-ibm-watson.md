---
title: React.js with IBM Watson
date: 2017-09-25T22:48:54.385Z
---
#### I am proud to present [Articulat.in](https://articulatin.herokuapp.com)! Here is the story behind this application:
<br/><br/>


For my final project at General Assembly’s developer bootcamp, I decided to create an ambitious application that merged IBM Watson capabilities with React functionality. I mentioned in my previous [blog post](https://kevinchen.netlify.com/post/first/) that I attended a few IBM meetups/hackathon. Having learned a lot in these events, a big goal for the final project was to demonstrate my ability to merge skills and technology I learned on my own with in-class material. The vessel to deliver my goal was an app that analyzed text differential of a written transcript and a user's voice recording. By doing so, algorithms could provide insight on how well the user memorized the original transcript prior to a big presentation.

The first challenge was to teach myself the ins and outs of Watson's [Speech-to-Text](https://www.ibm.com/watson/services/speech-to-text/) service. I built the first feasibility test using without React.js to avoid wrestling two things at once. By doing so, I spent a lot less thing debugging and got the API to translate user speech into text within a day. I then moved and refactored this functionality into a React.js component. By doing so, the component could be reused in future projects if I built it out correctly. This is a huge benefit of thoughtful components. For example, I reused and refactored the Sign In and Sign Up components from a previous group project because we took the time to make sure it was reusable and self-contained. The biggest issue when porting the code into React.js was difficulty dealing with the [watson-developer-cloud](https://www.npmjs.com/package/watson-developer-cloud) package. Thus, I took some time to explore concise [watson-speech](https://www.npmjs.com/package/watson-speech) package that resolved my microphone stream issue. With that solved, I overcame my first challenge and my project had it's first core functionality!


The second challenge I encountered was to create an algorithm that scored the differential of a written transcript and a user's voice recording. I found that data comparison was far more complicated than I had anticipated. There was a popular JavaScript text differencing implementation package called [jsdiff](https://github.com/kpdecker/jsdiff). However, I wanted a real challenge and promised I would only use this package if I failed come up with my own algorithms. After some research, I knew that a big chunk of my scoring would be to solve the longest common subsequence (LCS) problem so I took a deep dive into LCS. Here is a picture of my late night whiteboarding at school:

![whiteboarding-lcs](/img/blog/lcsproblem1.JPG)

The result of all this was an algorithm that did not work consistently as I was not too familiar with JavaScript matrix. After some searching, I found a great example from [Rosetta Code](http://rosettacode.org/wiki/Longest_common_subsequence#JavaScript) that helped me down the right path:

```
  let s,i,j,m,n,		
    lcs=[],row=[],c=[],		
    left,diag,latch;
```
While I did not overcome this challenge alone, I still learned a lot more about data comparison than I would have if I used the jsdiff package. The scoring turned out to be fairly accurate and gave my project the last function it needed!

I learned a lot in this project but I realized there are still a lot of problems such as the longest common substring algorithm in place. I will continue to refactor my code in attempt to make the scoring more accurate for the users. If anyone has any input or suggestions, I would be happy to hear about it! Thank you for reading about my final project experience.

Front-end Github Repository: [Click Here](https://github.com/kc657/Articulatin-Frontend) 
<br/><br/>
Back-end Github Repository:  [Click Here](https://github.com/kc657/Articulatin-Server)

