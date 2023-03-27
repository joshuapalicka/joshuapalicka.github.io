<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-R226D9G6FD"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-R226D9G6FD');
</script>

# Graduate Research Project: Sugarscape-Utilicalc

### Project description
The main goal for this project was to use our comprehensive Python implementation of Sugarscape, described [here](./sugarscape.md),
as a framework for implementing Utilitarian ethics using Jeremy Bentham's formula for Felicific Calculus, programmatically.
For this, we created Utilicalc, [link](https://github.com/joshuapalicka/utilicalc/), an implementation of Bentham's formula, 
which is a framework of classes for which to input the outcomes of potential actions an agent can make, and get an output 
of the moral value of those actions, which we use to decide agent moves in the Sugarscape.

### Background
Felicific Calculus quantifies the moral value of an action based on the consequences for all actors involved. The algorithm
considers various factors, such as intensity, duration, certainty, nearness in time, and others, to determine the overall
positive or negative impact of an action.

Background on the Sugarscape, as well as our implementation, is given [here](./sugarscape.md).

### Outcomes
We find that some heuristics of a healthy Sugarscape society, such as carrying capacity of the environment, are increased
when using Utilitarian Calculus for decision-making, rather than the default greedy algorithm that Sugarscape uses.
We are currently writing an academic paper on this work, and expect to publish it by the end of 2023. Through this project,
we successfully transformed a theoretical algorithm into functional code, showcasing our ability to adapt and apply theoretical 
concepts into practical programming solutions.

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
<figcaption>Snapshot of a Sugarscape run with sugar and spice, including optional stats and a graph</figcaption>
</figure>