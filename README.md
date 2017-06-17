# ClouderaHadoopTraining

This project contains java codes required to execute the wordcount programs in Cloudera VM.

  By default cloudera vm contains eclipse pre-installed with mapreduce skeleton java code.
  The program doesn't contain the logic for MR. This repository contain basic wordcount logic embedded on it which will be easy for new hadoopers to getting started with Hadoop MR.
  
  Following things are modified.
  
  * Added wordcount map logic into Mapper code
  * Added wordcount reduce logic into Reducer Code
  * Added code for receiving Input/Output paths while running the program
  * Driver Program is configured with Mapper/Reducer classes along with its respective input/ouput formats/key/value classes
  
  
   #Running the program

1. Change the code
2. Export the jar from eclipse with Main Class as StubDriver (wordcount.jar)
3. Create a sample input file with some text content(input.txt)
4. Create input hdfs directory with below command

hdfs dfs -mkdir -p /user/cloudera/data/input/

5. Place the input file into the input directory

hdfs dfs -put input.txt /user/cloudera/data/input/

6. Execute the program with below command

hadoop jar wordcount.jar  /user/cloudera/data/input/input.txt /user/cloudera/data/output/

7. Observe the results in output folder

hdfs dfs -text /user/cloudera/data/output/part-r-00000

