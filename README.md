# sessionFour-Assignment1-
  Find the average of numbers.Initialize the base RDD with a list of 1,2,3,4,5,6,7,8,9,10

val inputRDD = sc.parallelize(List(1,2,3,4,5,6,7,8,9,10))

val sumRDD = inputRDD.reduce((x,y) => x + y)

val countRDD = inputRDD.count

val avgRDD = sumRDD/countRDD

val answerRDD = avgRDD.collect


 Find the average of numbers.Read the numbers from a file, each number in separate line. 1,2,3,4,5,6,7,8,9,10

val inputRDD = sc.textFile("DATA.txt")

val splitRDD = inputRDD.split(",")

val sumRDD = splitRDD.reduce((x,y) => x + y)

val countRDD = splitRDD.count

val avgRDD = sumRDD/countRDD

val answerRDD = avgRDD.collect
