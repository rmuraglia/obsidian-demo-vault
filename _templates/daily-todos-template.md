work-period::

> [!todo]
> Tickets currently in progress:
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

> [!success]
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

> [!attention]
> Tickets currently blocked or on hold:
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