---
project: " #proj/koala "
work-period: " #Y2023Q2 "
status: " #complete "
results:
    - ""
---

- Ticket: `=choice(regextest("^T\d+_", this.file.name), "[" + split(this.file.name, "_")[0] + "](http://tracking.website.com/" + split(this.file.name, "_")[0] + ")", "n/a")`
- Results: `=choice(length(this.results[0]) = 0, "n/a", this.results)`

# Objective

Similar to [[T001_lemur-picture]], learn what koalas look like.

# Findings

Here are some pictures:

[source](https://images.app.goo.gl/eP1LghP9cWdbgo726)  
![[koala01.jpeg]]

[source](https://images.app.goo.gl/DYDeJFmLbvpfh98s8) 
![[koala02.jpeg]]