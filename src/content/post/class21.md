+++
date = "04 Apr 2024"
draft = false
title = "Class 21: Aliignment"
author = "David Evans"
slug = "class21"
+++

### Schedule

This weeks computing news discussion is now posted, and due before class on **Thursday, 4 April** for even ids, and by **Monday, 8 April** for odd ids.

There will be an **Exam** in class on **Thursday, 11 April**.

### Slides

[Class 21: Aliignment](https://www.dropbox.com/scl/fi/p7n077k5nru8opwdr0kpr/cs1010-class21.pdf?rlkey=x0pxhb4cfhiis7r87n5vphclp&dl=0)

- Edit distance
- Genome alignment

### Code

Here's the code for [editdistance.html](/editdistance.html):

```JavaScript
function edit_distance(s, t) {
    // Returns the minimum number of edits (single character insert,
    // delete, or replace operations) needed to transform s into t.

    if (!s || s.length == 0) {
        return !t ? 0 : t.length;
    } else if (!t || t.length == 0) {
        return s.length;
    } else {
        match = s[0] == t[0] ? 0 : 1; 
        return Math.min(match + edit_distance(s.substr(1), t.substr(1)), // replace
                    1 + edit_distance(s.substr(1), t), // delete first from s (insert first in t)
                    1 + edit_distance(s, t.substr(1))); // delete first from t (insert first in s)
    }
    console.assert(False, "Should not ever reach here!");
}
```

The version from class is [editdistance1.html](/editdistance1.html).