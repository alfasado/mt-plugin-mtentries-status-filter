# Entries Block Tag Status Filter Argument Plugin for Movable Type

In most situations a template should render the Entries marked as "published."
There are scenarios, however, when publishing entries with other statuses is
required. This plugin facilitates that with a new argument for the Entris block tag: `status_filter`.

Entries have one of the following statuses:

* Unpublished (`1`)
* Published (`2`)
* Review (not commonly used, `3`)
* Scheduled (`4`)
* Junk (used with community-submitted content, `5`)

The `status_filter` argument takes one or more of the numeric status representations; more than one should be in a comma-separated list. Examples are shown below.

The default behavior to render entries marked "published":

    <mt:Entries status_filter="2">
        <p><mt:EntryTitle></p>
    </mt:Entries>

Render any Entries marked "unpublished":

    <mt:Entries status_filter="1">
        <p><mt:EntryTitle></p>
    </mt:Entries>

Show all unpublished, published, and scheduled Entries:

    <mt:Entries status_filter="1,2,4">
        <p><mt:EntryTitle></p>
    </mt:Entries>

