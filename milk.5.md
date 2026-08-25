Chemical Industry & Chemical Engineering Quarterly
Available on line at
Association of the Chemical Engineers of SerbiaAChE
www.ache.org.rs/CICEQ
Chem. Ind. Chem. Eng. Q. 25 (4) 369−382 (2019) CI&CEQ
369
MANUELA SOUZA LEITE
MATHEUS A. SANTOS
EULINA M. F. COSTA
ACENINI BALIEIRO
ÁLVARO S. LIMA
ODELSIA L. SANCHEZ
CLEIDE M. F. SOARES
Tiradentes University, Institute of
Technology Research, Farolândia,
Aracaju, Sergipe, Brazil
SCIENTIFIC PAPER
UDC 66.081.3:637.12.047:004.8
### MODELING OF MILK LACTOSE REMOVAL BY
### COLUMN ADSORPTION USING ARTIFICIAL
### NEURAL NETWORKS: MLP AND RBF
Article Highlights
• Mathematical models are proposed for the removal of lactose from milk
• Multilayer perceptron and radial basis function neural networks are applied
• Neural models (MLP and RBF) were developed to predict breakthrough curves
• The operational parameters were evaluated for lactose adsorption capacity
• The models effectively predicted the breakthrough curves under various conditions
Abstract
Artificial neural network (ANN) techniques are effective in modeling nonlinear
processes, are simple to implement and require low computational time. In this
work, the lactose adsorption process for continuous flow in a fixed-bed column
with a molecularly imprinted polymer (MIP) adsorbent was modeled using an
ANN technique. The neural models allowed predicting the relative lactose con-
centration (C/C0) from the interactions between the variables of contact time
(min), temperature (°C), granulometry (mesh), bed height (cm) and flow rate
(mL min
-1
). The ANN models were developed in MATLAB using multilayer
perceptrons (MLP) and a radial basis function network (RBF). The MLP model
was developed using a three-layer feed forward backpropagation network with
5, 8 and 4 neurons in the first, second and third layer, respectively. The
function (RBF) network is also proposed and its performance is compared to a
traditional network type. The best architecture configuration RBF model was
developed using 5, 14 and 1 neurons in the first, second and third layer, res-
pectively. The proposal of development of mathematical models applied to
multi-component adsorption system for milk using these approaches is inno-
vative. The resulting breakthrough curve models for lactose adsorption were in
good agreement with the experimental results. Performance indices, such as
R², MSE, RMSE, SSE, MAE and RME were used to evaluate the reliabilities
and accuracies of the models. A comparison between the ANN models shows
the ability to predict the breakthrough curves of lactose removal in the milk
adsorption process. Though, the MLP network model shows more accurately a
higher correlation coefficient (R
2 
= 0.9751) and lower values for the obtained
error indices. The accuracy of the model is confirmed by the comparison
between the predicted and experimental data. The results showed that both
neural models efficiently described the non-linear process of lactose ads-
orption in a fixed-bed column.
Keywords: ANN, MLP, RBF, fixed-bed column, lactose, breakthrough
curves modeling.
Correspondence: M.S. Leite, Tiradentes University, Institute of Technology Research, Av. Murilo Dantas, 300, Farolândia, 49032-490
Aracaju, Sergipe, Brazil.
E-mail: sl.manuela@gmail.com
Paper received: 6 June, 2018
Paper revised: 13 November, 2018
Paper accepted: 9 April, 2019
https://doi.org/10.2298/CICEQ180606015L

---

M.S. LEITEet al.: MODELING OF MILK LACTOSE REMOVAL… Chem. Ind. Chem. Eng. Q. 25 (4) 369−382 (2019)
370
Lactose is the major carbohydrate in the milk of
most species, in addition to other components such
as moisture, protein(s), fat, mineral and lactic acid [1].
However, the consumption of milk as an energy
source is limited by the relatively high percentage of
people who are unable to digest lactose [2]. The
possibilities of lactose removal techniques from milk
are applied to offer the customers products with
reduced lactose content. Among these, it is possible
to highlight the process of milk lactose removal by
adsorption. This versatile and widely used method
has the ability to separate diverse types of chemical
compounds using simple operating procedures [3,4].
Its practical application is generally performed in a
fixed-bed column [5]. In this separation system, the
adsorption rates are favored because the adsorbent
is continuously in contact with the solution [6]. The
adsorbent efficiency can be improved by using the
molecular imprinting technique to obtain molecularly
printed polymers (MIP). The main advantage that
MIPs have over the conventional materials used in
extraction in the solid phase, is their molecular speci-
ficity [7]. Balieiroet al. [8] and Oliveiraet al. [9] stu-
died the adsorption process of molecularly imprinted
silica in a fixed-bed column with continuous flow, for
the extraction of lactose and cholesterol from milk,
respectively.
Some studies have used phenomenological
models to describe the adsorption mechanism [8-15].
In addition to the phenomenological models, the lite-
rature abounds with studies that use empirical models
developed using artificial neural network (ANN) tech-
niques, to obtain a model that best describes various
adsorption processes [9,11,16-22]. However, public-
ations with mathematical modeling for milk adsorption
systems are incipient.
The ANN has three layers including an input
layer, one or more hidden layers, and an output layer.
For each ANN, the input layers are composed of inde-
pendent variables and the output layer by dependent
variables. The input and output layers are intercon-
nected by intermediate layers, with multiple neurons.
Each neuron sums all the inputs it receives and con-
verts the sum to an output value based on a pre-
defined activation or the transfer function [23,24].
Neural networks have been successfully used in
multivariate and nonlinear systems and ANNs are
promising modeling techniques for multicomponent
processes [25-32]. Thus, an ANN approach was emp-
loyed by the authors to explore its potential applic-
ation in a multi-component sample, such as milk, with
specific emphasis on the adsorption of lactose. The
modeling of the adsorption process can be performed
by various types of architectures, such as multilayer
perceptron (MLP), as seen in the work of Oliveiraet
al. [9], Sargolzaeet al. [28] and Razaviet al. [29]; and
by networks with radial basis functions (RBF), such
as in the work of Hassanzadehet al. [18] and Solei-
maniet al. [33]. Oliveiraet al. [9] modeled the process
of cholesterol removal from milk in a continuous flow
adsorption column with a MIP adsorbent using ANN
models. In that study, the Levenberg–Marquardt
training algorithm for MLP was developed and a satis-
factory prediction of the experimental data was
obtained because it presented an efficient perform-
ance. Also, in the work of Sargolzaeet al. [28] the
effectiveness of ultrafiltration milk modeling has been
assessed using an MLP. The modeling results reveal
that ANN modeling also has a high ability in simul-
ating the dynamic behavior of permeate flux, total
hydraulic resistance using temperature and time as
the input parameters in the modeling of ultrafiltration
processes. Razaviet al. [29] also investigated the
neural network approach to predict complete perme-
ate flux, total hydraulic resistance and solutes reject-
ion during crossflow ultrafiltration of skim milk as a
function of the transmembrane pressure and tempe-
rature and to specify the role of these factors on the
mechanisms of flux, fouling and retention. The
authors concluded that the neural networks can be
successfully used to predict the milk ultrafiltration per-
formance.
However, there is no prior publication dealing
with ANN or other models to predict the breakthrough
curves of lactose for this system. In particular, the
modeling of lactose is challenging due to the com-
plexity of the physical interactions in a highly non-
linear water-in-oil emulsion (milk). In this context, the
present work aimed to investigate the capability of
two neural model types (MLP and RBF) in predicting
the breakthrough curves of milk lactose by a column
adsorption process with continuous flow, from the
effects of parameters including contact time (min),
temperature (°C), granulometry (mesh), bed height
(cm) and flow rate (ml min
-1
). Explanations of the
simulated results, from the models and the predicted
ANN results are presented.
MATERIALS AND METHODS
Milk and reagents
The bovine milk was packaged in plastic bags,
conditioned under refrigeration in thermal boxes and
transported to the Food Research Laboratory (LPA) of
the Institute of Technology and Research (ITP), 112
km from the collection point, where they were frozen
(-20 °C) until use.

