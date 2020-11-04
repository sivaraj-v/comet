---
twitterWidgets: true
---

# Twitter Widgets

To include the twitter widgets script on a page, add `twitterWidgets: true` to the YAML header. The docs front-end will load `https://platform.twitter.com/widgets.js` once cookie consent has been granted and the `DOMContentLoaded` event has fired.

Once you've enabled the twitter widgets script you can add the twitter-grid timeline to a page by inserting an anchor tag with the `twitter-grid` class and url to the appropriate timeline.

```markdown
---
twitterWidgets: true
---

## Twitter Grid

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean faucibus elit in elit mattis, eu venenatis elit cursus.

<a class="twitter-grid" href="https://twitter.com/TwitterDev/timelines/539487832448843776">National Park Tweets</a>

Nunc dignissim odio ut nisl fermentum malesuada. Morbi sit amet ex libero. Sed consectetur lectus sem, a varius dui tempus a. In dignissim ultricies lacus, quis rutrum tortor gravida sit amet.
```

Below is a live example:

## Twitter Grid

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean faucibus elit in elit mattis, eu venenatis elit cursus.

<a class="twitter-grid" href="https://twitter.com/TwitterDev/timelines/539487832448843776">National Park Tweets</a>

Nunc dignissim odio ut nisl fermentum malesuada. Morbi sit amet ex libero. Sed consectetur lectus sem, a varius dui tempus a. In dignissim ultricies lacus, quis rutrum tortor gravida sit amet.
