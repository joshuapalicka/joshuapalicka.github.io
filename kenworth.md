<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-R226D9G6FD"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-R226D9G6FD');
</script>

# CS Senior Capstone Project: Predicting REIs in Kenworth Trucks

### Background
Kenworth Truck Company, a truck manufacturer based in Kirkland, Washington, specializes in medium and heavy-duty trucks. 
As one of the three truck divisions under PACCAR INC, Kenworth provides functionality and flexibility to their customers 
by allowing each truck to be custom-ordered through submitting Option Approval Requests (OARs). This process produces 
unique Bills of Materials (BOMs) for each order, which can lead to the generation of Requests For Engineering Information 
(REIs) when a part cannot be automatically fitted onto the truck. These REIs require an engineer at Kenworth to fit parts 
on a truck. The BOMs are generated based on combinations of sales codes (part numbers) and OARs. With each truck being custom-built, 
there are thousands of combinations, presenting unique challenges for engineers on each order. At the time, there was no 
way to relate what was ordered on the truck to the amount of work that would be required by the engineering team 
to ensure the truck was built on time.

### Project description
My team, which included three other students and me, were paired with Kenworth for our CS Senior Capstone Project. Our 
project explored the relationship between sales codes and OARs in the Kenworth database to build a proof-of-concept 
machine learning model for predicting the number of REIs a given truck would have (which roughly translates to how much 
time an engineer must spend fitting parts onto the truck) based on BOMs and sales codes. The aim was to identify which Sales 
Codes or OARs drove REIs and to provide insights to the Kenworth Data Science team for further development.

### Collaboration
Throughout the project, our team maintained close communication with our sponsor liaisons at Kenworth, meeting virtually 
on a weekly basis. These meetings allowed us to keep them informed about our progress, ask questions, and receive valuable 
feedback to ensure the project's success.

### Tools and Technologies
During the project, we mainly used the following tools and technologies:
* **Snowflake**: for accessing Kenworth's database
* **Pandas**: for data pre-processing
* **Scikit-learn**: for machine learning model development
* **Jupyter Notebook**: for model development and data analysis
* **Tableau**: for data visualization
* **Microsoft Teams**: for communication and collaboration
* **AWS Workspaces**: for secure connection to Kenworth's systems

### Major Deliverables
1. **Entity Relationship Diagram**: We created a data map, which served as the basis of our exploration and allowed us to 
understand the data and how the pieces influenced each other.
2. **Machine Learning Model**: We leveraged Python’s Scikit-Learn library to test many machine learning models, and to 
build our final REI prediction model.
3. **Documentation, Scripts, and Visualization**: We delivered our files, scripts to build the model and predict, and 
documentation of the scripts so that the Kenworth Data Science team could continue this project.

### Outcomes
We deemed this project a success because we were able to predict REIs with an error around 6%. As students, we gained valuable 
experience in real-world applications of data science, machine learning, and Agile methodologies. The Kenworth Engineering Insights
team will continue our work by utilizing our documentation and models to further improve the process and better understand 
the relationship between sales codes and REIs.

<br><br>
<figure>
<a href="images/kenworth-scrum.png?raw=true" target="_blank">
<img src="images/kenworth-scrum.png?raw=true" alt="Project Scrum breakdown"/>
</a>
<figcaption>Project Roadmap</figcaption>
</figure>

<figure>
<br><br><br>
<a href="images/kenworth-predicted-actual.png?raw=true" target="_blank">
<img src="images/kenworth-predicted-actual.png?raw=true" alt="Graph of Predicted vs. Actual REIs"/>
</a>
<figcaption>Predicted REIs (X) vs. Actual REIs (Y) in our final model. Each point denotes a truck order.</figcaption>
</figure>