---

M.S. LEITEet al.: MODELING OF MILK LACTOSE REMOVAL… Chem. Ind. Chem. Eng. Q. 25 (4) 369−382 (2019)
371
The reagents used in this study were tetra-ethyl
ortho-silicate (98%), lactose (purity >99%), acetonit-
rile (99.9%), hexane (65%), hydrogen peroxide (32%),
sodium hydroxide (97%), hydrochloric acid (37%),
ammonium hydroxide (30%), chloroform (99.8%) and
ethanol (99.8%) and were all analytical grade.
Preparation of the adsorbent and analytical
determination of lactose
The preparation of the adsorbent and the ana-
lytical determination of the lactose were performed as
described by Balieiroet al. [8]. The adsorbent was
prepared using the sol-gel process and tetraethoxy-
silane (TEOS) as raw material. For molecularly imp-
rinted polymer (MIP-lac) adsorbent the TEOS and the
target molecule (lactose) were dissolved in ethanol.
The steps were as follows: pre-hydrolysis, hydrolysis,
solid material synthesis through gelation for 18 h, ext-
raction (washing) and drying at 277.2 K.
The calibration curve and measurement of lac-
tose were performed by high performance liquid chro-
matography (HPLC) using a liquid chromatography
(Shimadzu), with refractive index detector (RID-10A)
and software (LC-Solution) for the location of the
data. The concentration of the standard solution of
lactose ranged from 30 to 300 ppm. For processing
the data, the analytical column used was a Luna NH2
(250 mm×4.6 mm) (Phenomenex). The mobile phase
consisted of acetonitrile and ultrapure water (60:40) at
a flow rate of 1.5 mL min
-1
, with an analysis time of 10
min. For the determination of lactose from milk
samples: 30 μL samples were diluted in a 2 mL volu-
metric flask in ultrapure water and then the samples
were filtered through a 0.45 Millipore membrane and
subsequently injected into the equipment [8].
Adsorption column experimental method
Balieiroet al. [8] studied the effect of operational
variables on the adsorption of lactose in the packed
column by a fractional factorial design (2
4-1
) with four
independent variables (flow rate, temperature, granu-
lometry and bed height) and adsorption capacity as
dependent variable. The experimental variables and
its levels are shown in Table 1. The experiments (with
four replicates) for the removal of lactose were per-
formed following the experimental design presented
in Table 2.
Table 2. Experimental plan
Exp. test
TGHQ
(°C) (mEsh) (cm) (mL min
-1
)
1 - + - -
2 + + - +
3 - - - +
4 + - - -
5 - + + +
6 + + + +
7 - - + -
8 + - + +
9 0 0 0 0
10 0 0 0 0
11 0 0 0 0
12 0 0 0 0
Initially, the column was filled with the MIP ads-
orbent and then the adsorbent was hydrated for 30
min with deionized water. Next, the milk was fed
downwards into the column by a peristaltic pump
using the flow rates corresponding to the experimen-
tal design. A thermostatic bath was used to maintain
the column at a constant temperature by recirculating
the water in the system. The milk flow scheme is
schematically represented in Figure 1.
Figure 1. Schematic diagram of experimental unit for lactose
removal.
Throughout the experimental tests, samples
were collected from the base of the column at random
time intervals. These collections were performed until
the system reached equilibrium. The samples were
analyzed by HPLC to quantify the lactose concen-
trations. From the relative lactose concentration
(C/C0) data as a function of time, experimental break-
through curves were constructed to analyze the influ-
ence of the process variables. Then, to evaluate the
Table 1. Levels of experimental factors (codified and uncoded
values)
Operating variable -1 0 +1
X1 (temperature, K) 307.1 320.1 333.1
X2 (particle size, mesh) 32 42 60
X3 (bed height, cm) 7.5 10.0 12.5
X4 (flow rate, mL.min
-1
) 3 6 9

---

