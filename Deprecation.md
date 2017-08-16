# Good Deprecation Habits


1. Determine a thing needs deprecation and (discuss w/ knowledgable parties if applicable).
    1. How long it must remain deprecated before it is removed is an important factor driven by the context involved.
2. If used in new code it should barf w/ information:
    1. what is deprecated
    2. *if applicable*: why it was deprecated (or pointer to more info about the deprecation)
    3. when it was deprecated
    4. when it will be removed
    5. what case is tracking the removal
       1. case should have a due date and details of what needs removed/updated (including documentation)
       2. ensure that the case is followed through on at the given date
    6. what to use instead
    7. *if applicable* how to go ahead and use the deprecated thing
    8. Ideally, when changing the thing to be deprecated, you also remove all use of it from all code you control.
3. *if applicable*: if used in existing code: allow it to run but give the info in item 2 as a warning
4. *if applicable*: send out notices to appropriate audiences w/ info in item 2 about it being deprecated and again when it is removed
5. *if applicable*: The changelog should include clearly tagged deprecation and removal info (e.g. the “[Keep a Changelog](http://keepachangelog.com/en/1.0.0/)” format has a nice mechanism for that)
6. *if applicable*: map old systems to new (e.g. in a REST app a 301 could get them to the new route)
