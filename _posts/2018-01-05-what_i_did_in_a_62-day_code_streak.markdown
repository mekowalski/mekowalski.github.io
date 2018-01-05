---
layout: post
title:      "What I did in a 62-day code streak"
date:       2018-01-05 21:36:50 +0000
permalink:  what_i_did_in_a_62-day_code_streak
---

I committed code on Github for 62 days, I wanted to go for 75 days but it didn't happen and I was close.  Here are the topics of what I learned and did during the coding streak.

## -Began Hacktoberfest contribution on a Github user's repository
I had not contributed to Hacktoberfest until October 2017. I recall the event and legitimately I had already met the requirements of getting a Hactobkerfest t-shirt by a long shot but I wanted to actually use my skills and make a contribution.  I found a few [Hacktoberfest](https://hacktoberfest.digitalocean.com/) projects on the site and picked one that I believed I could contribute open-source code on.  This was a great new branch of coding I had done and broke up the daily learning I had done during the time.  Instead of learning I was using what I learned to contribute in the programming community.

## -Made my own project for Hacktoberfest for beginners to contribute to
In the month of October, Github and Digital Ocean sponsor a month long coding, contributing, programming event to get people involved in open source.  I was inspired and decided to create a [small project](https://github.com/mekowalski/hacktoberfest17-beginner) where newer coders can fork, clone and contribute a profile of themselves and a `Hello World` script in their favorite language.  This was great for me because I was also able to learn simple Github tasks of how to merge pull requests, write notes to other programmers and use tags.

## -Began Codewars challenges more, mainly with building JavaScript algorithms
During this coding streak I began partnering with a couple of students on the same level of programming as myself and I began attending Learn-hosted study groups to problem-solve [Codewars](https://www.codewars.com) katas.  I had been notified of Codewars many times but I never took the time to look it over and actually engage in the katas to practice and test my knowledge.  I finally began doing Codewars katas with the suggestion of an instructor who I deem a spectacular programmer.  If they suggested sharpening my skills with Codewars then that is what I was going to do.  I still work on katas and try to attend the weekly study groups for Codewars challenges but it's not as consistent as I'd like it to be.  Maybe that will be my next challenge.

## -I passed my 4th Learn assessment
Passing my [4th Learn assessment](https://www.youtube.com/watch?v=ykcQYRr7lrc&list=PLVGZtzeBJ6sPPodCh-Pw8ngNXZcdeZTAK&index=6) on Javascript with Rails was a huge milestone for me.  In the former meetings I only passed 1 of 4 assessments on one try.  The other 3 I had to go back and work on a few parts and re-learn a few topics.  This was the case with my 4th assessment.  Though, this one was possibly the worst of them.  I flew by the learning of JavaScript and barely grasped the concepts and information that was in front of me.  Because I took on the project with half the confidence, I failed my 4th assessment and was essentially asked to re-learn the fundamentals of Javascript alongside solving Codewars katas.  I rescheduled my 2nd attempt at reviewing and being tested on my 4th assessment and finally passed with twice the comprehension after re-learning JavaScript basics.  I had greater assurance of what I was asked to do and how to explain what I was doing.  I continue to tell myself that I need to understand what I am learning, that I have to take my time because this entire process will be a life time and that re-learning is already tough to begin with so don't make it even more difficult.  Passing the 4th assessment meant that I was able to move forward onto the final section of the curriculum.

## -Began learning an immense amount of React
React is tough. This is what I know of [React](https://reactjs.org/).  It mainly is a JavaScript library that is quite efficient, flexible and declarative for building user interfaces.  What I learned is that React helps easily render views. It `declaratively` programs what you want your code to do.

> Example:
> 
> Process of hiring someone to paint the house
> 
> -Hire the person
> 
> -Tell them to paint the house walls this color
> 
> -They get it done
> 
> No other explanation because the painter knows EXACTLY what to do

React works with JSX to help clean and organize the view code.  React can be rendered on the server which helps speed up a JavaScript application and show users the rendered HTML as quickly as possible.  Somehow someway React will introduce you to a loving of functional programming due to React working well with function, pure, immutable patterns.

>A few setbacks of React are:
>
>-You don't get an event system, besides vanilla DOM events
>
>-You don't have AJAX capabilities
>
>-There are no promises
>
>-There isn't any application framework
>
>-You work with plugins such as Webpack and Babel that may be confusing tools to use but they are worth knowing
>
>-Flux and data flow are great complex patterns for beginners, state management is difficult to comprehend for new React users.  Most users have now moved onto Redux from Flux and is the most popular state management library

So why should I consider React?  There are a few reason why React is still a great library.  It works well for teams that enforce UI and workflow patterns.  UI code is readable and easy to maintain.  Lastly component-based UI is the future of web development and is encouraged to learn now.

## -Learned about Props and State and how to differentiate the two
For most part while learning React I couldn't figure out props and state.  I was uncertain if they were the same or different, and if different, how so.  It took me a good amount of googling, article-reading and question-asking to figure out the differences.  

>This is what I know:
>
>-Both are POJO's, plain old JavaScript objects
>
>-Both props and state changes trigger render update
>
>-Both are deterministic
>
>-Props: props is short for properties. Props are component configurations, immutable(not changeable) as far as the component receiving them, component can't change its props but is responsible for putting them together
>
>-State: Begins with default value when a component mounts, serializable representation of one point in time(state is changeable).  State and props are related and the state of one component may often become the props of a child component.

## -Learned how to build Components
[Components](https://reactjs.org/docs/components-and-props.html#functional-and-class-components) let you split the UI into independent reusable pieces and keep the separation of each piece.  It is an abstract class, therefore it makes sense to refer to React.Component directly.  There is typically a subclass attached with the Coomponent that defines and requires a render() method.  Components have lifecycles for Mounting, Updating, Unmounting and Error-handling.  There are also class properties of `defaultProps` & `displayName` and instance properties of `props` & `state`.
	
## -Learned another mass amount of Redux
Redux is a fairly new topic for React, it was introduce by its creator [Dan Abramov](https://egghead.io/courses/getting-started-with-redux) in 2015.  It is considered brilliant in pairing with React but what is Redux exactly?  What I found in my research of Redux is this: Redux is a stable, lightweight, state container for JavaScript apps.  Redux encapsulates your entire application's state in one place and the application's state is immutable.  Because the original state or states are unchanged, this makes debugging easy because there is isolation on the action that caused state change(s).  I found that although, complex(for me), Redux is quite simple.  Functions are used to call a reducer(a JavaScript reduce method) that takes two parameters: an action and a next state.  Reducers are also pure functions therefore no side effects occur.

## -Learned the usage of Webpack, Babel and JSX
[Webpack](https://web-design-weekly.com/2014/09/24/diving-webpack/) is an efficient tool that, when working with a large application, helps organize the code by splitting the application into multiple files.  Once the codebase is split into chunks then they can be loaded on demand.  This helps reduce initial application loading time.  Breaking JavaScript code into modules is considered a great solution to handle organization.  Not only does a module system enhance development, it enhances the user experience.

Babel is known as a transpiler, efficient and useful for its ability to turn JavaScript ES6 into the code that runs on the browser being currently used.  Developers can virtually use all the new ES6 features without sacrificing backwards compatibility for older browsers.  [Babel](https://codemix.com/blog/why-babel-matters) not only tracks ES6, it also tracks the next version of JavaScript.  Babel does not have time constraints because it runs at compile time.

JSX is a syntax extension to JavaScript.  [JSX](https://reactjs.org/docs/introducing-jsx.html) is a preprocessor step that adds XML syntax to JavaScript.  It is used with React to describe with the UI should look like.  It may seem like a template language but it is with full power of JavaScript.  Although React does not require use of JSX, it is a helpful, visual aid when working with UI inside JavaScript code.

