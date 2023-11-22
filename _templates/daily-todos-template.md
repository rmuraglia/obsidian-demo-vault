work-period::

> [!Abstract] Not Started
> ```datavieww
> table without id
>     project
>     , choice(
>         regextest("^T\d+_", file.name)
>         , "[" + split(file.name, "_")[0] + "](http://tracking.website.com/" + split(file.name, "_")[0] + ")"
>         , "n/a"
>     ) as ticket
>     , file.link as obsidian_note
> from "tickets"
> where status = " #not-started "
> ```

> [!todo] In Progress
> ```datavieww
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

> [!success] In Review
> Tickets currently in review:
> ```datavieww
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

> [!attention] Blocked or On Hold
> ```datavieww
> table without id
>     project
>     , status
>     , choice(
>         regextest("^T\d+_", file.name)
>         , "[" + split(file.name, "_")[0] + "](http://tracking.website.com/" + split(file.name, "_")[0] + ")"
>         , "n/a"
>     ) as ticket
>     , file.link as obsidian_note
> from "tickets"
> where status = " #blocked " or status = " #on-hold "
> ```

# YYYY-MM-DD
