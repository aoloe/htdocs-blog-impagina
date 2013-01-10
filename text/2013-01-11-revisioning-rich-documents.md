---
title:
---
Among the most common requests for Scribus many relate to getting several people to collaborate while working on a document.
We hear often questions about collaboration. A straightforward way to implement it would be to share the documents through an existing revision system like SVN or GIT. If it works so well for sharing code, why shouldn't it work also for content? Well, big problems arise when merging files that have conflicting changes. Or even changes that seem to be conflicting.
And, here, also merging code can also produce headaches:
- when one does not notice that concurrent changes in different parts of a document or of the project are conflicting.
- when the same lines are edited in parallel in different ways.

-> rich content documents

So, one way to avoid conflict ­ or at least make it easier to check and solve the conflicts ­ would be to store the document in smaller parts:
- fewer chances that a file is edited in parallel
- the changes are easier to merge

Eventually, it should be even useful to separate the information about the content and the container.
