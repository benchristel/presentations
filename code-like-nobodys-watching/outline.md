## Part One: Failure Modes of Design

## Part Two: Style

- Why We Fail to Apply the Ideas of Masters
  - (design ideas come from analyzing the work of master programmers)
  - (masters often can't explain what they actually do)
  - (we cargo-cult the styles of masters)
  - (image-based architecture; image-based programs)
  - (but masters work "without style" - it's an output, not an input)
    - Kent Beck "the system is riding me"
    - C.A. "essentially a building without style"

## Part Three: Generative Rules

- Bridging the Master-Beginner Gap
  - Christopher Alexander: The Fundamental Process
    (C.A. works directly with clients and has built many "user-designed" buildings)
  - Sandi Metz & Katrina Owen: _99 Bottles of OOP_ and the flocking rules
    (whyarecomputers podcast)

## Part Four: Beginner's Mind

- how beginners program
- "the simplest thing that could possibly work"
- why imperative programming is essential
- "duplication is far cheaper than the wrong abstraction"

obstacles to working this way?

- frameworks
- side effects
- can't be naive about architecture

- create abstractions late, target specific problems during refactoring

## Part Five: The Timeless Way of Programming

- The likely character of programs that have unfolded by generative processes
- the flocking rules first produce procedures with no internal duplication and
  a high degree of symmetry (flat conditionals, case statements)
- then a shallow hierarchy of functions, procedures, and data values
- some data values attract functions and procedures to them, becoming objects
- high cohesion, low coupling, symmetry, very little duplication, isolated changes
- but some features that would be discouraged by current practice
  - some long methods
  - apparently missing abstractions, repeated code that hasn't been given a name
    and DRYed out. (this is the result of deferring abstraction)
  - long, flat `case` or `else if` chains, rather than nested conditionals
  - procedural code, not everything is object oriented
  - functional code in mostly-OO programs
  - stateful objects in mostly-functional programs
  - nothing called `Manager`
  - the code will be ordinary, free of pretention
- prefactor on master, (add the feature, postfactor) transactionally
