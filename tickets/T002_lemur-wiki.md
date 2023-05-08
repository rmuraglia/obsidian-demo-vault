---
project: " #proj/lemur "
work-period: " #Y2023Q2 "
status: " #in-review "
results:
    - "[wiki](https://en.wikipedia.org/wiki/Lemur)"
---

- Ticket: `=choice(regextest("^T\d+_", this.file.name), "[" + split(this.file.name, "_")[0] + "](http://tracking.website.com/" + split(this.file.name, "_")[0] + ")", "n/a")`
- Results: `=choice(length(this.results[0]) = 0, "n/a", this.results)`

# Objective

Find the wikipedia article about lemurs for further reading
