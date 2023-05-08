---
project: " "
work-period: " "
status: " "
results:
    - ""
---

- Ticket: ` =choice(regextest("^T\d+_", this.file.name), "[" + split(this.file.name, "_")[0] + "](http://tracking.website.com/" + split(this.file.name, "_")[0] + ")", "n/a")`
- Results: ` =choice(length(this.results[0]) = 0, "n/a", this.results)`
