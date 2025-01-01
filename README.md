# Linear Programming using Python PuLP
**This repository demonstrates how to use Linear programming using python package called pulp for optimization problem**

     Examining real-world challenges reveals that there are numerous approaches to guiding a problem toward a solution. Some methods may be intricate, while others could be straightforward. The effectiveness of the solution largely hinges on our strategy towards the issue at hand.

Reflecting on my university years, I recall studying heat and mass transfer principles, specifically how the flow of a liquid through a cylindrical pipe is influenced by various parameters. As we consider each factor incrementally, the precision of our understanding of the liquid's flow improves. Initially, we might think about the liquid's density, but further contemplation might lead us to consider its viscosity, boiling point, the type of container it's flowing through, ambient temperature, the friction between the liquid and the container, and the pipe's diameter, which affects its surface area, among other things.

This analogy may seem tangential, but the essence is that being aware of the environmental elements surrounding a problem, and having a thorough understanding of them, can significantly contribute to devising a robust solution.

Similarly, in the software industry, we encounter numerous problems for which various solutions exist. However, the efficiency of a solution often doesn't become a concern until we're forced to optimize for factors like performance, efficiency, and maintenance. I remember encountering a particular challenge some time ago, and that's when I appreciated how **Linear Programming**, which we studied in school, can be incredibly useful in practice. Let's delve into a discussion about that.

#### Linear Programming Overview:

Linear programming is a mathematical approach designed to optimize processes within certain restrictions. Its primary goal is to either increase or decrease a numerical value to its utmost extent. This technique involves linear functions that are constrained by a series of linear equations or inequalities. Linear programming is recognized as a crucial method for achieving optimal resource utilization. Breaking down the term "linear programming," 'linear' refers to the direct proportionality between variables of the first degree. Meanwhile, 'programming' relates to the procedure of choosing the most favorable solution from a set of possible options.

Linear programming has broad applications across various disciplines, including mathematics, as well as in fields like economics, business, telecommunications, and manufacturing. In this discussion, we will explore the concept of linear programming, its key components, and the strategies for solving linear programming challenges.

#### What is Linear Programming:

Linear programming (LP), also referred to as Linear Optimization, is the process of maximizing or minimizing a linear objective function subject to a set of linear constraints, which can take the form of either equalities or inequalities. These optimization problems frequently revolve around computing gains and losses. As a significant category of optimization, linear programming is instrumental in identifying the feasible region—the set of possible solutions—and refining the outcome to achieve the maximum or minimum value of the objective function.

Put simply, linear programming serves as a strategy for optimizing an objective function within a mathematical model, where this function must be either maximized or minimized subject to a collection of constraints expressed through linear relationships. The central purpose of a linear programming problem is to pinpoint the most advantageous solution.

Essentially, linear programming involves assessing various inequalities pertinent to a particular situation and determining the most favorable outcome within those specific parameters.

#### Components of Linear Programming:

***Target Function***: This refers to the specific function that is to be either maximized or minimized. It is commonly a linear function expressed as f(x) = c1x1 + c2x2 + ... + cnxn, where c1, c2, ..., cn represent the coefficients and x1, x2, ..., xn represent the variables involved.

***Decision Variables***: These are the elements we are attempting to solve for. The values of these variables will influence the result of the target function.

***Limitations***: These act as the bounds or caps placed on the variables. They are formulated in a linear manner, either as equations or inequalities—for instance, a1x1 + a2x2 + ... + anxn ≤ b, where a1, a2, ..., an are the coefficients, x1, x2, ..., xn are the decision variables, and b is a fixed value.

***Non-Negative Constraints***: This stipulation mandates that all variables must be non-negative, meaning x1, x2, ..., xn ≥ 0. This is because in many practical scenarios, negative figures do not make logical sense (for example, negative amounts of inventory are impossible).

#### Approaches to Linear Programming:

To resolve linear programming issues, one might employ strategies such as the Simplex method, Graphical techniques (suitable for two-variable scenarios), or Interior Point methods. Additionally, computational tools like Python or specialized software like open solver can be utilized. The objective is to ascertain the set of variable values that will optimize the target function while adhering to all the given limitations.

#### Uses of Linear Programming:

Linear programming has a wide array of applications across different sectors. Here are some typical instances where it is applied:

*Optimizing Resource Utilization*: Companies employ linear programming to efficiently distribute resources like workforce, materials, and machinery to either augment profits or diminish expenses.
*Scheduling Manufacturing Processes*: This method aids in organizing production timelines to ensure optimal employment of factory machinery and workforce while adhering to deadlines.
*Nutritional Planning*: Linear programming is instrumental in creating the most economical dietary plan that meets all nutritional standards, often referred to as the "diet problem" within the field.
*Streamlining Transportation and Logistics*: It is utilized to figure out the most cost-effective strategies for routing and timing deliveries, reducing the expenses associated with transporting goods.
*Managing Network Traffic*: Linear programming is applied to network construction and traffic control to enhance the flow across a network, aiming to reduce blockages or increase capacity.
*Investment Portfolio Management*: In the financial arena, linear programming can be harnessed to amplify returns or minimize risks in an investment portfolio, while observing limitations such as budget or risk preferences.
*Energy Systems Planning*: It is used to strategize and manage energy production and distribution, cutting costs by taking into account variables like consumer demand, fuel prices, and environmental laws.

#### Real-Time Problem Solving:
 
Linear programming can be adapted to solve problems in real-time by using it within decision support tools that take current data as input and provide optimized solutions almost instantaneously. With advances in computational power and algorithms, it is increasingly possible to solve complex linear programming problems in real-time, making it a valuable tool for dynamic and time-sensitive decision-making in industries such as finance, transportation, manufacturing, and energy.

In conclusion, linear programming provides a powerful and flexible framework for modeling and solving optimization problems and can be a critical tool for decision-making in both strategic planning and real-time operational situations.

Let us solve a sample problem using Python Pulp package.https://github.com/coin-or/pulp which is an linear and mixed integer programming modeler written in Python. With PuLP, it is simple to create MILP(Multi Integer Linear Programming)optimisation problems and solve them with the latest open-source (or proprietary) solvers.

Consider the following Problem,

Shilpa has two part-time positions, designated as Job X and Job Y. She is committed to working no more than 12 hours weekly across
both jobs. She has calculated that each hour of work at Job X necessitates 2 hours of prep time, while each hour at Job Y requires
an hour of prep time. Additionally, Shilpa has set a limit of 16 hours for the total preparation time for both jobs.
 
To optimize her earnings, how many hours per week should Shilpa allocate to working at Job X and Job Y, considering she earns $40 per
hour at Job X and $30 per hour at Job Y?
