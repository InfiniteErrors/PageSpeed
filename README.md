## Website Performance Optimization portfolio project
This is my submission for the Performance Optimization project. So far it's been a great way to really dig into how a page runs javascript and some things developers have to watch out for.

### Getting started

#### Part 1: Optimize PageSpeed Insights score for index.html

My strategy with index.html was basically to follow all the pagespeed insights and then really try to get those images compressed as far as possible.
Also inlining the CSS proved to be very helpful for mobile users which made sense considering how small of a file it really was. My page speed score ended up being 96 on mobile and 97 on desktop. Not too shabby!

#### Part 2: Optimize Frames per Second in pizza.html

I must admit I was out of my javascript depth on this file. But after reading through come of the source material provided. My basic strategy was just to look for logic that was being repeated unnecessarily and try to simplify it. Also there was functions that were doing things like creating 100 pizza animations on the page at once. When really we should be accounting for the window size instead. I tried using "innerWidth" for the longest time and then realized that was silly. InnerHeight rounded up each time makes for a far better solution.

The resizepizza function saw a big update and simplification. It was doing all of these crazy calculations inside of loops that never needed to be done in the first place. That function now simply changes the css width style of each pizza picture on the page to a new percentage.

The update positions functions was the tough one. Seeing as this was my first time dealing with animation frames. This article from Paul Lewis was my guide. Thanks Paul! In a nutshell, this technique allows the browser to choose when the optimal time to bring up a new frame.
 https://www.html5rocks.com/en/tutorials/speed/animations/


 Note - I will be VERY happy to never look at this UGLY pizza site ever again haha! ;) Sorry Cam.

 #### Need help getting this page running?

Follow this [link](https://infiniteerrors.github.io/PageSpeed/) and browse away.