M.S. LEITEet al.: MODELING OF MILK LACTOSE REMOVAL… Chem. Ind. Chem. Eng. Q. 25 (4) 369−382 (2019)
372
ideal operating conditions, the adsorption capacity
(qo) for each test was calculated by Eq. (1) and the
results expressed as milligrams of lactose per gram of
adsorbent [8]:
2t 
00 0
0 00 0
d 
4C
mVC VC qCD
tH
CC
επ− 
= +
##  
(1)
whereV is the flow rate (mL min
-1
),ε is the porosity of
the bed,D is the particle diameter,H is the height of
the particle.C0 is the initial concentration (mg mL
-1
),C
is the concentration at the exit (mg mL
-1
) from the
bed, andm is the mass of the adsorbent (g).
Artificial neural network (ANN)
Characteristics of ANN models
ANN techniques have been used to develop
nonlinear models. The number of ideal neurons in the
hidden layer is optimized through a learning proce-
dure and its output layer provides the results of the
processed information. The performance of the net-
work is influenced by the selection of the appropriate
number of hidden neurons and the transfer functions
[24]. The connection between the neurons in separate
layers is defined in terms of weights and bias, as
shown in Figure 2. The activation of the neuron (Ωj) is
given by Eq. (2):
( )
i
jj i j
i
W x βΩ = +
##  
(2)
Figure 2. Schematic representation of a single neuron with “n”
inputs and of ANN structure in a feedforward network.
whereW
i
j represents the weight binding of neuroni to
neuronj,xi is the input of neuroni, andβj is the
deviation of neuronj.
In the MLP model, the following transfer func-
tions can be used: pure linear activation function
(purelin), hyperbolic tangent sigmoid (tansig) and
logarithmic sigmoid (logsig). These are represented
by the equations given in Table 3. The linear function
is generally used in the output layer. Logsig is a non-
linear and limited function between 0 and 1, and
tansig is delimited between -1 and +1. These func-
tions are often used in engineering applications in
process description [24–26,33,34].
Table 3. Typical transfer functions of the MLP model and their
respective equations
Transfer function Equation
Linear ( )y x x=
Sigmoidal logarithm (Sig. log.) 
( ) 
1
1
x
y x 
e 
−
= 
+
Hyperbolic tangential sigmoid
(Hyp. tang. sig.)
2
( ) 2 / (1 ) 1
x
y xe 
−
= + −
The RBF model can also be applied to various
tasks due to its high efficiency, speed, and simplicity.
It is easy to learn because there are few parameters
to be optimized, which include the constant spread of
the radial basis function and the number of neurons in
the hidden layer. Each layer of an RBF network can
have any number of neurons, but more neurons may
be required in the hidden layer than the MLP model
[23,36]. Furthermore, unlike the MLP networks, which
have sigmoid functions, the RBF networks have radial
basis functions in the middle layer. The radial basis
transfer function is presented in Eq. (3):
2
( )
x
y x e 
−
= (3)
Development of ANN models
The ANN models in this work were developed in
MATLAB software (R2015a) for MLP and RBF archi-
tectures. This research was conducted according to
the sequence of steps illustrated in Figure 2. The top-
ology of the MLP model was evaluated to determine
the ideal architecture,i.e., the number of neurons
required in the hidden layer, the transfer functions
and the training algorithm, which provide the best
result. The number of epochs, the learning rate, and
the objective error remained unchanged. The RBF
model has no change in its transfer function. The
constant spread (width of the radial basis functions)
and the number of neurons were investigated to achieve
the combination that provided the best response.

---

M.S. LEITEet al.: MODELING OF MILK LACTOSE REMOVAL… Chem. Ind. Chem. Eng. Q. 25 (4) 369−382 (2019)
373
The database was constructed from experimen-
tal data and the contact time (min) temperature (°C)
granulometry (mesh) bed height (cm) and flow rate
(ml min
-1
) were defined as the input variables for the
ANN model. The relative concentration (C/C0) was
selected as the output parameter of the ANN model.
The initial structure of the network is shown in Figure 3.
A total of 249 data were used, which were shuf-
fled and divided into three groups: 70% for training,
15% for validation and 15% for testing. Table 4 shows
the minimum and maximum values for each set,
where the test and validation ranges are contained
within the training range. The origin of the conver-
gence problem lies in the use of denormalized experi-
mental input data to the model [33] so, for the con-
duction of the learning process, the database was
normalized in a range of -1 to 1.
In order to find the ideal topology of the models,
we compared some performance indices, which mea-
sure the efficiency of ANN prediction, such as the
coefficient of determination (R
2
), mean square error
(MSE), root of the mean square error (RMSE), sum of
the squared error (SSE), mean absolute error (MAE)
and relative mean error (RME), which are defined in
Eqs. (4)–(9), respectively, whereti is the experimental
value,pi is the predicted value,N is the data number,
tm is the mean of the experimental values, andpm is
the mean of the predicted values:
2
2 1
2
1
( )
1
( )
N 
i i
i
N 
i m
i
pt
R 
t t
=
=
−
= − 
## 
##  ## − 
(4)
2
1
( )
N 
i i
i
pt
MSE 
N
= 
−
= 
##  
(5)
2
1
( )
N 
i i
i
pt
RMSE 
N
= 
−
= 
##  
(6)
Figure 3. Structure of the constructed neural network (MLP and RBF).
Table 4. Experimental ranges of the input and output variables for training, validation, and testing
Variable 
Training Validation Test
Min. Max. Min. Max. Min. Max.
Input Time (min) 1.5 40 2 40 2 30
Temperature (°C) 34 60 34 60 34 60
Granulomety (mesh) 32 60 32 60 32 60
Bed height (cm) 7.5 12.5 7.5 12.5 7.5 12.5
Flow rate (ml min
-1
) 3 9 3 9 3 9
OutputC/C0 0.0077 1.1951 0.0069 1.0855 0.0085 1.0951

---

