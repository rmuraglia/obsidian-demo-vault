Valid ticket statuses: #not-started #in-progress #in-review #blocked #on-hold #complete #abandoned

work-period::

Active projects:
```dataviewjss
let projTags = (
    dv.pages('"tickets"')
    .where(t => t['work-period'].includes(dv.current()['work-period']))
    .project.flatMap(p => p.split(' '))
    .where(p => p.startsWith('#'))
    .distinct()
);

dv.list(
    dv.pages('"projects"')
    .where(p => "project" in p)
    .where(p => projTags.includes(p.project))
    .file.link
)
```

```dataviewjss
const pattern = /^[TD]\d+_/;
const urlPrefix = 'http://tracking.website.com/';

let projTags = (
    dv.pages('"tickets"')
    .where(t => t['work-period'].includes(dv.current()['work-period']))
    .project.flatMap(p => p.split(' '))
    .where(p => p.startsWith('#'))
    .distinct()
);

for (const projTag of projTags) {
    dv.header(1, projTag)

    let tickets = (
        dv.pages('"tickets"')
        .where(t => 
            (t['work-period'].includes(dv.current()['work-period']))
            && (t.project.includes(projTag))
        )
    )

    dv.table(
        ['status', 'ticket', 'obsidian_note', 'results', 'created_date'],
        tickets.sort(t => t.file.cday, 'desc')
            .map(t => [
                t.status
                , pattern.test(t.file.name)
                    ? '[' + t.file.name.split('_')[0] + '](' + urlPrefix + t.file.name.split('_')[0] + ')'
                    : 'n/a'
                , t.file.link
                , t.results
                , t.file.cday
            ])
    )
}
```
