# My-Works-with-C-
This field has my codes when I started to learn C# at university.


using System;

class Program
{
 static void Main(string[] args)
   {
    string[,] employees = {
           { "Ali", "Developer", "100000", "8" },
           { "Ayse", "Developer", "100000", "9" },
           { "Mehmet", "Developer", "100000", "2" },
           { "Osman", "Manager", "500000", "2" },
           { "Pelin", "Manager", "500000", "9" },
           { "Murat", "Developer", "100000", "1" }
    };

    Console.Write("Enter your name: ");
    string name = Console.ReadLine();

    string[] employee = GetEmployee(employees, name);
        if (employee != null)
         {
            Console.WriteLine($"Hello dear {employee[0]} with your performance rate of {employee[3]}   ");
            buraya gelecek var
         }  
         else
         {
            System.Console.WriteLine("Employee not found. ");
         } 
   }
   Calısanı  bulma metodu
   static string[] GetEmployee (string[,] employee, string name)

        {
            for( int i = 0;
            i < employee.GetLength(0);i++ )
            {
                if (employee[i, 0].Equals(name, StringComparison.OrdinalIgnoreCase))
             {
                 return new string[] { employee[i, 0], employee[i, 1], employee[i, 2], employee[i, 3] };
             }
            }

        }
}
class Program
{
    static void Main(string[] args)
    {
        string[,] employees = {
            { "Ali", "Developer", "100000", "8" },
            { "Ayse", "Developer", "100000", "9" },
            { "Mehmet", "Developer", "100000", "2" },
            { "Osman", "Manager", "500000", "2" },
            { "Pelin", "Manager", "500000", "9" },
            { "Murat", "Developer", "100000", "1" }
        };

        Console.Write("Enter your name: ");
        string? name = Console.ReadLine();

        string[]? employee = GetEmployee(employees, name);
        if (employee != null)
        {
            Console.WriteLine($"Hello dear {employee[0]} with your performance rate of {employee[3]} you've deserved {Raise(employee)} monthly");
        }
        else
        {
            Console.WriteLine("Employee not found.");
        }
    }

    // Çalışanı bulma metodu
    static string[]? GetEmployee(string[,] employees, string name)
    {
        for (int i = 0; 
        i < employees.GetLength(0); i++)
        {
            if (employees[i, 0].Equals(name, StringComparison.OrdinalIgnoreCase))
            {
                return new string[] { employees[i, 0], employees[i, 1], employees[i, 2], employees[i, 3] };
            }
        }
        return null;
    }

    // Maaşı hesaplayan metot
    static double Raise(string[] employee)
    {
        string role = employee[1];
        double salary = double.Parse(employee[2]);
        int performance = int.Parse(employee[3]);

        if (role == "Manager")
        {
            if (performance > 5)
                return salary * 1.4;  // %40 zam
            else
                return salary * 0.6;  // %40 kesinti
        }
        else if (role == "Developer")
        {
            if (performance > 5)
                return salary * 1.3;  // %30 zam
            else
                return salary * 0.7;  // %30 kesinti
        }

        return salary;  // Rol bulunamazsa değişiklik yapma
    }
}
{
    static void Main()
    {
        System.Console.WriteLine("Number   |  Square  | Cube   ");
        System.Console.WriteLine("---------|----------|--------");

    }
}/*
{
    static void Main()

  { */
     string password = "123";
    System.Console.Write(" Please enter the passwor: ");
    string enterpassword = Console.ReadLine();
    /*Random rnd = new Random();
    int x = rnd.Next(1,10);
    int guess;
    int guessCount;

    System.Console.Write("Guess a number: ");
    int guess = int.Parse(Console.ReadLine());

    do
    {  
       System.Console.WriteLine("Enter your guess: ");



    }
  }

}*/


