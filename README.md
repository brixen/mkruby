# mkruby

This is a tool to build a Ruby implementation.


## Installation

Coming soon.

Install mkruby with your favorite package manager or install from source.


## Make a Ruby

Every implementation of Ruby has a build system. Every. Single. One.

This simple fact is apparently of no particular interest to most package
managers.

This fact suggests a relatively simple goal for a tool to install one or more
implementations of Ruby: *Put the focking thing where the user requested it,
and don't do anything else.*

Or, in algorithmic pseudo code:

* Put
* the focking thing
* where the user requested it
* Period

Why is this so hard?


## What The Fock, World?

There's the joke about the two hard problems in Computer Science. Naming
things, cache invalidation, and off-by-one errors are undeniably hard
problems. However, they have nothing on package management.

There is *one* hard problem in system maintenance: Installing a piece of
software.

It is such a stupid and hard problem that every single platform has multiple
ways of doing it. They hardly ever work well together. And most of them don't
even work correctly all by themselves. They can't manage dependencies
correctly. They can't upgrade *and* downgrade correctly. They can't
interoperate with other package managers.  They can't interoperate with the OS
defaults. They can't interoperate with the file system's standards or
defaults. They can't interoperate with software installed from source. They
have terrible user experience. This list is not exhaustive.

There are actually hierarchies of package managers. There's the uber-package
manager for the whole system. Then there are specialty package managers for a
single programming language, like RubyGems. There are package managers for
implementations of a language, like ruby-build. The uber-package managers
*hate* the specialty package managers because they never respect the
all-important uber-package managers. Users of the specialty package managers
*hate* the uber-package managers for making stupid decisions for a language
they know nothing about. The software authors *hate* everyone because no
package manager correctly uses the software's own build system, which required
tons of effort to make work across platforms.

It is such a stupid and easy problem that everyone thinks they know the best
way to solve it. And they are certain their way is more correct compared to
all the others. Actually, they usually just suck less in one or a few limited
areas.

The solution: *There is no focking solution.* It's like trying to *solve*
religion.

There is only one dismal hope: *Make a thing that works as well as it can in a
crazy world for the few people who will use it.*


## Principles and Assumptions

Just because hope is dim does not require us to abandon the world or suffer
with existing solutions when we can clearly see what rather simple thing would
make our day a bit brighter.

To inform our decisions, a dash of assumptions and a few principles will go a
long way.

Assumptions:

* the user knows that she wants
* the software knows how to build itself
* all software has dependencies

Principles:

* do the fewest number of things
* use the simplest defaults
* do only what the user explicitly requested
* modularize
* isolate
* ask, don't tell

Application of these principles and assumptions should ensure, for instance,
that changing unrelated code doesn't repeatedly break other code. Or that we
never assume when the user requests that we install Ruby that they actually
wanted us to install a new package manager for them. Seriously, what the fock?
Or that we somehow know better than the software authors how to focking build
the focking software.


## Credits

RVM: For what to not ever, ever do.

rbenv: For launching the exodus. You had so much potential.

ruby-build: You had so much potential, too.

chruby: Finally. Simple, useful. And for name inspiration.


## License

BSD. See the LICENSE file.

