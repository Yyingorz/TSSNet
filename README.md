TSSNet

All codes and cases are available for free after publication.

================

What about this project/study?

      
The integration of renewable energy resources (RESs) into energy systems presents significant operational 
challenges due to their intermittent and stochastic nature. Microgrids (MGs) offer a compelling alternative 
for reliable accommodation of various RESs. However, multiple uncertainties, caused by the introduction of 
multi-RESs and load fluctuations, complicates the operation of MGs. To address this issue, we introduce TSSNet, 
an innovative neural network-based two-stage stochastic programming framework for grid-connected MG operation. 
Firstly, we developed an autoencoder to generate a compact representation across the scenario sets, enabling 
TSSNet to handle any number of scenarios. Then, a novel sampling approach is proposed to assist TSSNet in 
accurately capturing the policy between the two stages. Consequently, TSSNet can efficiently address multiple 
uncertainties, alleviating the dependency between problem scale and scenarios, and achieving near-optimal 
solutions rapidly. Simulations in three different cases validate TSSNet's flexibility and effectiveness in
various practical settings.


User Guide
-----------

The description of implement code files 

    TSSP_tranditional : optimizing the original two-stage stochastic programming problem to gather ground truth.
    
    data_generation : randomly generating solutions and plugging into TSSP problem to gather infeasible (mainly) solutions.
   
    TSSP_train :  training a neural network based on the data from the first step, saving the parameters of trained NNT.
    
    TSSP_reformualtion :  convert the trained NNT to pyomo model, combining with the first stage problem, then optimizing this TSSNet problem.
    
    net_params_caseA/B/C.pkl :  store parameters of the trained network for case A/B/C.
    
    case_A/B/C_data :  store all training datasets for case A/B/C.
    
    Wind_power : Historal wind data.

    PV_power : Historal photovaltaic data.

    mydatatypes: define the data structure used in this project.

    Readdata: read the case setting from the file.
    
    ReadRes: read renewable data from file.

Prerequisite:
-----------
    Python                       3.11.5
    Julia                        1.10.4
    tensorflow                   2.12.0
    Pyomo                        6.7.3
    omlt                         1.1
    gurobipy                     11.0.2


Publication:
-----------
    If you find our paper/code is useful to you, please cite it.




About Us 
-----------
    Authors：Ying Yang (yingyoung1997@gmail.com), Yankai Cao(yankai.cao@ubc.ca), Lingfeng Yang (ylf@gxu.edu.cn), Arka Ian Goswami
    Webpage: https://optimal.chbe.ubc.ca
