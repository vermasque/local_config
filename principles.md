Principles
==========

Principles for software development inspired by the book Principles by Ray Dalio.

## Execution

- Before doing something, consider how it can be done safer and don't be lazy in managing risk.
- If an event has low probability of occurring and low impact, then it is not worth addressing.  Cut scope to focus on what matters.
- When an obviously good solution is not available, aim for a middle ground (for example, 50/50) to balance competing concerns.
- Inaction should be justified to prevent indecision.
- Be consistent in decisions to provide clarity on when to do what.
- Balance forward progress with perfection and perfection now vs. later.
- Set time limits for something to be done and pivot when the limit is reached.
- Completeness to improve confidence that something wasn't missed.
- Iterate by breaking tasks up so you can get something worthwhile in a reasonable time frame for those who are waiting.

## Software

- Validate inputs before using them.
- Reduce context switching to speed things up (for example, study an example entirely before designing based on it).
- All bug fixes or features should go through some design process to:
  - Produce excellent code
  - Increase the accuracy of estimates (more aware of effort required)
  - Split total effort into small tasks that:
    - Can be done in parallel
    - Can fill backlogs with high-value tasks instead of defaulting to low-value tasks just to give someone things to do are easier for reviewers to review
- If a new feature applies to a lot of traffic automatically (not opted in by users), there is significant risk; an unknown problem could affect a lot of the traffic without a way for users to revert.  Add a feature flag so the feature can be rolled back rapidly without rolling back an entirely release.
- Use staged rollouts to learn about problems in new features while minimizing impact of unknown bugs.
- Choose straightforward long-term options unless an unresolvable problem(s) forces a short-term solution.
- Design for the long-term to determine those unresolvable problems with timeboxing to avoid analysis paralysis.
- Use exponential estimation to trade precision for accuracy.
- We should not have pockets of wrong that might bite us in the future.
- Prefer the strongest type for some field or column in general.
  - For example, Country over short to simplify downstream (nil or Country value).
- Implementation and tests should be simple to explain to avoid confusing users and developers.
- Design to eliminate potential edge cases, failures, or errors instead of letting be possible and then defending against them.
- TDD provides a minimum level of testing but may need to convince reviewers of sufficient testing with more thoroughness.
- Write unit tests first over integration tests for speed primarily as well as easier discoverability and debugging.
  - Integration tests supplement for wiring and serde and when unit testing is not feasible.
  - Can see overlap between unit and integration tests but not if perceived as functionality vs. wiring.

## People

- Hold people accountable or watch quality drop (productivity, availability, etc.).
- If you have a question, insist on it getting answered to avoid potential problems. Something not understood might mean something wrong.

