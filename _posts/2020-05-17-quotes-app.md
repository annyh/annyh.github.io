---
layout: post
title: Creating a React Native app over a weekend
tags: technology
---

Since one of my guiding principles is **to create more than I consume**, and I've been reading on my phone, I figured why not create a *mobile app to direct my reading*?
Specifically I wanted a [quotes app](https://github.com/annyh/quote-app-react-native) to save interesting quotes by interesting people. As for skill level, I've dipped my toes in [React Native](https://reactnative.dev/) (a framework for developing native apps) a few weeks before, and have 5+ years of React and JavaScript experience. Here's how I, a React Native newbie, designed and created a React Native app over one weekend.

### Video walkthrough of the [Quotes App](https://github.com/annyh/quote-app-react-native)
[![Quote app](http://img.youtube.com/vi/8e7yGb7OFbI/0.jpg)](http://www.youtube.com/watch?v=8e7yGb7OFbI "Quote app")

### 1. Be clear about what the app does
For research I looked on Google Play to find quote-saving apps, and found them ad-filled and/or sharing-oriented. Instead I wanted a simple, ad-free interface to save interesting quotes by insteresting people. On Friday post dinner I sketched the app's UI on a paper notebook, and the sketches set the tone for the development on Saturday.

### 2. Keep the UI simple
I used [react-native-elements](https://react-native-elements.github.io/react-native-elements/docs/overview.html) for the UI, including a ListView and ButtonGroup. For navigation I used [react-navigation's bottom tabs](https://reactnavigation.org/docs/bottom-tab-navigator/) because tabs are faster to access than the collapsible sidebar.

### 3. Reuse code 
To get quotes I used this [Heroku app derived from Goodreads](https://goodquotesapi.herokuapp.com/#/developer). For data storage I used [AsyncStorage](https://reactnative.dev/docs/asyncstorage.html), which stores data on the phone. [AsyncStorage has a 6MB limit](https://dev.to/amanhimself/what-is-asyncstorage-in-react-native-4af4) and it's not a deal-breaker since I'm prototyping and storing short strings. I could have gone with [Firebase](https://firebase.google.com/) or another database, but given the tight deadline, I reused the AsyncStorage save/delete code, mostly from [this repo](https://github.com/mahmudahsan/todos-react-reactnative/tree/master/mobile/model). 

### 4. Some UI decisions are made midway
Midway through Saturday I thought about and added a **link to the authors' Wikipedia page**, since the URL structure is predictable for most English authors. This makes the authors' backgrounds easy to access. Additionally I noticed how taxing it is for the user to come up with a new search for quotes. So I added the search by **random tag** feature. The **random tag** is one of [100 possible values](https://www.cmu.edu/career/documents/my-career-path-activities/values-exercise.pdf). Randomization lowers the barriers to discover more interesting quotes.

### 5. Track to dos to work briskly
I jot down development tasks in the [readme.md](https://github.com/annyh/quote-app-react-native/blob/master/readme.md#todo) so I can pick up where I left off. Also typing out the tasks clarifies the steps for progress.

### That's a wrap!
It was a productive weekend, with enough time leftover to take [a video](http://www.youtube.com/watch?v=8e7yGb7OFbI) and write up this blog post. The [source code is here](https://github.com/annyh/quote-app-react-native). It still has [some to dos](https://github.com/annyh/quote-app-react-native/blob/master/readme.md#todo), so I can pick it up during the week, or another weekend :)








