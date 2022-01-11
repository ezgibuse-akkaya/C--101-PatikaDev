# CSharp-101-PatikaDev

[Patika.dev](https://app.patika.dev/egitimler) adresindeki "C# 101" eğitiminde kullandığım kaynak kodları içeren bir repo.

Bu README dosyasında Patika.Dev C# Ödev Soruları Ve Yanıtlarını bulacaksınız.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## :brain: Ödev 1 (değişkenler)

### :question: SORU 
Yeni bir console projesi açıp dersteki örnekleri yazınız ve ödevi tamamlayınız.
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
    
```csharp
    
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

## :brain: Ödev 2 (operatörler)
### :question: SORU 
Yeni bir console projesi açıp dersteki örnekleri yazınız ve ödevi tamamlayınız.
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
    
```csharp
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
    
## :brain: Ödev 3 (tip dönüşümleri)

### :question: SORU 
Yeni bir console projesi açıp dersteki örnekleri yazınız ve ödevi tamamlayınız.
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
    
```csharp
using System;

namespace Tip_Donusumleri
{
    class Program
    {
        static void Main(string[] args)
        {
            byte x = 1;
            sbyte y = 2;
            short z = 3;

            int v = x+y+z;
            Console.WriteLine("v:"+v);

            long a = v;
            Console.WriteLine("a:"+ a);

            float b = a;
            Console.WriteLine("b:"+b);

            string c = "alperen";
            char d = 'f';
            object e = c+d+v;
            Console.WriteLine("e:"+e);

           Console.WriteLine("------------------------");
          

           int r = 3;
           byte t = (byte)r;
           Console.WriteLine("t:"+t);
           
           float j = 5.2f;
           byte l =(byte)j;
           Console.WriteLine("l:"+l);

           Console.WriteLine("------------------------");

           int abc = 9;
           string xyz = "5";
           int yy = abc + Convert.ToInt32(xyz);
            Console.WriteLine(yy);

            int def = 9;
           string ghj = def.ToString();
            Console.WriteLine("ghj:"+ghj);
            ParseMethod();
        }

        public static void ParseMethod()
        {

           string yazi1 = "6";
           string yazi2 = "9";
           int sayi1;
           double sayi2,toplam;

           sayi1 = Int32.Parse(yazi1);
           sayi2 = Double.Parse(yazi2);
           toplam = Convert.ToDouble(sayi1)+sayi2;
           Console.WriteLine(toplam);
        }
    }
}
```
</details>

## :brain: Ödev 4 (hata yönetimi)

### :question: SORU 
Yeni bir console projesi açıp dersteki örnekleri yazınız ve ödevi tamamlayınız.
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
    
```csharp
using System;

namespace HataYonetimi
{
    class Program
    {
        static void Main(string[] args)
        {
            try{
          Console.WriteLine("Bir sayı griniz: ");
          int sayi=Convert.ToInt32(Console.ReadLine());
          Console.WriteLine("Girmiş olduğunuz sayi: " +sayi);

            }
            catch(Exception ex){
            Console.WriteLine("Hata" +ex.Message.ToString());
            }
            //finally{
            //Console.Write("İşlem Tamamlandı");
            //}
            try{
            //int a=int.Parse(null);
            //int a=int.Parse("test");
            int a=int.Parse("-141415161718");

            }
            catch(ArgumentNullException ex) {
            Console.WriteLine("Boş değer Girdiniz.");
            Console.WriteLine(ex);
            }
            catch(FormatException ex){
            Console.WriteLine("Veri Tipi Uygun Değil.");
            Console.WriteLine(ex);
            }
            catch(OverflowException ex){
            Console.WriteLine("Çok küçük veya çok büyük bir değer girdiniz.");
            Console.WriteLine(ex);
            }
            finally{
                Console.WriteLine("İşlem Başarıyla Tamamlandı");
            }
        }
    }
}
```
</details>

## :brain: Ödev 5 (Karar Yapıları)

### :question: SORU 
Yeni bir console projesi açıp dersteki örnekleri yazınız ve ödevi tamamlayınız.
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
    
```csharp
using System;

namespace KararYapilari
{
    class Program
    {
        static void Main(string[] args)
        {
           int time=DateTime.Now.Hour;
           if(time>=6 && time<11){
               Console.WriteLine("Günaydın");
           }
           else if(time<=18)
           {
               Console.WriteLine("İyi Günler");
           }
           else{
               Console.WriteLine("İyi Geceler");
           string sonuc=time<=18 ? "İyi Günler" : "İyi Geceler";
          
           sonuc=time>=6 &&  time<11 ? "Günaydin" :time<=18 ? "İyi Günler" : "İyi Geceler";
           Console.WriteLine(sonuc);
           }

        }
    }
}
```
</details>

## :brain: Ödev 6 (karar yapıları 2)

### :question: SORU 
Yeni bir console projesi açıp dersteki örnekleri yazınız ve ödevi tamamlayınız.
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
    
```csharp
using System;

namespace Karar_Yapilari
{
    class Program
    {
        static void Main(string[] args)
        {
           int mounth=DateTime.Now.Month;
           //expression
           switch (mounth)
           {
               case 1:
                Console.WriteLine("Ocak Ayındasınız");
                break;
                 case 2:
                Console.WriteLine("Şubat Ayındasınız");
                break;
                 case 3:
                Console.WriteLine("Mart Ayındasınız");
                break;
                 case 4:
                Console.WriteLine("Nisan Ayındasınız");
                break;
               
               default:
               Console.WriteLine("Yanlış Veri Girişi");
               break;
           }
           switch (mounth)
           {
               case 12:
               case 1:
               case 2:
            Console.WriteLine("Kış Ayındasınız");
            break;
            case 3:
               case 4:
               case 5:
            Console.WriteLine("İlkbahar Ayındasınız");
            break;
            case 6:
               case 7:
               case 8:
            Console.WriteLine("Yaz Ayındasınız");
            break;
            case 9:
               case 10:
               case 11:
            Console.WriteLine("Sonbahar Ayındasınız");
            break;
          
               default:
               break;
           }
        }
    }
}
```
</details>

## :brain: Ödev 7 (döngüler)

### :question: SORU 
Yeni bir console projesi açıp dersteki örnekleri yazınız ve ödevi tamamlayınız.
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
    
```csharp
using System;

namespace Donguler
{
    class Program
    {
        static void Main(string[] args)
        {
            //EKRANDAN GİRİLEN SAYIYA KADAR OLAN TEK SAYILAR
            Console.Write("Lütfen bir sayı giriniz: ");
            int sayac=int.Parse(Console.ReadLine());
            for(int i=1;i<=sayac;i++)
            {
                //komutlar
               if(i%2==1) {
                Console.WriteLine(i);
            }
            //1-1000 arasındaki tek ve cift sayıların toplamı
            int tekToplam=0;
            int ciftToplam=0;
        for (int i = 0; i < 1000; i++)
        {
          if(i%2==1){
              tekToplam+=1;
        
          } 
          else 
          ciftToplam+=1; 
        }
        Console.WriteLine("Tek Toplam:" +tekToplam);
        Console.WriteLine("Çift Toplam:" +ciftToplam);
            
        //break, continue
        for (int i = 0; i < 10; i++)
        {
            if(i==4){
                break;
                Console.WriteLine(i);
            }
             }
             for (int i = 0; i < 10; i++)
        {
            if(i==4){
                continue;
                Console.WriteLine(i);
           
        }
        }
       }
}
```
</details>
    
## :brain: Ödev 8 (döngüler 2)

### :question: SORU 
Yeni bir console projesi açıp dersteki örnekleri yazınız ve ödevi tamamlayınız.
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
    
```csharp
using System;

namespace Donguler
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Lütfen bir sayi giriniz: ");
            //1 den baslayarak console dan girilen sayıya kadar ortalama hesaplayıp console a yazdıran program
            int sayi=int.Parse(Console.ReadLine());
            int sayac=1;
            int toplam=0;
           while (sayac<=sayi)
           {
               toplam+=sayac;
               sayac++; 
           }
           Console.WriteLine(toplam/sayi);
        
        //a-z tüm harfleri yaz
        char karakter='a';
        while (karakter<'z')
        {
             Console.Write(karakter);
             karakter++;
        }
        //foreach
        string [] arabalar={"BMW", "Ford","Toyota","Nissan"};
        foreach (var araba in arabalar)
        {
            Console.WriteLine(araba);
        }
        }
       }
}
```
</details>

## :brain: Ödev 9 (Diziler)

### :question: SORU 
Yeni bir console projesi açıp dersteki örnekleri yazınız ve ödevi tamamlayınız.
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
    
```csharp
using System;

namespace Diziler
{
    class Program
    {
        static void Main(string[] args)
        {
           //dizi tanımlama
           string[] renkler=new string[5];
           string[] hayvanlar={"kedi","köpek","kuş"};
           int[] dizi;
           dizi= new int[5];
           //dizilere değer atama ve erişim
           renkler[0]="Mavi";
           dizi[3]=10;
           Console.WriteLine(dizi[3]);
           Console.WriteLine(hayvanlar[0]);

           //döngülerle dizi kullanımı
           //klavyeden girilen n tane sayının ortalamasını alan program
           Console.WriteLine("Lütfen dizini eleman sayısını giriniz: ");
           int diziUzunlugu=int.Parse(Console.ReadLine());
           int[] sayiDizisi=new int[diziUzunlugu];
           for (int i = 0; i < diziUzunlugu; i++)
           {
               Console.WriteLine("Lütfen {0}. sayıyı giriniz: ",i+1);
               sayiDizisi[i]=int.Parse(Console.ReadLine());

           }
           int toplam=0;
           foreach (var sayi in sayiDizisi)
           {
             toplam+=sayi;
             Console.WriteLine("Ortalama", toplam/diziUzunlugu);
               
           }
        }
       }
 }
 ```
</details>   
    
## :brain: Ödev 10 (diziler 2)

### :question: SORU 
Yeni bir console projesi açıp dersteki örnekleri yazınız ve ödevi tamamlayınız.
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
    
```csharp
using System;

namespace Diziler
{
    class Program
    {
        static void Main(string[] args)
        {
            //sort
         int [] sayiDizisi={23,12,4,86,72,3,11,17};
         Console.WriteLine("sırasız dizi");
         foreach (var sayi in sayiDizisi)
         {
             Console.WriteLine(sayi);
             
         }
         Console.WriteLine("sıralı dizi");
         Array.Sort(sayiDizisi);
         foreach (var sayi in sayiDizisi)
         {
             Console.WriteLine(sayi);
         }
         //clear
         //ikinci indexten sonra 2 tane 0 yapar
                  Console.WriteLine("array clear ");
                  Array.Clear(sayiDizisi,2,2);
                  foreach (var sayi in sayiDizisi)
                  {
                      Console.WriteLine(sayi);
                  }
          //reverse
          //elemanları tersine cevirir
          Array.Reverse(sayiDizisi);
          foreach (var sayi in sayiDizisi)
          {
              Console.WriteLine(sayi);
              
          }
          //indexOf
            Console.WriteLine(Array.IndexOf(sayiDizisi,23));
         //resize
         Array.Resize<int>(ref sayiDizisi,9);
         sayiDizisi[8]=99;
         foreach (var sayi in sayiDizisi)
         {
             Console.WriteLine(sayi);
         }
        }
       }
}
```
</details>

## :brain: Ödev 11 (Metotlar)

### :question: SORU 
Yeni bir console projesi açıp dersteki örnekleri yazınız ve ödevi tamamlayınız.
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
    
```csharp
using System;

namespace Metotlar
{
    class Program
    {
        static void Main(string[] args)
        {
                //erişimbelirtec,geridönüştipi,metotsdi(parametreListesi/arguman)   
                //(
                    //komutlar;
                    //return;
                //)
                int a=2;
                int b=3;
            
                Console.WriteLine(a+b);
            int sonuc=Topla(a,b);
            Console.WriteLine(sonuc);    
            
            Metotlar ornek=new Metotlar();
            ornek.ekranaYazdir(Convert.ToString(sonuc));

            int sonuc2=ornek.ArttırVeTopla(ref a, ref b);
            ornek.ekranaYazdir(Convert.ToString(sonuc2));
            ornek.ekranaYazdir(Convert.ToString(a+b));

        }
       static int Topla(int deger1,int deger2);
          {
            return (deger1 + deger2);
          }
        }
        class Metotlar{
           public void ekranaYazdir(string veri)
            {
                Console.WriteLine(veri);
            }
    public int ArttırVeTopla( ref int deger1,ref int deger2)
    {
        deger1+=1;
        deger2+=2;
        return deger1+deger2;
    }
        }
}
```
</details>

## :brain: Ödev 12 (Metotlar)

### :question: SORU 
Yeni bir console projesi açıp dersteki örnekleri yazınız ve ödevi tamamlayınız.
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
    
```csharp
using System;

namespace Metot_Overloading
{
    class Program
    {
        static void Main(string[] args)
        {  
         //out parametreler
         string sayi="999";

         bool sonuc=int.TryParse(sayi,out int outSayi);
         if(sonuc){
             Console.WriteLine("Başarılı");
             Console.WriteLine(outSayi);
         }
         else{
             Console.WriteLine("Başarısız");
            }
         Metotlar instence=new Metotlar();
         instence.Topla(4,5, out int ToplamSonucu);
         Console.WriteLine(ToplamSonucu);
         //metot asırı yüklenme-overloading

         int ifade=999;
         instence.ekranaYazdir(Convert.ToString(ifade));
         instence.ekranaYazdir("ezgi","buse");
        //metod imzası
        //metotadi+parametre sayisi+parametre
        }
       }
       class Metotlar{
           public void Topla(int a, int b, out int toplam){
               toplam=a+b;
           }
           public void ekranaYazdir(string veri){
               Console.WriteLine(veri);
           }
            public void ekranaYazdir(string veri,string veri2){
               Console.WriteLine(veri+veri2);
           }
       }
}
```
</details>
    
## :brain: Ödev 13 (Metotlar)

### :question: SORU 
Yeni bir console projesi açıp dersteki örnekleri yazınız ve ödevi tamamlayınız.
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
    
```csharp
using System;

namespace Recursive_Extension
{
    class Program
    {
        static void Main(string[] args)
        {  
          //recursive-özyinelemeli
          //3^4
          int result=1;
          for (int i = 0; i < 5; i++)
          {
              result=result*3;
              Console.WriteLine(result);
              islemler instence=new();
              Console.WriteLine(instence.Expo(3,4));

              //extension metotlar
              string ifade="Ezgi Buse Akkaya";
              bool sonuc=ifade.CheckSpaces();
              Console.WriteLine(sonuc);
              if(sonuc){
                  Console.WriteLine(ifade.RemoveWhiteSpaces());
              }
          }
        }
        public class islemler{
            public int Expo(int sayi,int us){
                if(us<2)
                return sayi;
                return Expo(sayi,us-1)*sayi;
            }
            
                 
            }
            public static class Extension{
                public static bool CheckSpaces(this string param){
                  return param.Contains(" ");
                }
            }
            public static string RemoveWhiteSpaces(this string param){
                string[] dzi=param.Split(" ");
                return string.Join("",dizi);
            }
            }
}
```
</details>
       
## :brain: Ödevleeerrrr

### :question: SORU 
Bir konsol uygulamasında kullanıcıdan pozitif bir sayı girmesini isteyin(n). Sonrasında kullanıcıdan n adet pozitif sayı girmesini isteyin. Kullanıcının girmiş olduğu sayılardan çift olanlar console'a yazdırın.
Bir konsol uygulamasında kullanıcıdan pozitif iki sayı girmesini isteyin (n, m). Sonrasında kullanıcıdan n adet pozitif sayı girmesini isteyin. Kullanıcının girmiş olduğu sayılardan m'e eşit yada tam bölünenleri console'a yazdırın.
Bir konsol uygulamasında kullanıcıdan pozitif bir sayı girmesini isteyin (n). Sonrasında kullanıcıdan n adet kelime girmesi isteyin. Kullanıcının girişini yaptığı kelimeleri sondan başa doğru console'a yazdırın.
Bir konsol uygulamasında kullanıcıdan bir cümle yazması isteyin. Cümledeki toplam kelime ve harf sayısını console'a yazdırın.

### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
    
```csharp
using System;

namespace Odev_1
{
    class Program
    {
        static void Main(string[] args)
        {
            /* 1- Bir konsol uygulamasında kullanıcıdan pozitif bir sayı girmesini isteyin(n). 
             * Sonrasında kullanıcıdan n adet pozitif sayı girmesini isteyin. 
             * Kullanıcının girmiş olduğu sayılardan çift olanlar console'a yazdırın.
             

            Console.Write("Bir pozitif sayı adeti giriniz: ");           
            int n = Convert.ToInt32(Console.ReadLine());
            if(n > 0)
            {
                int[] array = new int[n];
                for (int i = 0; i < n; i++)
                {
                    Console.WriteLine("Bir sayı giriniz: ");
                    int sayi = Convert.ToInt32(Console.ReadLine());
                    array[i] = sayi;                   
                }
                for (int j = 0; j < n; j++)
                {
                    if(array[j] % 2 == 0)
                    {
                        Console.WriteLine(array[j]);
                    }
                }

            }

            

            2 - Bir konsol uygulamasında kullanıcıdan pozitif iki sayı girmesini isteyin(n, m).
            Sonrasında kullanıcıdan n adet pozitif sayı girmesini isteyin.
            Kullanıcının girmiş olduğu sayılardan m'e eşit yada tam bölünenleri console'a yazdırın.
            

            Console.Write("Bir pozitif sayı giriniz: ");
            int n = Convert.ToInt32(Console.ReadLine());
            Console.Write("Bir pozitif sayı giriniz: ");
            int m = Convert.ToInt32(Console.ReadLine());

            int[] array = new int[n];
            for (int i = 0; i < n; i++)
            {
                Console.Write("Bir sayı giriniz: ");
                array[i] = Convert.ToInt32(Console.ReadLine());
            }

            for (int i = 0; i < n; i++)
            {
                if (m == array[i] || m % array[i] == 0)
                {
                    Console.WriteLine(array[i]);
                }
            }

            3 - Bir konsol uygulamasında kullanıcıdan pozitif bir sayı girmesini isteyin(n).
                Sonrasında kullanıcıdan n adet kelime girmesi isteyin.
                Kullanıcının girişini yaptığı kelimeleri sondan başa doğru console'a yazdırın.

            

            Console.Write("Bir pozitif sayı giriniz: ");
            int n = Convert.ToInt32(Console.ReadLine());
            string[] array = new string[n];
            for (int i = 0; i < n; i++)
            {
                Console.Write("Bir kelime giriniz: ");
                array[i] = Convert.ToString(Console.ReadLine());
            }

            foreach (var i in array)
            {
                Console.WriteLine(i);
            }

            Console.WriteLine("******************************");
            Array.Reverse(array);

            foreach(var i in array)
            {
                Console.WriteLine(i);
            }

            

            4 - Bir konsol uygulamasında kullanıcıdan bir cümle yazması isteyin.
                Cümledeki toplam kelime ve harf sayısını console'a yazdırın.

            */

            Console.WriteLine("Bir cümle giriniz: ");
            string cumle = Convert.ToString(Console.ReadLine());

            string[] parcalanmısCumle = cumle.Split(" ");
            char[] harfler = cumle.ToCharArray();
            int kelimeToplami = 0;
            int harfToplami = 0;


            foreach (var item in parcalanmısCumle)
            {
                kelimeToplami++;
            }

            foreach (var item in harfler)
            {
                if(item == ' ')
                {
                    continue;
                }
                harfToplami++;
            }

            Console.WriteLine("Kelime sayısı: " +kelimeToplami);
            Console.WriteLine("Harf Toplamı: " +harfToplami);


        }
    }
}
```
</details>
