# MapReduceWordCount
## Map Reduce Hortonwork
### Steps
* Open ssh client
On terminal, type

```
mkdir mapreduce
cd mapreduce
git clone https://github.com/AmirinNS/MapReduceWordCount
mkdir WCclass
cd MapReduceWordCount
javac -classpath /usr/hdp/2.5.0.0-1245/hadoop/hadoop-common-2.7.3.2.5.0.0-1245.jar:/usr/hdp/2.5.0.0-1245/hadoop-mapreduce/hadoop-mapreduce-client-core-2.7.3.2.5.0.0-1245.jar:usr/hdp/2.5.0.0-1245/hadoop-mapreduce/commons-cli-1.2.jar WordMapper.java SumReducer.java WordCount.java -d ~/mapreduce/WCclass
cd ..
jar -cvf WordCount.jar -C WCclass /
```
* Upload txt file on ambari
* Finally, on terminal

```
hadoop jar WordCount.jar WordCount /user/mapreduce /user/mapreduce/output
```
