Description : Write a program read numbers from a file in C language and print the biggest number and minumim number 

Level : Hard

Enjoy :

@Alhakami

Code : 

 FILE* numbers;
    int number;
    int min;
    int max;
    int count;
    numbers = fopen("/challenge/numbers.txt", "r");
        for (count = 0;
            fscanf(numbers, "%d", &number) == 1;)
            if (number >= 0)
            {  if (!count)
                {min = max = number;
                    count = 1;}
                else if (number > max) max = number;
                else if (number < min) min = number;}
        
        printf("%d\n", max);
        printf("%d\n", min);
