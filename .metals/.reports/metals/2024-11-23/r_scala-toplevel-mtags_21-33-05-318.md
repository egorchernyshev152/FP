error id: file:///C:/lab_1/src/main/scala/Main.scala:[641..644) in Input.VirtualFile("file:///C:/lab_1/src/main/scala/Main.scala", "
//..1..
@main def hello() =
  println("Hello, Egor!")

//..2..
def helloNTimes(n: Int) = {
  for (i <- 1 to n)
  if (i%2 == 0) println(s"hello $i") else println(s"hello ${n - i}") 
}

//..3_1..
def splittingIndexes(collection: Seq[Int]): (Seq[Int], Seq[Int]) = {
  val evenIndexed = collection.zipWithIndex.filter ((_, index) => index % 2 == 0 ).map(_._1)
  val oddIndexed = collection.zipWithIndex.filter ((_, index) => index % 2 != 0 ).map(_._1)
  (evenIndexed, oddIndexed)
}
//..3_2..
def findMax(collection: Seq[Int]): Int = {
  collection.reduce ((x, y) => if (x > y) x else y)
}
//..4..
def

//..5..
//..6..
def compose[A, B, C](f: B => C, g: A => B): A => C = {
  (x: A) => f(g(x))
}
// Пример вызова функции
@main def start() = {
  //..2..
helloNTimes(5)

println()

//..3_1..
val (evens, odds) = splittingIndexes(1 to 10)
println(s"Четкие индексы: $evens") 
println(s"Нечеткие индексы: $odds") 

println()

//..3_2..
val maxElement = findMax(Seq(4, 8, -2, 0, 11))
println(s"Максимальный элемент $maxElement")
}
")
file:///C:/lab_1/src/main/scala/Main.scala:27: error: expected identifier; obtained def
def compose[A, B, C](f: B => C, g: A => B): A => C = {
^
#### Short summary: 

expected identifier; obtained def