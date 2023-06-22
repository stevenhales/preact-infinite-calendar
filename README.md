<div align="center">
<img src="https://raw.githubusercontent.com/clauderic/react-infinite-calendar/master/.github/logo.png" width="180"/>
</div>

# Preact Infinite Calendar
This is a fork of react-infinite-calendar. The purpose is to add compatibility for Preact. An error you will get if using the original with preact is:
TypeError: Cannot create property 'current' on string 'node'
Preact does not support string-based refs, so I have replaced them with callback refs to work correctly with Preact.

Features
---------------

* **Infinite scroll** – Just keep scrollin', just keep scrollin'
* **Flexible** – Min/max date, disabled dates, disabled days, etc.
* **Extensible** – Add date range-selection, multiple date selection, or create your own HOC!
* **Localization and translation** – En français, s'il vous plaît!
* **Customizeable** – Customize and theme to your heart's content.
* **Year selection** – For rapidly jumping from year to year
* **Keyboard support** – ⬆️ ⬇️ ⬆️ ⬇️ ⬅️ ➡️ ⬅️ ➡️ ↩️
* **Events and callbacks** – beforeSelect, onSelect, onScroll, etc.
* **Mobile-friendly** – Silky smooth scrolling on mobile

<div style="padding:30px">
<img src="https://raw.githubusercontent.com/clauderic/react-infinite-calendar/master/.github/preview.gif" width="300" />
</div>

Getting Started
---------------

Using [npm](https://www.npmjs.com/):
```
npm install preact-infinite-calendar --save
```

ES6, CommonJS, and UMD builds are available with each distribution. For example:
```js
import InfiniteCalendar from 'preact-infinite-calendar';
import 'preact-infinite-calendar/styles.css'; // Make sure to import the default stylesheet
```

Usage
------------
### Basic Example

```js
import InfiniteCalendar from 'preact-infinite-calendar';
import 'preact-infinite-calendar/styles.css'; // only needs to be imported once

// Render the Calendar
var today = new Date();
var lastWeek = new Date(today.getFullYear(), today.getMonth(), today.getDate() - 7);

render(
  <InfiniteCalendar
    width={400}
    height={600}
    selected={today}
    disabledDays={[0,6]}
    minDate={lastWeek}
  />,
  document.getElementById('root')
);
```
License
---------
*preact-infinite-calendar* is available under the MIT License- as per the original.
