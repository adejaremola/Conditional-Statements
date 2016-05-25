# Conditional-Statements
///<summary>
/// An array that gets 10 random scores, 
/// prints them out,
/// reverses the scores, 
/// and then the new array gets printed out
///</summary>

int [] Scores = new int[10];
int n = Scores.Length;
Random myRandom = new Random();
int randomEntry;
int[] reverseArray = new int[10];

            for (int index = 0; index < n; index++)
            {
                randomEntry = (int)(myRandom.NextDouble() * 100) + 1;
                Scores[index] = randomEntry;
            }

            for (int index = 0; index < n; index++)
            {
                if (index != 0 && (index % 5) == 0)
                {
                    Console.Write(Scores[index] + "\n");
                }
                else
                {
                    Console.Write(Scores[index] + " ");  
                }               
            }
            Console.WriteLine();

            for (int index = 0; index < Scores.Length; index++)
            {
                reverseArray[Scores.Length - index - 1] = Scores[index];
            }

            for (int index = 0; index < n; index++)
            {
                if (index != 0 && (index % 5) == 0)
                {
                    Console.Write(reverseArray[index] + "\n");
                }
                else
                {
                    Console.Write(reverseArray[index] + " ");
                }

            }
            Console.ReadLine();
