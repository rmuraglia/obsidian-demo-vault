project:: #proj/koala
active work periods: `$= dv.pages('"tickets"').where(p => p.project.includes(dv.current().project))['work-period'].distinct().sort().join()`

# Ticket index

```dataview
table without id
    work-period
    , status
    , choice(
        regextest("^T\d+_", file.name)
        , "[" + split(file.name, "_")[0] + "](http://tracking.website.com/" + split(file.name, "_")[0] + ")"
        , "n/a"
    ) as ticket
    , file.link as obsidian_note
    , results
    , file.cday as created_date
from "tickets"
where contains(project, this.project)
sort work-period desc, file.cday desc
```
