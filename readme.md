                               
                                     < A REST-API based on LangGraph, Python and C# >
                                            Dr. Ing. Ashkan Mansouri Yarahmadi

- The C# as GUI, and the LangGraph along with Python as backends were used to design a REST-API product

- The product decides on the amount of discount to be applied on sum amount of purchase appeared on bill

- The sum amount appeared on bill is passed to the Python as backend, where a graph decides on how much percentage is allowed to be applied

A picture of my bill visualized within the designed GUI using C# :

<p align="center">
  <img src="https://github.com/ashkanmy/Insight-Gallery/blob/main/Figs/gui-restapi.png" width="512" height="812">
</p>

Here, total amount of purchased is 9,19 (€). Once the user clicks on "Call LangGraph to get discount ...", the control of the flow will be sent to the Python 
code as backend, where a graph is established using LangGraph seen below :

<p align="center">
  <img src="https://github.com/ashkanmy/Insight-Gallery/blob/main/Figs/graph.png" width="512" height="512">
</p>

The amount on bill, namely 9,19 (€), enters to the "initial node" where it is decided which scheme of discount to be applied. More precisely, the bill 
amount will be compared to a threshold value and based on the outcome, the flow will be sent to either of the two consequetive nodes. Note that, the dotted 
edges represent the condition as part of the graph. Below is the Python code snippet corresponding to the "initial_node".

<div align="center">
    <img src="https://github.com/ashkanmy/Insight-Gallery/blob/main/Figs/EdgeCondition.png" width="1024" height="256" alt="Edge Condition">
</div>

Finally, as 9,19 (€) is less than our threshold values of 20,00 (€). Hence, the appeared "Diescounted sum ( in Euro ) :" (See below) is 8,73 (€) after reduction of 5% discount.

<div align="center">
    <img src="https://github.com/ashkanmy/Insight-Gallery/blob/main/Figs/rewe-discount-bill.png" width="512" height="812" alt="Edge Condition">
</div>

The construction of the graph using LangGraph is shown as below code snippet :

<div align="center">
    <img src="https://github.com/ashkanmy/Insight-Gallery/blob/main/Figs/tree.png" width="512" height="200" alt="Edge Condition">
</div>

#### A short captured video from my monitor running the REST-API can be found here :
https://vimeo.com/1049019449?share=copy