M.S. LEITEet al.: MODELING OF MILK LACTOSE REMOVAL… Chem. Ind. Chem. Eng. Q. 25 (4) 369−382 (2019)
374
2
1
( )
N 
i m
i
SSEpt
= 
−= 
##  
(7)
1
1N 
i i
i
MAEpt
N =
= −
##  
(8)
1
100N i i
i 
i
pt
RME 
Np
=
−
= 
##  
(9)
TheR² is a statistical measure of how well the
regression line approximates the predicted points to
the real data. AnR² equal to 1, indicates that the
regression line fits perfectly to the data [22]. TheMSE
measures the sum of the squared difference between
the network output and the experimental value divided
by the number of data. When theMSE approaches
zero, it indicates that the model error is minimal. The
RMSE is the square root of theMSE. The lower the
value ofRMSE, the better the model performance
[23]. TheSSE is the sum of the squared difference
between the experimental data and the mean of the
predicted data. The MAE is a quantity used to mea-
sure how close predictions are to the eventual out-
comes. TheMAE describes the average magnitude of
the errors, regardless of their signal.MAE values
range from zero to ∞, where smaller values are better
[23,36]. TheRME values are the mean of the relative
errors in percentage and are obtained by dividing the
difference between the experimental data and that
predicted by the model by the predicted value.
Relative importance of variables in lactose removal
process
The relative importance of the process variables
is the contribution of each of the variables in pre-
dicting the dependent variable. In the quantification of
the relative importance of the independent variables,
used in the prediction of the output variable of the
neural network, a method referred to as connection
weights (CWs) was used. The CWs algorithm calcul-
ates the sum of the products between the weights of
the input layer for each intermediate and the final
CWs of the hidden neurons to the output layer [36].
The relative importance of a given input variable can
be defined by Eq. (10):
1
1 1
m 
xy yz
y
xnm 
xy yz
xy
w w
RI
w w
=
= =
= 
## 
##  ##  
(10)
whereRIx is the relative importance of the input
neuronx, 
1
m 
xy yz
y 
w w
=###  
is the sum of the product
between the weights of input layers for hidden layers
and the weights of hidden layers for output layers,y is
the total number of hidden neurons,z is the number
of output neurons, and 
1 1
nm 
xy yz
xy 
w w
= =###  ###  
is the total
sum of the products among the weights. This
approach is based on estimates of the net weights
obtained by network generation [36]. It is observed
that these estimates of the final weights can vary with
the change in initial weights used to start the training
process.
RESULTS AND DISCUSSION
Optimization of ANN structure
The MLP model was developed with feedfor-
ward architecture. Initially, the number of neurons in
the intermediate layer was determined and, as a cri-
terion of choice, its validation MSE was analyzed. The
Levenberg–Marquardt training algorithm, andtansig
between the input layer and the intermediate layer,
andpurelin for the output layer were initially retained.
A three-layer ANN, an input layer with 5 neurons
(contact time, temperature, granulometry, bed height
and flow rate), a hidden layer with 8 neurons and an
output layer with 1 neuron (5-8-1), is established. Fig-
ure 4a shows the relation between the number of
neurons andMSE for the selected ANN model and
confirms that the construction of the model containing
eight hidden neurons permits the accurate, repeat-
able and predictive behavior of lactose adsorption
(minimumMSE of 0.0217).
When the number of neurons in the hidden layer
is much greater than necessary, a problem called
over-fitting may occur. This phenomenon refers to the
reduction in generalization ability that can occur as
networks are trained, and it must be avoided
[23,28,29,36]. In contrast, an insufficient number of
neurons in the hidden layer implies another problem
called under-fitting, which is the incompetence of the
neural network to solve the addressed process,
namely, the model has a complexity inferior to the
problem [9,18,19,21,38]. Thus, to avoid these prob-
lems occurring in the performance of the production
of relative concentration (C/C0), the cross-validation
technique was used. Figure 4a shows the results
obtained and verify that there was no over-fitting
because the validationMSE did not increase relative
to the training and testMSE. This decrease in the
validation error also indicates an obtained model with
generalization capacity of the network.
The effect of the transfer functions on the per-
formance of the model was evaluated based on the
comparison between the trainingR² results, validation
and test, and the validationMSE. These results are
presented in Table 5 for each combination of the
transfer functions in the input and intermediate layers.

---

M.S. LEITEet al.: MODELING OF MILK LACTOSE REMOVAL… Chem. Ind. Chem. Eng. Q. 25 (4) 369−382 (2019)
375
Among the results, the ANN-5 model, with
tansig between the two layers, provided the best
values forR² andMSE, giving the better correlation
between the model data and the experimental data.
Different training algorithms were also analyzed based
onMSE andR², in addition to considering the number
of epochs and their interactions. Table 6 presents the
results for the various types of model algorithms.
The Levenberg–Marquardt algorithm provided
the best performance indices, with fewer times and
interactions, as observed by Maghsoudiet al. [3] and
Kunduet al. [34]. By finding the ideal parameters of
the network architecture, the training was interrupted
and the weights and bias used to generate the MLP
model are presented in Table 7.
Figure 4. a) Effect of neuron number in the hidden layer and Performance of the MLP model (5-8-1) in the training phase
(MSE = 0.021677 after 14 epochs). b) Effect of neuron number in the hidden layer and training MSE results used to evaluate
the ideal spread constant of the RBF model.
Table 5. Determination of the transfer functions for the MLP model with eight neurons in the hidden layer
Model Transfer function 1 Transfer function 2 TrainingR² ValidationR² TestR²MSE of validation
ANN-1 Sig. log. Hyp. tang. sig. 0.9572 0.9624 0.9543 0.0223
ANN-2 Hyp. tang. sig. Linear 0.9514 0.9604 0.9462 0.0316
ANN-3 Sig. log. Linear 0.9583 0.9619 0.9513 0.0293
ANN-4 Hyp. tang. sig. Sig. log. 0.8801 0.9081 0.9551 0.4676
ANN-5 Hyp. tang. sig. Hyp. tang. sig. 0.9607 0.9711 0.9693 0.0217
ANN-6 Sig. log. Sig. log. 0.8419 0.8936 0.9268 0.4693
ANN-7 Linear Sig. log. 0.6542 0.6803 0.6949 0.4932
ANN-8 Linear Linear 0.8289 0.8219 0.8454 0.1215
ANN-9 Linear Hyp. tang. sig. 0.9062 0.9025 0.9551 0.0891

---

M.S. LEITEet al.: MODELING OF MILK LACTOSE REMOVAL… Chem. Ind. Chem. Eng. Q. 25 (4) 369−382 (2019)
376
The general formula of the MLP model for the
calculation of the prediction is described in Eq. (11):
## ( ## )
2
22 12
2 
1
1
2 
1
1
x
jij ijjx
MLP 
e
bbwx w
e
−
−
 
= − ×
 
+ 
  
× + − +  
+  
## 
(11)
The RBF model was constructed using the
same database as the MLP model. Initially, the RBF
model was trained with 30 neurons and its objective
error was the smallest possible, so its constant
spread was determined according to the evaluation of
the smallestMSE generated.
Figure 4b shows the data of the constant spread
determination step relative to the trainingMSE. It is
observed that an adequate spread constant was 0.2.
Figure 4b shows the behavior of theMSE decrease
and the number of neurons during optimization of the
RBF model. It was verified that the increase in the
number of neurons directly influenced the perform-
ance of the model and that after 14 neurons, the
performance of the model did not change signific-
antly. After obtaining the ideal structure of the RBF
network (5-14-1), the training step was completed.
Thus, its weights and bias are shown in Table 8. Eq.
(12) is a general formula of the RBF model:
# ( # ) ( ## )
22
22 1
s
jij ijj
sRBF e bebwx w
−
  
−= + +  
  
