---
title: Software Engineering at Google
date: 2025-08-18T14:06:03.651+02:00
category: books
tags: []
excerpt: My highlights
---

## Page 495

> Many software engineers are attracted to the task of building and launching new systems, not maintaining existing ones.


----
## Page 500

> “hope is not a strategy.”


----
## Page 502

> We’ve learned at Google that without explicit owners, a deprecation process is unlikely to make meaningful progress, no matter how many warnings and alerts a system might generate.


----
## Page 505

> statically determine which customers use a given library, and often to sample existing usage to see what sorts of behaviors customers are unexpectedly depending on. Because runtime dependencies generally require some static library or thin client use, this technique yields much of the information needed to start and run a deprecation process. Logging and runtime sampling in production help discover issues with dynamic dependencies. Finally, we treat our global test suite as an oracle to determine whether all references to an old symbol have been removed.


----
## Page 505

> To prevent deprecation backsliding on a micro level, we use the Tricorder static analysis framework to notify


----
## Page 506

> users that they are adding calls into a deprecated system and give them feedback on the appropriate replacement.

