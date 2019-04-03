# EDaWS
Early Diagnostic and Warning System

It is said that ‘A Stitch in time saves nine’. All over the world, people are applying this principle to personal health, by undergoing regular health checkups, even when their health seems to be in a good condition. The reason is to catch that disease early, before its’ symptoms start manifesting. If a disease is detected early, it will significantly reduce the cost of treatment; leave aside the loss of precious man hours, inconvenience and possibly permanent impairment.
The same principle is valid for any machinery. Today preventive maintenance is performed as per manufacturers schedule or in event of a malfunction, when it becomes ‘symptomatic’.

This can be further explained through example of say a disease like Diabetes. Let’s say upper permissible limit of sugar level is 140 and a particular individual has his/her sugar level maintained at say 115 for last decade. However in the previous year the sugar level recorded was 117 and this year its 121, both well within the prescribed limit, where person is declared perfectly healthy. Yet if plotted graphically the rise “trend” in sugar level is observed which can be extrapolated to predict a date by when sugar levels may cross the prescribed limits. Hence preventive measures like diet control, regular exercise etc. could be adopted to avoid or at least considerably postpone the disease.

We use a similar methodology for protecting valuable machinery and industrial plants through constant online monitoring of crucial parameters, much similar to taking an ‘ECG’.  It involves measurement of various parameters that determine the wellbeing of the machines such as temperature, vibration, sound (noise), Pressure, flow, input values of voltage and current etc. Thereafter software can identify two important deviations from specified parameters:
1.	Parameters crossing the prescribed threshold limits (sets alerts to go for root cause analysis of the deviations)
2.	Even if parameters are within the prescribed threshold limits is there any trend that can be spotted which has potential of future deviation 

Any event of deviation of parameters beyond the benchmark values would suggest of a potential malfunction in one of its subsystems. This will check a major break down in the plant in its nascent stage. In this condition, immediate steps can be taken to correct the error at its early stage which would minimize the cost of repair, downtime, inefficiency, and loss of production.
EDaWS goes to the extent of gathering various information like vibration, temperature, pressure, flow, energy consumption, power factor, process performances, historical records and the understanding of maintenance cultures in order to formulate a 'Condition Portrait' in solving predicting and preventing complex problems.

BENEFITS
1.	Solve Problem before they manifest
2.	Reduce Downtime Cost
3.	Increase lifetime of Machinery 
4.	Prevent Catastrophic Failures 
5.	Reduce Energy Bills 
6.	Improve Safety
7.	Improve the quality of work by improving the quality of the working environment

PARAMETERS TO BE MONITORED
1.	Temperature
2.	Noise (sound)
3.	Vibration
4.	Pressure
5.	Flow
6.	Electrical Current
7.	Power factor
8.	Energy consumption

Other parameters can be added, changed and modified depending upon the kind of system being monitored and the need of client.
The software will analyze the captured parameters and is a tailored approach towards a comprehensive predictive maintenance package for critical assets that requires detail observation for any change in equipment health. EDaWS will also provide necessary technical analytics of collected data after every significant survey scan to highlight equipment with significant change in health condition thus enabling customers on probable maintenance course of action or other preventive means like adding lubrication, adjusting load condition, verifying where about of other inputs

EDaWS uses the power of Azure combined with the support of embedded devices such as sensors in an IoT  configuration.
For the current prototype design we are using a Raspberry Pi 2 model B connected to sensors like LM35 (temperature sensor) and SW420 (vibration sensor). The data gathered by these sensors is sent to the Raspberry Pi unit by wired connection. The Raspberry Pi unit in turn communicates with the client app using Azure services. For demonstration purposes we are simulating all these functions using a windows console application.

 In our project we have used the following Azure services:
1. Azure Event Hub – this is used to collect data from the Raspberry Pi and save it on cloud.
2. Azure System Analytics – this is used to transfer data from events hub to an Azure SQL database.
3. Azure Mobile Services – this is used by the client app to get data from the Azure SQL database.

To sense anomalous behavior of a machine component and to check variance in the trend of the machine’s behavioral data collected by the sensor we will employ a machine learning algorithm, again deployed on Azure which will take data from the Raspberry Pi as the input and will determine whether the incoming data is within the acceptable domain in real time.
