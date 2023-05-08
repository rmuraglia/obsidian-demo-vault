---
project: " #proj/lemur "
work-period: " #Y2023Q1 "
status: " #complete "
results:
    - "[pic 1](https://images.app.goo.gl/RQDXXsSoR4Fm3c8c9)"
    - "[pic 2](https://images.app.goo.gl/ifPmHvBTtyosuYeZA)"
---

- Ticket: `=choice(regextest("^T\d+_", this.file.name), "[" + split(this.file.name, "_")[0] + "](http://tracking.website.com/" + split(this.file.name, "_")[0] + ")", "n/a")`
- Results: `=choice(length(this.results[0]) = 0, "n/a", this.results)`

# Objective

Learn what lemurs look like

# Findings

Here are two pictures I found:

[source](https://images.app.goo.gl/RQDXXsSoR4Fm3c8c9) 
![[lemur01.png]]

[source](https://images.app.goo.gl/ifPmHvBTtyosuYeZA) 
![[lemur02.png]]