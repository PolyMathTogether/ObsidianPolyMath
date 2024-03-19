# Definition
---
> [!info]
> Schedule is collection of **[[System]]s** and **metadata**.

# Metadata
---
- Run conditions.
- Odering dependencies.
- Systems sets.

# Primary Schedules:
---
- There are **3 foundational schedules**: [[Main]], [[Extract]], [[Render]].
- These run repeatly in a loop and each loop construct a frame.
- [[Main]] runs a sequence of other schedules, includes [[Update]]. With first runs a sequence of "startup" systems (such as [[Startup]]).