##  
(12)
In order to compare the quality of the production
between the two models of ANNs, a test was per-
formed with 30% of the database that is not included
in the training stage. Figure 5 shows the regression
plots for the MLP and RBF models, respectively.
The MLP model presented aR² higher than the
RBF model, indicating a better approximation in its
prediction.
Efficiency of lactose removal and influence of process
variables
According to Table 9, the bed height in the
studied range expressed the greatest significant influ-
ence on the process, whereas the temperature was
the variable of least influence.
Table 6. Optimization of training algorithms
Training algorithm TrainingR² (70%) ValidationR² (15%) TestR² (15%)MSE of validation Epoch Iterations
Gradient descent backpropagation 0.5424 0.5203 0.3183 0.283 1000 1000
Gradient descent with momentum
backpropagation
0.5221 0.6287 0.2754 0.2415 1000 1000
Levenberg-Marquardt backpropagation 0.9672 0.9711 0.9751 0.0105 14 20
BFGS quasi-Newton backpropagation 0.9205 0.9469 0.9001 0.0488 34 40
Gradient descent with adaptive learning
rate backpropagation
0.8911 0.9023 0.8822 0.0739 429 435
One-step secant backpropagation 0.9092 0.9415 0.9026 0.0596 38 44
Random order incremental training with
learning functions
0.7625 0.8091 0.4985 0.1596 29 35
Resilient backpropagation 0.8416 0.8471 0.7607 0.1136 14 20
Scaled conjugate gradient
backpropagation
0.8871 0.9022 0.8925 0.0824 44 50
Table 7. Network weights and biases of the MLP model
Neurons 
Weights from input layers to hidden layers Bias to hidden
layers
Weights from hidden
layers to output layers 
Bias to output layers
Time Temperature Granulometry Bed height Flow rate
1 -1.6411 -1.0314 -0.2218 1.4326 1.0767 1.0627 2.4494 -2.2668
2 -1.8958 0.7684 2.5437 0.7062 0.2812 2.2404 1.4611
3 -1.9015 -0.7206 -2.3748 1.8732 1.4295 1.1361 -2.0602
4 4.0264 1.9543 -3.2454 -0.5353 1.3658 3.1884 1.6843
5 -2.1390 1.5682 -1.6511 0.5067 -2.6376 0.6011 -1.9889
6 2.4698 3.0636 -1.1665 -0.7547 -2.5089 2.6911 0.7432
7 -6.4296 1.8824 1.5393 -1.7996 1.7874 -6.2597 -2.5910
8 -1.0912 -0.3890 1.4388 0.1959 1.7282 2.3409 -1.9751

---

M.S. LEITEet al.: MODELING OF MILK LACTOSE REMOVAL… Chem. Ind. Chem. Eng. Q. 25 (4) 369−382 (2019)
377
Table 8. Network weights and biases of the RBF model
Neurons 
Weights from input layers to hidden layers Bias to hidden
layers
Weights from hidden
layers to output layers
Bias to output
layers
Time Temperature Granulometry Bed height Flow rate
1 -0.9740 0.0000 -0.2857 0.0000 0.0000 4.1628 -1.4422 0.4692
2 -0.9688 1.0000 -1.0000 1.0000 1.0000 4.1628 -1.4518
3 -0.9740 -1.0000 1.0000 1.0000 1.0000 4.1628 -1.4655
4 -0.9584 -1.0000 1.0000 -1.0000 -1.0000 4.1628 -1.3966
5 -0.9688 -1.0000 -1.0000 -1.0000 1.0000 4.1628 -2.3817
6 -0.6104 0.0000 -0.2857 0.0000 0.0000 4.1628 0.1244
7 -0.6104 0.0000 -0.2857 0.0000 0.0000 4.1628 0.0000
8 -0.6987 -1.0000 -1.0000 1.0000 -1.0000 4.1628 -1.2770
9 -1.0000 1.0000 1.0000 -1.0000 1.0000 4.1628 -2.1296
10 -0.8182 -1.0000 -1.0000 -1.0000 1.0000 4.1628 1.1880
11 -0.8182 1.0000 1.0000 1.0000 -1.0000 4.1628 -1.4047
12 -0.8182 1.0000 1.0000 -1.0000 1.0000 4.1628 1.0385
13 0.2208 0.0000 -0.2857 0.0000 0.0000 4.1628 0.2160
14 -0.7662 1.0000 -1.0000 -1.0000 -1.0000 4.1628 -1.3967
15 0.4805 -1.0000 1.0000 1.0000 1.0000 4.1628 0.5903
16 1.0000 0.0000 -0.2857 0.0000 0.0000 4.1628 0.4656
Figure 5. Regression plot showing regression coefficient of MLP and RBF models in 30% of the test data.
Table 9. Quantification of the relative importance of input vari-
ables
Variable Temperature Granulometry Bed height Flow rate
Relative imp-
ortance (%)
19.3960 22.2805 30.5598 27.7637
The results of the adsorption capacity (q0) of
each experimental condition studied, according to the
experimental design (Table 1), are presented in
Figure 6.
In relation to bed height, the increased lactose
removal is associated with a greater amount of filling,
the MIP adsorbent is more selective, so it absorbs
more lactose, allowing a maximum mass transfer
between particles through the bed. It is verified, in
these cases, that the greater the height of the bed, for
the same flow, the greater the saturation of the bed,
as expected [8,9]. It was observed that the best oper-
ating conditions were associated with experimental
test 5 (temperature = 34 °C, granulometry = 60 mesh,
bed height = 12.5 cm, flow = 9 mL min
-1
), which
provided an adsorption capacity equal to 63.31 mg g
-1
.
The maximum adsorption capacity of batch chol-
esterol related in work of Oliveiraet al. [9] was 74.2
mg g
-1 
cholesterol from molecular imprinting tech-
nique for the removal of cholesterol in milk in a batch
regime. Jiet al. [39] applied molecularly imprinted
polymer for rapid determination of bisphenol A in
environmental water and milk samples, and the ads-
orption capacity of the adsorbent was found to be 390
and 270 mg g
-1
. The authors note that the adsorption
capacity of the MIP is equivalent to the contribution
from the specific binding sites on the adsorbent, and

---

