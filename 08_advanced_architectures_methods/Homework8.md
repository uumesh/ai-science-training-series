# Homework

## Submit a paragraph about:

How could you use AI for a problem that interests you?
What is the task?
What kind of data would you use?
What kind of method or model might be appropriate?
What kind of metric would you use to measure success?

## Response
I am interested to use AI to solve chemical kinetics and its evolution in a fluid flow system. For complex chemical species, the chemical kinetics are often too elaborate and numerical solution of the reaction system pose several challenges such as numerical stiffness (due to wide differences in reaction time scales of different species), computational expense (computation scales as O(N^2) or O(N^3) ). Therefore, CFD of reacting flow systems often resort to simplified chemical kinetic mechanisms that lead to uncertainties with respect to the fidelity of the numerical solution. The use of AI could potentially alleviate this by providing a surrogate model for the reaction kinetics occuring in the system.

Data from simpler 0D and 1D system simulations could be used to learn AI models. Datasets for these simplistic systems can be easily generated through chemical solvers without the full 3D CFD solver. These are also faster to solve and therefore, large datasets can be generated for training in a shorter period of time. As a first attempt, a fully connected deep neural network might be a model of choice. However, given the number of input variables (number of species) the cost of the final model might be large. Theoretically, since chemical reactions occur within pairs of chemical species, a portion of the dense connections could be avoided leading to something like a sparsely connected neural network. (I am yet to explore how this could be learnt from data). The metric to measure success of the model would be to measure the accuracy of the trained model at diverse temperature/pressure conditions that was not used in the training phase.
