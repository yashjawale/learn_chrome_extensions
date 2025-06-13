# Learning Chrome Extensions

This is my repository for learning to build chrome extensions

Each branch has code relevant to chapters from [Chrome for developers extensions getting started guide](https://developer.chrome.com/docs/extensions/get-started/)

## Hello World
First hello world extension \
Displays "Hello Extensions" when user clicks the extension toolbar icon

**Branch:** `main`

## Run scripts on every page
First extension that inserts a new element on the page. \
Adds the expected reading time to any Chrome extension and Chrome Web Store documentation page.

### Interesting points:

-   [Regular expressions](https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions#writing_a_regular_expression_pattern) used to count only the words inside the `<article>` element.
-   [`insertAdjacentElement()`](https://developer.mozilla.org/docs/Web/API/Element/insertAdjacentElement) used to insert the reading time node after the element.
-   The [classList](https://developer.mozilla.org/docs/Web/API/Element/classList) property used to add CSS class names to the element class attribute.
-   [Optional chaining](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/Optional_chaining) used to access an object property that may be undefined or null.
-   [Nullish coalescing](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing_operator) returns the `<heading>` if the `<date>` is null or undefined.

**Branch:** `run_scripts_on_every_page`

## Inject scripts into the active tab
Simplify the styling of the current page by clicking the extension toolbar icon. \
Simplifies the styling of the Chrome extension and Chrome Web Store documentation pages so that they are easier to read.

### Interesting points:

-   Use the extension service worker as the event coordinator.
-   Preserve user privacy through the `"activeTab"` permission.
-   Run code when the user clicks the extension toolbar icon.
-   Insert and remove a style sheet using the [Scripting](https://developer.chrome.com/docs/extensions/reference/api/scripting) API.
-   Use a keyboard shortcut to execute code.

**Branch:** `inject_scripts_into_active_tab`

## Handle events with service workers
Introduction to Chrome Extension service workers. \
allows users to quickly navigate to Chrome API reference pages using the omnibox.

### Interesting points:

-   Register your service worker and import modules.
-   Debug your extension service worker.
-   Manage state and handle events.
-   Trigger periodic events.
-   Communicate with content scripts.

**Branch:** `handle_events_with_service_workers`

## Manage tabs
A tabs manager to organize your Chrome extension and Chrome Web store documentation tabs.

### Interesting points:

-   Create an extension popup using the [Action](https://developer.chrome.com/docs/extensions/reference/api/action) API.
-   Query for specific tabs using the [Tabs](https://developer.chrome.com/docs/extensions/reference/api/tabs) API.
-   Preserve user privacy through narrow host permissions.
-   Change the focus of the tab.
-   Move tabs to the same window and group them.
-   Rename tab groups using the [TabGroups](https://developer.chrome.com/docs/extensions/reference/api/tabGroups) API.
-   The [Collator](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Intl/Collator) used to sort the tabs array by the user's preferred language.
-   The [template tag](https://web.dev/webcomponents-template/) used to define an HTML element that can be cloned instead of using `document.createElement()` to create each item.
-   The [URL constructor](https://developer.mozilla.org/docs/Web/API/URL/URL) used to create and parse URLs.
-   The [Spread syntax](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Operators/Spread_syntax) used to convert the Set of elements into arguments in the `append()` call.

**Branch:** `manage_tabs`

---
Learning Chrome Extensions