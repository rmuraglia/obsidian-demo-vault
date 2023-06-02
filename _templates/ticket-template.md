---
project: " "
work-period: " "
status: " "
results:
    - ""
---

- Project hub: ` $=dv.pages('"projects"').where(p => dv.current().project.includes(p.project)).file.link`
- Ticket: ` =choice(regextest("^T\d+_", this.file.name), "[" + split(this.file.name, "_")[0] + "](http://tracking.website.com/" + split(this.file.name, "_")[0] + ")", "n/a")`
- Results: ` =choice(length(this.results[0]) = 0, "n/a", this.results)`
