work-period:: #Y2023Q1 

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

# 2023-02-25

- [ ] do stuff