M.S. LEITEet al.: MODELING OF MILK LACTOSE REMOVAL… Chem. Ind. Chem. Eng. Q. 25 (4) 369−382 (2019)
378
this contribution increases with the concentration of
bisphenol A because more specific recognition sites
are activated at higher BPA concentrations. Chenget
al. [40] studied the application of surface molecularly
imprinted silica gel was adopted as the adsorbent of
solid-phase extraction for detecting melamine from
milk samples. Based on the Langmuir adsorption
equation, the saturated adsorption capacity was
7.719 mg g
-1
. Soleimaniet al. [41] used synthesis of
molecularly imprinted polymer as a sorbent for solid
phase extraction of bovine albumin from whey, milk,
urine and serum. The adsorption capacity of the ads-
orbent reported by the authors was 24 mg g
-1
. From
the data reported in the literature, it can be seen that
the adsorption capacity depends, in addition to the
form of preparation of the adsorbent, especially on
the molecule to be extracted.
In the process used as a case study in this
paper, the best adsorption capacity was obtained in
test 5 when the lowest temperature (34 °C), the
maximum flow (9 mL min
-1
) and the maximum bed
height (12.5) in the studied range were applied. In
contrast, an unsatisfactory result was obtained when
a higher temperature (60 °C) and the minimum flow
rate (3 mL min
-1
) were applied (test 6), with the same
granulometry and bed height as test 5. The tempera-
ture influenced the process when combined with the
flow rate. Normally, the increase in temperature is
detrimental to the removal efficiency because at
higher temperatures there is an increase in molecular
agitation, which makes it difficult for the adsorbent to
adsorb the lactose molecules.
An unsatisfactory result was also obtained in
test 7, when the bed height was maximum (12.5 cm)
and the flow rate was minimal (3 mL min
-1
). Main-
taining the temperature and the flow rate, the influ-
ence of the granulometry and bed height variables
was observed in tests 3 and 5. An increase in the
granulometry and bed height increased the lactose
removal because the contact surface area increased,
increasing the number of sites available for adsorption.
Comparing model responses and experimental data
With the developed MLP and RBF models, their
relative concentration predictions (C/C0) were com-
pared graphically to the experimental tests, whose
conditions are presented in the experimental design.
These data were used to calculate the performance
indices: mean values ofR²,MSE,RMSE,SSE,MAE
andRME (Table 10).
Table 10. Mean values of performance indices for the MLP and
RBF models in the prediction of tests 1-9
Performance index 
Model
MLP RBF
R² 0.9751 0.9505
MSE 0.0105 0.0178
RMSE 0.0888 0.1291
SSE 2.4551 2.4348
MAE 0.0646 0.0901
RME / % 34.5456 36.3801
When error indexes approach 0 it means that
the error of our model decreases. It is a good mea-
sure of accuracy. Smaller values of error indices
mean a better performance of the model. These indi-
ces (defined in Eqs. (4)-(9)) describe the average
magnitude of the errors. It is a good measure of
accuracy. Under these conditions, all indices of assay
quality were acceptable for both ANN models
[28,29,33,42], as shown in Table 10.
The best approximation predictions were related
to the MLP and this behavior can be attributed to the
fact that this model has a validation step in its learn-
ing process [43,44] However, the RBF model was
Figure 6. Adsorption capacity data for the experimental tests.

---

M.S. LEITEet al.: MODELING OF MILK LACTOSE REMOVAL… Chem. Ind. Chem. Eng. Q. 25 (4) 369−382 (2019)
379
efficient in some experimental tests, but, like the MLP
model, could not predict some points.
Figures 7–9 show the profiles of the break-
through curves under various operating conditions
(tests 1−9), with the predictions of the three different
models. These curves describe the adsorption pro-
cess of milk lactose, where the final and initial lactose
concentrations are equal when the relative concentra-
tion reaches the breakpoint, namely when the ads-
orbent is saturated [12,15,44].
Figure 7. Breakthrough curves of experimental tests (1, 2 and 3) and prediction of the ANN models.
Figure 8. Breakthrough curves of experimental tests (4, 5 and 6) and prediction of the ANN models.
0 5 10 15 20 25 30
Relative Concentration
(C/Co)
0
0.5
1
Test data 7 Prediction MLP Prediction RBF
Time (min)
0 5 10 15 20 25 30
0
0.5
1
Test data 8 Prediction MLP Prediction RBF
0 5 10 15 20 25 30
0
0.5
1
Test data 9 Prediction MLP Prediction RBF
T: 34 (ºC) G: 32 (mesh) B: 12.5 (cm) F: 3 (mL/min)
T: 47 (ºC) G: 42 (mesh) B: 10 (cm) F: 6 (mL/min)
T: 60(ºC) G: 32 (mesh) B: 12.5 (cm) F: 9 (mL/min)
Figure 9. Breakthrough curves of experimental tests (7, 8 and 9) and prediction of the ANN models.

---

