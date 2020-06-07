Environment variables:

    export SPARK_HOME="/home/jstrebel/devel/spark/spark-2.4.5-bin-hadoop2.7/"
    export PATH="/home/jstrebel/devel/spark/spark-2.4.5-bin-hadoop2.7/bin/:$PATH"

Build:

`mvn clean package dependency:copy-dependencies`

Run with all dependencies:

    spark-submit --class de.strebel.App --master local[2] ./target/scala_spark_mvn-1.0-SNAPSHOT-jar-with-dependencies.jar

Run only the JAR file:
 
    spark-submit --class de.strebel.App --master local[2] --jars ./target/dependency/ ./target/scala_spark_mvn-1.0-SNAPSHOT.jar 
