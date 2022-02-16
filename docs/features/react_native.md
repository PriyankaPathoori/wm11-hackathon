---
title: React Native
layout: default
parent: Docs
nav_order: 1
---

# {{ page.title }}


React Native is a mobile app framework from Facebook. It is based on ReactJS priniciples (Virtual DOM). Developers define app UI using the React Native markup (and extensions) in JavaScript. In runtime, based on this UI definition, React Native will render UI using native UI controls (similar to native apps).

In mobile devices, Cordova apps displays HTML based UI using a browser component. So, developers can use HTML, CSS along with JavaScript in Cordova apps. React native apps will run JavaScript in JavaScript runtime (jsc and hermes). React Native bridge manipulates native UI based on the response (Virtual DOM) from javascript. So, **CSS and HTML cannot be used in React Native apps**. Markup (jsx), styles, and logic have to be defined in JavaScript for React Native apps.

## Things to be noted

In WaveMaker, apps are developed with WaveMaker markup, variables, Javascript and styles defined in CSS. Let see the changes in the platform and the required learnings.

### Markup
During build, WaveMaker platform will convert the WaveMaker markup to React Native markup. So, there is no change in the existing WaveMaker markup. But, not all widgets and widgets properties are supported. [Click here](./widgets.html) to check widget support. 

### Variables
There is no change in the way of defining variables. Databases and corresponding variables are not supported. [Click here](./variables.html), to check the Variable support.

### Script
All UI and Variable event callbacks work as it is. Web browser APIs are not supported. HTML DOM manipulating JS libraries (jQuery etc.,) will not work when app is installed in a phone. Adding a JS library is not supported.

### Styles
React Native styles have to be defined in JavaScript. CSS is not supported in React Native. But, in WaveMaker styles are defined in CSS. A partial CSS support is added so that WaveMaker developer can define styles in CSS. Donot add CSS classes copied from web preview HTML DOM tree. More details can be [found here](../how_to/styles.html).

### Theme
Themes are supported. Click here to learn about how to generate themes.

### Prefabs
Prefabs are supported. But, following limitations are applicable
- HTML DOM and API to manipulate it, should not be used.
- As a prefab can be used in a web app, Cordova based mobile app or a React Native based mobile app. Stylsheet of a prefab has to be divided into two parts by the line ``` /*REACT_NATIVE_STYLES*/ ```. After this line, styles for React Native environment can be placed.
- Adding a JS file is not supported
- Widgets that are not supportetd by WaveMaker React Native runtime, are discarded.

## Additional Resources
[React JS](https://reactjs.org/)<br>
[React Native](https://reactnative.dev/)<br>
[Native Studio Introduction Video - 1](https://drive.google.com/file/d/1ZeVc6bR_GbsIosm8YlW_8LfoJNGjXZ7n/view?usp=sharing)<br>
[Native Studio Introduction Video - 2](https://drive.google.com/file/d/1OsouVnNFQWEJEgmTXKjggS4Ft8Zaod3A/view?usp=sharing)<br>