M.S. LEITEet al.: MODELING OF MILK LACTOSE REMOVAL… Chem. Ind. Chem. Eng. Q. 25 (4) 369−382 (2019)
380
Initially, it was noticed that the adsorbent MIP
was able to efficiently adsorb the lactose. However,
the lactose concentration increased as a function of
time and the removal efficiency decreased because
the number of active sites in the adsorbent available
to adsorb lactose also decreased. At the end of the
process, the final concentration was higher than the
initial one and this can be explained by the desorption
process, which occurs when the adsorbed lactose is
released from the adsorbent after saturation. In test 5,
a plateau is present, which indicates a period with
constant lactose removal. This unusual behavior imp-
lied a difficulty in the prediction of the RBF models.
However, the dynamics were captured and predicted
by the MLP neural model.
The breakthrough curves were atypical com-
pared to the ones described in the literature because
it surpassed the breakpoint. This behavior may be
because milk is a multicomponent mixture [8,9]. For
these fluids, theC/C0 ratio can extrapolate the bound-
ary of the unit, considering the different adsorption
affinities of the various solutes. Curves of this type
reflect the phenomenon of sequential exchange, in
which a more selective solute is able to remove, from
the site, another previously exchanged solute, which
is released into the liquid medium [45]. Similar results
have been reported by another researcher who used
an adsorption process in a multicomponent system [46].
As can be seen from the breakthrough curves
(Figures 7 and 9), higher breakpoint time of the pro-
cess was achieved at a lower flow rate. As the flow
rate increases, breakthrough time was obtained
earlier. This can be explained by the fact that the dif-
fusion process that controls the adsorption becomes
slow, and hence, the adsorbent needs more time to
bind with the lactose efficiently. The decrease in the
breakthrough time with an increase in the flow rate
may be due to a fixed saturation capacity of the bed
based on the same driving force giving rise to a
shorter time for saturation at higher flow rates [45,47].
It was verified that the model MLP obtained the
most satisfactory performance even for the profiles
that presented the plateau, thus, demonstrating that
the model is apt to predict nonlinear problems. In
addition, this model was able to predict the experi-
mental data, regardless of the conditions analyzed.
Hence, the ANN modeling technique is promising to
describe processes involving non-linear problems and
can be used to optimize the operational conditions of
lactose removal. The precision of data influences the
applicability of the models.
CONCLUSION
In the present work, milk lactose adsorption in a
fixed bed column with a MIP adsorbent was modeled
using an empirical approach by neural networks.
Neural models efficiently predicted the nonlinear
behavior of relative lactose concentration (C/C0) in
milk from interactions between the contact time (min),
temperature (°C), granulometry (mesh), bed height
(cm) and flow rate (ml min
-1
) parameters. The MLP
model with Levenberg-Marquardt algorithm had a
meanR² of 0.9751,MAE of 0.064 andRMSE of
0.0888 in the prediction of the experimental tests of
this study. The RBF model also showed a satisfactory
performance, which had an averageR² of 0.9505,
MAE of 0.090 andRMSE of 0.1291. Both models give
highly accurate predictions, since the performance
indices values are close. The high coefficient of deter-
mination of both networks (for the whole data set)
together with the important statistical parameters indi-
cated that the neural networks have been well
trained. These ANN models aimed to predict the
breakthrough curve in lactose adsorption. The results
showed that the ANN is a powerful technique to use
when dealing with multicomponent fluid processes.
Besides being simple to implement and requiring low
computational time, the neural network models satis-
factorily described the milk lactose adsorption and
these models can provide an additional contribution to
optimize and a better understanding of the dynamic of
the process. Furthermore, this allowed a feasible way
for on-line control of the process.
Nomenclature
Symbols
b1j bias to hidden layers
b2 bias to output layers
C0 initial concentration (mg mL
-1
)
C concentration at the exit (mg mL
-1
) from the bed
D particle diameter (cm)
H height of the particle (cm)
m mass of the adsorbent (g)
N data number
pi predicted value
pm mean of the predicted values.
q0 adsorption capacity (mg g
-1
)
ti experimental value
tm mean of the experimental values
V flow rate (mL min
-1
)
xi input of neuroni
xij input values
Wij weight binding of neuroni to neuronj

---

