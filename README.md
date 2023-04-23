# Data-Repository
DATA OVERVIEW
This is the data repository for the case study section of the paper "Distributed Slack-bus Based DC Optimal Power Flow with Transmission Loss: A Second-Order Cone Programming Approach and Sufficient Conditions". The authors established the data repository to enable interested readers to conduct further research based on their studies. The authors compared their proposed method with four existing methods: 1) the ACOPF model; 2) the lossless DCOPF model; 3) the DCOPF-based method in [1], which modeled the transmission loss linearly and adopted the iterative algorithm; and 4) the DCOPF-based methods modeling the nonlinear transmission loss with a single slack bus in [2]. The comparison data came from 13 small systems and 9 large systems from MATPOWER 8.0b[3]-[4], including real-world cases such as the Polish 2383-bus systems. 

DATA FORMAT
For the test systems:
The authors have provided the specific modification results using the standard MATPOWER case format in the folder "Data of Modified Cases". If readers wish to understand the data format of the case studies, they can refer to the MATPOWER User's Manual, which can be downloaded from https://matpower.org/doc/.

For "LMPs calculated by different methods in 22 IEEE test systems"
The data is stored in CSV format and contains locational marginal prices (LMPs) calculated by various methods in 22 IEEE test systems, along with their corresponding meanings.   Specifically, the dataset includes:

\dot LMP: the specific locational marginal price calculated by each method.
\dot Methods: the calculation methods used, including Lossless DCOPF, Method in [18] (corresponding to reference [1] in README), Method in [22] (corresponding to reference [2] in README), Proposed method, and ACOPF. Their detailed explanations can be found in the paper.
\dot Congestion State: whether the tested system is congested. If at least one branch of the system has reached its transmission capacity in the solved state, it is classified as 'Congested', otherwise is classified as 'Non-congested'.
\dot System Scale: indicates whether the system is large or small. We classify systems with 500 or more buses as large, and other systems as small.
\dot Case: indicates the system name of the test.
\dot Bus Number: indicates the number of the bus corresponding to the calculated LMP.



In cases where the transmission capacity of certain branches was not provided, the limit was assumed to be proportional to the total load demand. 





References
[1]	B. Eldridge, R. O'Neill and A. Castillo, "An improved method for the DCOPF with losses," IEEE Trans. Power Syst., vol. 33, no. 4, pp. 3779-3788, Jul. 2018.
[2]	T. Ding, C. Zhao, T. Chen and R. Liu, "Conic programming-based Lagrangian relaxation method for DCOPF with transmission losses and its zero-gap sufficient condition," IEEE Trans. Power Syst., vol. 32, no. 5, pp. 3852-3861, Sept. 2017.
[3]	R. D. Zimmerman, C. E. Murillo-Sánchez and R. J. Thomas, "MATPOWER: steady-state operations, planning, and analysis tools for power systems research and education," IEEE Trans. Power Syst., vol. 26, no. 1, pp. 12-19, Feb. 2011.
[4]	C. Josz, S. Fliscounakis, J. Maeght, et al, “AC Power Flow Data in Matpower and QCQP Format: iTesla, RTE Snapshots, and PEGASE.” [Online] Available: https://doi.org/10.48550/arXiv.1603.01533.
