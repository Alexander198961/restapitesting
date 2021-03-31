to run tests without GUI
jmeter -n -t  Test.jmx -l testresults.jtl
and view result in testresults.jtl file

or can run jmeter with GUI jmeter -t Test.jmx
click the run button and view result in View Results Tree

for set up parallel mode we need modify Test.jmx for example: 

<stringProp name="ThreadGroup.num_threads">1</stringProp>

change num_threads and set up threads count
change mode from true to false in line
<boolProp name="TestPlan.serialize_threadgroups">true</boolProp>

