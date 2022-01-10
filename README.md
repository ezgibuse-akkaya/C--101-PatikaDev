# CSharp-101-PatikaDev

[Patika.dev](https://app.patika.dev/egitimler) adresindeki "C# 101" eğitiminde kullandığım kaynak kodları içeren bir repo.

Bu README dosyasında Patika.Dev C# Ödev Soruları Ve Yanıtlarını bulacaksınız.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## :brain: Ödev 1

### :question: SORU 
Yeni bir console projesi açıp dersteki örnekleri yazınız ve ödevi tamamlayınız.
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
    
```csahrp
    
using System;

namespace Degiskenler
{
    class Program
    {
        static void Main(string[] args)
        {
           
           byte a = 1;
           sbyte b =2;

           short c = 3;
           ushort d = 4;

           Int16 e = 5;
           int f =6;
           Int32 g =7;
           Int64 h =8;

           uint i =9;
           long j =10;
           ulong k =11;

           float l =12;
           double m =13;
           decimal n =14;


          
           string p ="ab";
            
        
           bool r = true;
           bool s =false;

           DateTime dt = DateTime.Now;

           object t = "16";
           object u = "ab";
           object v = 17;
           object y = 18;
           object z = 18.1;


           string abc = string.Empty;
           abc = "deneme";
           string marka = "arçelik";
           string model = "Su ısıtıcısı";

           bool bl = 3>5;

           string vb = "20";
           int ty =20;
           string nr = vb + ty.ToString();
           int er = ty + Convert.ToInt32(vb);
           int yu = ty + int.Parse(vb);

        }
    }
}
```
</details>

## :brain: Ödev 2

### :question: SORU 
Yeni bir console projesi açıp dersteki örnekleri yazınız ve ödevi tamamlayınız.
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
    
```csahrp
using System;

namespace Operatorler
{
    class Program
    {
        static void Main(string[] args)
        {
            
           int a = 2;
           int b = 4;
           a = a+1;
           Console.WriteLine(a);
           a+=1;
           Console.WriteLine(a);
           a/=1;
           Console.WriteLine(a);
           b*=4;
           Console.WriteLine(b);

         //--------------------------------

           bool isSuccess = true;
           bool isCompelted = false;

           if (isSuccess && isCompelted )
           Console.WriteLine("Wonderfull!");

           if (isSuccess || isCompelted )
           Console.WriteLine("Excellent!");

           if (isSuccess && !isCompelted )
           Console.WriteLine("Good!");


         //--------------------------------

           int c =1;
           int d =6;
           bool sonuc = c<d;           
           Console.WriteLine(sonuc);
           sonuc = d<c;
           Console.WriteLine(sonuc);
           sonuc = d==c;
           Console.WriteLine(sonuc);
           sonuc = d>=c;
           Console.WriteLine(sonuc);
           sonuc = d<=c;

        //--------------------------------

           int g =11;
           int h =34;
           int sonuc1 = g + h;
           Console.WriteLine(sonuc1);
           sonuc1 = g + h;
           Console.WriteLine(sonuc1);
           sonuc1 = g * h;
           Console.WriteLine(sonuc1);
           sonuc1 = g / h;
           Console.WriteLine(sonuc1);
           sonuc1 = h++;
           Console.WriteLine(sonuc1);

        //--------------------------------

           int t = 20%3;
           Console.WriteLine(t);

        }
    }
}
```
</details>