using System;
 class Program
 {

    static void Main()
    {

        Console.Write("Enter a number: ");
        int number = int.Parse(Console.ReadLine());


        if (IsDarmstadtiumNumber(number))
        {
            Console.WriteLine($"{number} is a Darmstadtium number.");
        }
        else
        {
            Console.WriteLine($"{number} is not a Darmstadtium number.");
        }

 }
System.Console.Write(" Please enter the number: ");using System;

class Program
{
    static void Main()
    {
        Kullanıcıdan üst sınırı al
        Console.Write("Bir sayı girin (n): ");
        int n = int.Parse(Console.ReadLine());

        int sum = 0;


        for (int i = 1; i <= n; i += 2) 
        {

            int factorial = Factorial(i);
            sum += factorial;
        }


        Console.WriteLine("0'dan {0}'a kadar olan tek sayıların faktöriyel toplamı: {1}", n, sum);
    }


    static int Factorial(int number)
    {
        int result = 1;
        for (int i = 1; i <= number; i++)
        {
            result *= i;
        }
        return result;
    }
}

int number =int.Parse(Console.ReadLine());

int sum = 0;
for (int i = 1; i <= n; i += 2)  
        {
            int factorial = Factorial(i);
            sum += factorial;
        }

 using System;
using static System.Console;

class ArrayDemo2
{
    static void Main()
    {
        int[] scores = new int[8];  // 8 elemanlı bir dizi oluşturduk
        int x;                       // Sayaç değişkeni
        string inputString;          // Kullanıcıdan gelen girişleri saklamak için string değişkeni

        int count;                   // Tire sayacını tutacak değişken
        const int DASHES = 50;       // Sabit: 50 tire

        for (x = 0; x < scores.Length; x++)
        {
            Write("Enter score {0}: ", x + 1);  // Kullanıcıya kaçıncı puanı girdiğini göster
            inputString = ReadLine();           // Kullanıcıdan giriş al
            scores[x] = int.Parse(inputString); // Stringi integer'a çevir ve diziye ekle
        }
    }
}
using System;

class Program
{    
    static void Main()
    {
        double accountBalance = 1000.0;
        System.Console.WriteLine("Initial Balance: "+ accountBalance + " TL ");

        Deposit(ref accountBalance, 200.0);
        System.Console.WriteLine("Updated Balance: "+ accountBalance + " TL ");

        Deposit(ref accountBalance);
        System.Console.WriteLine("Updated Balance: "+ accountBalance + " TL ");


    }
    
}

Console.Write("1. Sayı: ");
var sayı1 = Convert.ToInt32(Console.ReadLine());

Console.Write("2. Sayı: ");
var sayı2 = Convert.ToInt32(Console.ReadLine());

System.Console.WriteLine("Toplama için + ");
System.Console.WriteLine("Çıkarma için - ");
System.Console.WriteLine("Çarpma için * " );
System.Console.WriteLine("Bölme için  / " );

System.Console.Write("Seçiminiz: ");
var secim = Console.ReadLine();
double sonuc = 0;
bool ok = true;
if( secim == "+"){
    sonuc= sayı1 + sayı2;
} else if (secim =="-"){
   
    sonuc= sayı1 - sayı2;
} else if ( secim == "*"){
    sonuc= sayı1 * sayı2;

} else if ( secim == "/"){
     if (sayı2==0){
        ok= false;
        System.Console.WriteLine(
"Dikkat, Bölen sıfır olamaz. ");
     }else{
    sonuc= sayı1 / sayı2;

     }
    
} else {
     ok = false;
    System.Console.WriteLine("Yanlış seçim. ");

}
if(ok){
        System.Console.WriteLine($"İşlem sonucu : {sayı1} {secim} {sayı2} = {sonuc}");
}




System.Console.Write("a: ");
int a = Convert.ToInt32(Console.ReadLine());

System.Console.Write("b: ");
int b = Convert.ToInt32(Console.ReadLine());

System.Console.Write("c: ");
int c = Convert.ToInt32(Console.ReadLine());


int enbuyuk = 0;
if (a > b && a> c){
    enbuyuk = a ;
} else if (b > a && b> c){
    enbuyuk = b ;
}
else {
    enbuyuk = c;
}
System.Console.WriteLine("en buyuk sayı: "+ enbuyuk);
int ortalama = (a + b + c) / 3;
System.Console.WriteLine("Sayıların ortalaması :" + ortalama);
 
 int ay=13;
  switch (ay)
  {
    case 12:
    case 1:
    case 2:
    System.Console.WriteLine("kış");
         break;

    case 3:
    case 4:
    case 5:
    System.Console.WriteLine("ilkbahar");
         break;
     case 6:
    case 7:
    case 8:
    System.Console.WriteLine("yaz");
         break;

    
    case 9:
    case 10:
    case 11:
    System.Console.WriteLine("sonbahar");
         break;
     
    default:
    System.Console.WriteLine("Hatalı ay bilgisi.");
        break;

  }


 int sayi= -1087;
 System.Console.Write(sayi + ": ");
 var sonuc =(sayi % 2 == 0) ? 
                          (sayi > 0 ) ? "pozitif çift sayı" :"negatif çift sayı": 
                          (sayi > 0 ) ? "pozitif tek sayı"  : "negatif tek sayı";

 System.Console.WriteLine(sonuc);
 var toplam = 0;
for(var i = 1; i <=7 ; i++)
{ 
           toplam += i;
  System.Console.WriteLine(toplam);

     if( i % 2 == 0)
     {
           toplam += i;

  System.Console.WriteLine(toplam);

     }

     
}
  System.Console.WriteLine(toplam);



class Country
{ 
    public Country(){}
    public Country(string name , int pop , bool eu ) 
    {
        Name = name;

        Population = pop;

        EuMember = eu;

    }

    public Country(string name ,bool eu) 
    {
        Name = name;

         EuMember = eu;

    

    }

    public string Name { get; set; }
    public int Population { get; set; }
    public bool EuMember { get; set; }


}



class TestCarpet
{

}
