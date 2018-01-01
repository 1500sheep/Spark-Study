### Spark Install



#### Spark Install (JAVA 사전에 설치)

1. sudo apt-add install scala
2. tar -xvzf spark-2.1.0-bin-hadoop2.7.tgz
3. bin/spark-shell(스파크 실행)

#### Spark WordCount(Scala, Python)

1. Scala

   1. Spark directory위치에서 bin/spark-shell.

   2. WordCount 

      > val textFile = sc.textFile("/home/jameskang/spark/word.txt")
      >
      > val counts = textFile.flatMap(line => line.split(" "))map(word =>(word,1))reduceByKey(_ + _)
      >
      > counts.collect()

2. Python

   1. Spark directory위치에서 bin/pyspark.

   2. WordCount

      > text_file = sc.textFile("/home/jameskang/spark/word.txt")
      >
      > counts  = text_file.flatMap(lambda line : line.split(" ")).map(lamda word:(word,1)).reduceByKey(lambda a,b : a +b)
      >
      > counts.collect()

   **localhost:4040으로 completed Jobs확인** 

