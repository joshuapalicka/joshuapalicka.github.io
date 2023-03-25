## Sugarscape

### Project description
A comprehensive Python implementation of Joshua M. Epstein and Robert Axtell's agent-based simulation: Sugarscape, as 
detailed in their book "Growing Artificial Societies: Social Science from the Bottom Up". 

### Background
The Sugarscape is designed to simulate social interactions and economic activities among agents within an artificial environment. 
The Sugarscape itself is a two-dimensional grid representing a landscape with "sugar" and "spice" resources that vary 
in distribution and quantity. In this model, agents are autonomous entities with unique characteristics, such as vision, 
metabolism, and wealth. They navigate the Sugarscape by moving to nearby cells and collecting resources to increase their 
wealth, which they consume to stay alive. Agents can also reproduce, creating new agents with inherited traits. The Sugarscape 
model allows researchers to explore various social phenomena, such as population growth, migration, trade, cultural transmission, 
and the emergence of social behavior, by observing the interactions that these agents have with the environment and other
agents around them.

### Goals
The main goal for this project was to implement the Sugarscape and all of its rules and interactions, which are described in
"Growing Artificial Societies". We wanted to do this because we deemed the Sugarscape a solid building-block for another 
project, which was to implement Utilitarian ethics using Jeremy Bentham's formula for Felicific Calculus, programmatically - [link](https://github.com/joshuapalicka/sugarscape-utilicalc).

Although other implementations of Sugarscape exist in other languages, another goal was to make Sugarscape accessible. 
For this reason, we built upon and updated a previous, incomplete Python 2 implementation of Sugarscape - [link](https://github.com/langerv/sugarscape). 
We chose this language because it is extremely accessible, and easy to work with. This previous version used Pygame for 
rendering the Sugarscape world. To remove this dependency, we rewrote the code to use  Tkinter, a Python standard library 
package. The only non-standard library dependency for the project is matplotlib, which is used for graphing Sugarscape 
statistics during program runtime.

### Outcomes
We were successful in reproducing Sugarscape. Although there is not enough detail given in the book for an exact copy,
we are able to reproduce many of the results from the book, and it worked well for us in our ethics project. I gained
skills in project management, working with constraints, performance optimization, communication, and collaborative problem-solving

<br><br>
<figure>
<a href="images/sugarscape-sugar-graphs.png?raw=true" target="_blank">
<img src="images/sugarscape-sugar-graphs.png?raw=true" alt="Snapshot of Basic Sugarscape run with optional location stats and mean trade volume graph"/>
</a>
<figcaption>Snapshot of a basic Sugarscape run including optional stats and a graph.</figcaption>
</figure>

<figure>
<br><br><br>
<a href="images/sugarscape-sugar-spice-graphs.png?raw=true" target="_blank">
<img src="images/sugarscape-sugar-spice-graphs.png?raw=true" alt="Standard Sugar and Spice Sugarscape run with optional location stats and mean trade volume graph"/>
</a>
<figcaption>Snapshot of a Sugarscape run with Sugar and Spice, including optional stats and a graph</figcaption>
</figure>