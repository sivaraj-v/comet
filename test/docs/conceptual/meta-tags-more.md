---
title: Testing Metadata | Microsoft Docs
description: < & / ' > he's Special characters
---

# Testing metadata

Let's make sure that meta tags are rendered as they should be, escaping HTML entities in the "description" and "og:description" meta tags.

The meta tags in the description should be encoded, and in the source they should look like this:

```
&lt; &amp; &#x2F &#x27; 's Special characters
```

Both metadata tags should match - except that the "description" tag does not escape the forward slash.

This approach will double-encoded existing encoding values.
