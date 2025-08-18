---
title: Software Engineering at Google
date: 2025-08-18T12:41:17.792+02:00
category: books
tags: []
excerpt: My highlights
---

## Page 505

> statically determine which customers use a given library, and often to sample existing usage to see what sorts of behaviors customers are unexpectedly depending on. Because runtime dependencies generally require some static library or thin client use, this technique yields much of the information needed to start and run a deprecation process. Logging and runtime sampling in production help discover issues with dynamic dependencies. Finally, we treat our global test suite as an oracle to determine whether all references to an old symbol have been removed.

