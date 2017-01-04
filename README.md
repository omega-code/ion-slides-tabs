# ion-slides-tabs
Second fork from [Rakonda] (https://github.com/Rakonda/ion-slides-tabs). Add support for on-slide-changed attribute. onSlideChanged expression is called when seected tab is changed.
This fork is an adaptation of the [JKnorr91 code](https://github.com/JKnorr91/ion-slide-box-tabs) using the new directive [ion-slides](http://ionicframework.com/docs/api/directive/ionSlides) instead of [ion-slide-box](http://ionicframework.com/docs/api/directive/ionSlideBox).

All credits and thanks to [JKnorr91](https://github.com/JKnorr91).

Changes:

* Replaced ion-slide-box directive with ion-slides.
* Centralized the active tab. (when possible)
* Updated the demos to Ionic v1.3.1

This Directive adds Tabs for the Ionic Slidebox with moving indicator at the bottom.

## Preview & Demos

![alt tag](/example/img/slideTabs.gif)

[Example 1: Simple, fixed sizes](https://leoruhland.github.io/ion-slides-tabs/example/example1.html)

[Example 2: Multiple tabs, scrollable](https://leoruhland.github.io/ion-slides-tabs/example/example2.html)

[Example 3: Multiple dynamic tabs, scrollable](https://leoruhland.github.io/ion-slides-tabs/example/example3.html)

[Example 4: Initial slide](https://leoruhland.github.io/ion-slides-tabs/example/example4.html)

## Installation

1. Add the *slidingTabsDirective.js* to your Ionic Project and include it in your *index.html*.

  Example:
  If you put the *slidingTabsDirective.js* to your *js* folder, you should paste the following line into your *index.html* anywhere after the ionic inclusion.

  ```html
  <script src="js/slidingTabsDirective.js"></script>
  ```

2. Add the SCSS or the CSS code from *slidingTabs.scss* or *slidingTabs.css* to your project Styles.

## Usage

In order to use the Tabs with an existing Slides, add the *ion-slides-tabs* Attribute to the *ion-slides* Element.
To name the Tabs you should add the Attribute *ion-slide-tab-label="yourLabel"* to the *ion-slide-page* of the Slides. You can paste in any HTML for the labels.

Example:
```html
<ion-content scroll="false">
    <ion-slides slider="slider" ion-slides-tabs on-slide-changed="selectedPostChanged(index)">
        <ion-slide-page ion-slide-tab-label="test"><h1>Tab 1</h1></ion-slide-page>
        <ion-slide-page ion-slide-tab-label="secondTest"><h1>Tab 2</h1></ion-slide-page>
        <ion-slide-page ion-slide-tab-label="<b>boldTest</b>"><h1>Tab 3</h1></ion-slide-page>
    </ion-slides>
</ion-content>
```

## API
Currently there ist only one attribute to change the behaviour of the tabs:


|Attribute|Type|Default|Description
|-----------|------|-------------|---------|
| slide-tabs-scrollable | boolean | *true* | Wheter the tabs should be scrollable (*true*) or fill up the viewport width (*false*). In case of *false*, every tab will have the same size.
