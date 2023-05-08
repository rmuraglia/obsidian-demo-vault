---
project: " #proj/koala #proj/lemur "
work-period: " #Y2023Q2 "
status: " #in-progress "
results:
    - "[doc](http://tracking.website.com/docs/qwertyuiop)"
---

- Ticket: `=choice(regextest("^T\d+_", this.file.name), "[" + split(this.file.name, "_")[0] + "](http://tracking.website.com/" + split(this.file.name, "_")[0] + ")", "n/a")`
- Results: `=choice(length(this.results[0]) = 0, "n/a", this.results)`

# Objective

Compare the diets of lemurs and koalas

# Findings

## 2023-05-07

Based on review of [[T002_lemur-wiki]], lemur diets are varied:

- generally smaller species eat fruit and insect
- while larger species eat mostly plant material

Tomorrow, I plan to learn what koalas eat to complete the comparison.