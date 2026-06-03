## Code Review Exercise

### Issue 1 - Accessibility, Empty Close Popup Buttons

After conducting a WAVE report, there are a couple "empty button" reports because the buttons only contain an icon and do not have readable text for screen readers. This is an issue because interactive elements should have an accessible name. Since the icon itself is decorative, the button should include an aria-label so assistive technologies can explain what the button does. Adding a title attribute also helps by showing a tooltip when users hover over the button.

Initial code:

```html
<button class="close-popup-button">
  <i class="fa-solid fa-xmark"></i>
</button>
```

Updated code:

```html
<button
  class="close-popup-button"
  aria-label="close popup window"
  title="close popup window"
>
  <i class="fa-solid fa-xmark"></i>
</button>
```

### Issue 2 - Semantic HTML

Another issue I found is the improper use of heading levels throughout the webpage. The page contains multiple h1 headings for different sections such as “Introduction”, “History”, “Characteristics”, “Cat Facts”, and “Tell us what you want to learn more”. While this may visually work, it creates semantic and accessibility issues because heading levels should follow a logical hierarchy. This is an issue because screen readers and assistive technologies rely on heading structure to help users navigate a webpage.

Initial code:

```html
<h1 class="heading-1">Scottish Fold</h1>
<h1>Introduction</h1>
<h1 class="clear-margin-bottom">History</h1>
<h1>Characteristics</h1>
<h1>Cat Facts</h1>
```

Updated code:

```html
<h1 class="heading-1">Scottish Fold</h1>
<h2>Introduction</h2>
<h2 class="clear-margin-bottom">History</h2>
<h2>Characteristics</h2>
<h2>Cat Facts</h2>
```
