# sparkprograms
Spark Programs
first

//library Functions
package sparker
import org.apache.spark._
import org.apache.spark.SparkContext
import org.apache.log4j._

//scala object
object f1spark {
      def main(args:Array[String]){
       //log level to print errors
        Logger.getLogger("org").setLevel(Level.ERROR)
       val sc=new SparkContext("local[*]","tort")
      val lines=sc.textFile("C:/ml-100k/ml-100k/u1.info")
 

       
      println(lines.count())
        val ratings=lines.map(x=>x.toString().toUpperCase())
        ratings.foreach(println)
              val ratings1=lines.map(x=>x.toString().capitalize)
        ratings1.foreach(println)
       // val results=ratings.countByValue()
      //  val sortedresults=results.toSeq.sortBy(_._1)
        
      }
}   

