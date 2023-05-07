work-period:: #Y2023Q2

> [!todo]
> Tickets currently in progress:
> ```dataview
> table without id
>     project
>     , choice(
>         regextest("^T\d+_", file.name)
>         , "[" + split(file.name, "_")[0] + "](http://tracking.website.com/" + split(file.name, "_")[0] + ")"
>         , "n/a"
>     ) as ticket
>     , file.link as obsidian_note
> from "tickets"
> where status = " #in-progress "
> ```

> [!success]
> Tickets currently in review:
> ```dataview
> table without id
>     project
>     , choice(
>         regextest("^T\d+_", file.name)
>         , "[" + split(file.name, "_")[0] + "](http://tracking.website.com/" + split(file.name, "_")[0] + ")"
>         , "n/a"
>     ) as ticket
>     , file.link as obsidian_note
> from "tickets"
> where status = " #in-review "
> ```

# 2023-05-07

- [ ] create two sample projects
- [ ] create ticket index template
- [ ] create ticket index
- [ ] create sample tickets

# 2023-05-06

- [x] create daily todos template
- [x] create daily todos tracker for #Y2023Q2 
- [x] create project hub template
- [ ] create two sample projects
- [ ] create ticket index template
- [ ] create ticket index
- [x] create ticket template
- [ ] create sample tickets