
public class CheckRepeatedNoInArray {
    
    public static void main(String[] args) {
        int [] myArray = {10,5,7,10,5,7,10,0,5,0,3};
             GetRepeatedNoIn(myArray); //Calling GetRepeatedNoIn Method --> only accept positive Integer numbers
             
    }
    
    public static int GetRepeatedNoIn(int [] inputArray) // GetRepeatedNoIn Method calculate how many numbers are repeated in inputArray
    {
        
     int y =0, counter = 0;;
     int [] myArray = inputArray; // intializing inputArray values in myArray
       
        for (int item :myArray)
        {
           y=-1;
           for (int x :myArray)
           {         
            y++;              
                if (item ==x & myArray[y]!=-1)
                {
                  counter++;
                  myArray[y]=-1; 
                }          
           }           
       
         if (counter >= 1)
         {
          System.out.println("No."+item+" is repeated "+counter +" time");
         }
            counter =0;
        } 
        return 0;
    }
}
