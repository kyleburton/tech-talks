Introducing (`bake`)[https://github.com/kyleburton/bake]

Overview

About Your Presenter

My Journey With Build and Automation Tools

* wtf's a buidl tool?
* make: wow, this is awesome! (o'reilly book cover shot here)
    expressive; built in; felt great
    larger project, recursive makefiles; not so great
    oh fuck, whitespace is a thing
    shell escaping hell
* autotools: (automake, autoconf) wow: powerful for cross platform, wow: overwhelming complexity, M4?
* dynamic languages time, lesser need for builds, automation?  these languages were great for automation
* ohai Java
  * recursive makefiles & make pattern rules would invoke `javac` over and over
  * killer for performance, non-starter
  * ohai `ant`
    * no commonly accepted standards or conventions for projects -> inconsistency
    * lots of manual
  * ohai `mvn`
    * where the f@*% do I put things?
    * wtf's a life cycle?
    * holy mother of dependencies!  &lt;-- a killer feature IMO
    * zen of maven: flow with the river, aka just follow the conventions everyone will be happier
    * consistency lead to lots of easily leveragable features
    * became defacto standard
* best so far: `mvn` but it sucks for anything but java
* I'm working outside of the Java on the JVM for a while (Ruby, JavaScript front-ends, starting on DevOps)
* Ruby: `rake`, `capistrano`, `mina`, `chef` such a wonderful DSL and set of tools/framework
  * compared to what came before these were f.u.n.
  * 'heavy man'; to ruby 2.0 or not to ruby 2.0?; oh crap rake isn't quite compatible with all the versions of ruby
* I start using Go
  * Hrm, can I do this in Go?
  * spike: `grake`
    * whoah, hello fast, I've missed you so!
    * tried to get close to Ruby's Rake DSL, kinda worked
    * hard to make automagic
    * distribution not so great: requires the full go build tooling to be installed
    * on the fly code generaion, compilation & execution was a bit error prone
    * this tool doesn't really do it for me
* inspired question: can I just do this in bash?
  * Can I do this w/no dependencies?  (languages, libraries)
  * What am I really trying to solve for here?
    * factoring
    * re-use of code/libraries
    * minimize accidental complexity, how close can we get to Ruby's Rake DSL?

Hello Bake!


Bake: why?

Bake: what have I leanred?

 * like: no dependencies over putting `bake` on your `$PATH`
 * like: re-use achieved
 * like: I have a way of doing 'batteries included'

Bake: gotchas, pitas

* commands w/the same name