M.S. LEITEet al.: MODELING OF MILK LACTOSE REMOVAL… Chem. Ind. Chem. Eng. Q. 25 (4) 369−382 (2019)
381
wij andwxy weights from input layers to hidden
layers
w2j andwyz weights from hidden layers to output
layers
Greek symbols
ε porosity of the bed (mesh)
βj deviation of neuronj
Acknowledgment
The authors are grateful to the Brazilian financial
support of CAPES, CNPq and FAPITEC/SE.
REFERENCES
[1] A. K. Shrestha, T. Howes, B.P. Adhikari, B.R. Bhandari,
LWT-Food Sci. Technol. 40 (2007) 1593–1600
[2] K.Pawłowska, W. Umławska, B. Iwańczak, Pediatr. Pol. 1
(2016) 1–7
[3] [M. Maghsoudi, M. Ghaedi, A. Zinali, A.M. Ghaedi, M.H.
Habibi, Spectrochim. Acta, A134 (2015) 1–9
[4] Y. Zhang, B. Pan, Chem. Eng. J. 249 (2014) 111–120
[5] E. Oguz, M. Ersoy, Chem. Eng. J. 164 (2010) 56–62
[6] R. Tovar-Gómez, M.R. Moreno-Virgen, J.A. Dena-Agui-
lar, V. Hernández-Montoya, A. Bonilla-Petriciolet, M.A.
Montes-Morán, Chem. Eng. J. 228 (2013) 1098–1109
[7] H. Yavuz, V. Karakoç, D, Türkmen, R. Say, A. Denizli, Int.
J. Biol. Macromol. 41 (2007) 8–15
[8] A.L. Balieiro, R.A. Santos, M.M. Pereira, L.S. Freitas,
O.L.S. Alsina, A.S. Lima, C.M.F. Soares, Braz. J. Chem.
Eng. 33 (2016) 61–72
[9] G.R. Oliveira, A.V. Santos, A.S. Lima, C.M.F. Soares,
M.S. Leite, LWT-Food Sci. Technol. 64 (2015) 632–638
[10] N. Diban, G. Ruiz, A. Urtiaga, I. Ortiz, J. Food Eng. 78
(2007) 1259-1266
[11] G. Bogdanović, M. Gorgievski, D. Božić, V. Stanković,
Chem. Ind. Chem. Eng. Q. 15 (2009) 237-249
[12] L. Tercinier, A. Ye, S. Anema, A. Singh, H. Singh, J.
Colloid Interface Sci. 394 (2013) 458–466
[13] M. Rajeshkannan, N.R. Rajasimman, Chem. Ind. Chem.
Eng. Q. 17 (2011) 67−79
[14] M. Kodric, S. Stojanovic, B. Markovic, D. Djordjevic,
Chem. Ind. Chem. Eng. Q. 23 (2016) 22-22
[15] M.L. Soto, A. Moure, H. Dominguez, J.C. Parajó, J. Food
Eng. 209 (2017) 52-60
[16] R.M. Aghav, S. Kumar, S.N. Mukherjee, J. Hazard Mater.
188 (2011) 67–77
[17] S. Elemen, E.P. Kumbasar, S. Yapar, Dye Pigment 95
(2012) 102–111
[18] Z. Hassanzadeh, M. Kompany-Zareh, R. Ghavami, S.
Gholami, A. Malek-Khatabi, J. Mol. Struct. 1098 (2015)
91–98
[19] K.V. Kumar, K. Porkodi, Chem. Eng. J. 148 (2009) 20–25
[20] M.S. Petrović, T.D. Šoštarić, L.L. Pezo, S.M. Stanković,
C.M. Lačnjevac, J.V. Milojković, M.D. Stojanović, Chem.
Ind. Chem. Eng. Q. 21 (2015) 249-259
[21] B. Singha, N. Bar, S.K. Das, J. Mol. Liq. 211 (2015) 228–
–232
[22] N.G. Turan, B. Mesci, O. Ozgonenel, Chem. Eng. J. 171
(2011) 1091–1097
[23] S. Chakraverty, S. Mall, CRC press, Taylor & Francis
Group, EUA, 2017
[24] Y. Rafiq, D.J. Easterbrook, G. Bugman, Comput. Struct.
79 (2001) 1541-1552
[25] A.A. Amooey, M. Ahangarian Maryam, F. Rezazadeh,
Chem. Ind. Chem. Eng. Q. 20 (2014) 565-569
[26] M. Beigi, M. Torki-Harchegani, M. Mahmoodi-Eshkaftaki,
Chem. Ind. Chem. Eng. Q. 23 (2017) 251-258
[27] J. Ding, H. Wang, K. Dai, Y. Zi, Z. Shi, Chem. Ind. Chem.
Eng. Q. 20 (2014) 29-38
[28] . Sargolzaei, N. Saghatoleslami, S.M. Mosavi, M. Khosh-
noodi, Iran. J. Chem. Chem. Eng. 25 (2006) 67
[29] A. Razavia, S.M. Mousavib, S.A. Mortazavia, Chem. Eng.
Sci. 58 (2003) 4185-4195
[30] M.S. Leite, B. Ferreira, L. Maria, F. Lona, V. Silva, A.
Maria, F. Fileti, Chem. Eng. Trans. 24 (2011) 385–390
[31] B.F. Santos, M.S. Leite, F.V. Silva, A.M.F. Fileti, Chem.
Pap. 66 (2012) 654–663
[32] D.F. Viana, G.R. Salazar-Banda, M.S. Leite, Sep. Sci.
Technol. (2018) 1-15 DOI: 10.1080/
/01496395.2018.1463264
[33] R. Soleimani, N.A. Shoushtari, B. Mirza, A. Salahi, Chem.
Eng. Res. Des. 91 (2013) 883–889
[34] P. Kundu, V. Paul, V. Kumar, I.M. Mishra, Chem. Eng.
Res. Des. 104 (2015) 773–790
[35] A.O. Oladunjoye, S.A. Oyewole, S. Singh, O.A.
Ljabadeniyi, LWT - Food Sci. Technol. 76 (2017) 9–17
[36] J. Liu, Springer Ed., Heidelberg, EUA, 2013
[37] O.M. Ibrahim, J. Appl. Sci. Res. 9 (2013) 5692–5700
[38] M. Kashaninejad, A.A. Dehghani, M. Kashiri, J. Food
Eng. 91 (2009) 602-607
[39] Y. Ji, J.Yin, Z. Xu, C. Zhao, H. Huang, H. Zhang, C.
Wang, Anal. Bioanal. Chem. 395 (2009) 1125–1133
[40] W. Cheng, Z. Liu, Y. Wang, Talanta 116 (2013) 396–402
[41] M. Soleimani, S. Ghaderi, M.G. Afshar, S. Soleimani, J.
Microchem. J. 100 (2012) 1–7
[42] D. Azeez, M.A. Ali, K. Gan, I. Saiboon, SpringerPlus 2(1)
(2013) 416
[43] M. Bagheri, S.A. Mirbagheri, M. Ehteshami, Z. Bagheri,
Process Saf. Environ. Prot. 93 (2015) 111–123
[44] M. Khanmohammadi, A.B. Garmarudi, K. Ghasemi, S.
Garrigues, M. Guardia, Microchem. J. 91 (2009) 47–52
[45] M.A. Fulazzaky, M.H. Khamidun, R. Omar, Chem. Eng. J.
228 (2013) 1023–1029
[46] A. Talebian, A.R. Keshtkar, M.A. Moosavian, Korean J.
Chem. Eng. 33 (2016) 2205-2214
[47] S. Gupta, B.V. Babu, Bioresour. Technol. 100 (2009)
5633–5640.

---

M.S. LEITEet al.: MODELING OF MILK LACTOSE REMOVAL… Chem. Ind. Chem. Eng. Q. 25 (4) 369−382 (2019)
382
MANUELA SOUZA LEITE
MATHEUS A. SANTOS
EULINA M. F. COSTA
ACENINI BALIEIRO
ÁLVARO S. LIMA
ODELSIA L. SANCHEZ
CLEIDE M. F. SOARES
Tiradentes University, Institute of
Technology Research, Farolândia,
Aracaju, Sergipe, Brazil
NAUČNI RAD
MODELOVANJE UKLANJANJA LAKTOZE IZ MLEKA
ADSORPCIONOM KOLONOM KORIŠĆENJEM MLP
I RBF VEŠTAČKIH NEURONSKIH MREŽA
Veštačke neuronske mreže (ANN) su efikasne u modelovanju nelinearnih procesa,
jednostavne su za implementaciju i zahtevaju kratko vreme računanja. U ovom radu,
kontinualni proces adsorpcije laktoze u koloni sa fiksnim slojem molekularno utisnutim
polimernim (MIP) adsorbentom je modelovan korišćenjem ANN tehnike. Ovi neuralni
modeli omogućili su predviđanje relativne koncentracije laktoze (C/C0) iz interakcija
između procesnih promenljivih: vremena kontakta, temperature, veličine čestica, visine
sloja i protoka. Modeli ANN razvijeni su u MATLAB-u uz pomoć višeslojnih perceptrona
(MLP) i mreže radijalnih baznih funkcija (RBF). MLP model je razvijen korišćenjem tro-
slojne povratne mreže sa 5, 8 i 4 neurona u prvom, drugom i trećem sloju. Predložena je
i RBF mreža i njena performansa je upoređena sa tradicionalnim tipom mreže. Najbolji
model arhitekture RBF je razvijen koristeći 5, 14 i 1 neuron u prvom, drugom i trećem
sloju. Korišćenjem ovih pristupa, razvojeni su inovativni matematički modeli koji su pri-
menjeni na višekomponentni adsorpcioni sistem za mleko. Dobijeni modeli krivih pro-
boja za adsorpciju laktoze se dobro slažu sa eksperimentalnim podacima. Kriterijumi,
kao što su R², MSE, RMSE, SSE, MAE i RME, korišćeni su za procenu pouzdanosti i
tačnosti modela. Poređenjem ANN modela mogu se predvideti krive proboja za uklanja-
nje laktoze iz mleka procesom adsorpcije. Ipak, MLP model je tačniji i sa većim koefici-
jentom korelacije (R
2 
= 0,975) i manjim vrednostima greški. Tačnost modela je potvrđen
poređenjem predviđenih i eksperimentalnih podataka. Rezultati su pokazali da oba
modela efikasno opisuju nelinearni proces adsorpcije laktoze u koloni sa fiksnim slojem.
Ključne reči: ANN, MLP, RBF, kolona sa fiksnim slojem, laktoza, modelovanje
krive proboja.