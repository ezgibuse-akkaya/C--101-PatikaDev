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
1) Bir konsol uygulamasında kullanıcıdan pozitif bir sayı girmesini isteyin(n). Sonrasında kullanıcıdan n adet pozitif sayı girmesini isteyin. Kullanıcının girmiş olduğu sayılardan çift olanlar console'a yazdırın.
2) Bir konsol uygulamasında kullanıcıdan pozitif iki sayı girmesini isteyin (n, m). Sonrasında kullanıcıdan n adet pozitif sayı girmesini isteyin. Kullanıcının girmiş olduğu sayılardan m'e eşit yada tam bölünenleri console'a yazdırın.
3) Bir konsol uygulamasında kullanıcıdan pozitif bir sayı girmesini isteyin (n). Sonrasında kullanıcıdan n adet kelime girmesi isteyin. Kullanıcının girişini yaptığı kelimeleri sondan başa doğru console'a yazdırın.
4) Bir konsol uygulamasında kullanıcıdan bir cümle yazması isteyin. Cümledeki toplam kelime ve harf sayısını console'a yazdırın.

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

## :brain: Ödev 14 (Hazır Metotlar)

### :question: SORU 
Yeni bir console projesi açıp dersteki örnekleri yazınız ve ödevi tamamlayınız.
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
    
```csharp
using System;

namespace string Metot
{
    class Program
    {
        static void Main(string[] args)
        {  
         string degisken="Dersimiz CSharp, Hoşgeldiniz";
         string degisken2="dersimiz CSharp, hosgeldiniz";
         //length
         Console.WriteLine(degisken.Length);
         ////Toupper,Tolower
         Console.WriteLine(degisken.ToLower());
         Console.WriteLine(degisken.ToUpper());
         //concat(birlestirme)
         Console.WriteLine(String.Concat(degisken,"Merhaba"));
         //compare,compareTo(aynı ise 0,buyuk ise 1,kücükse -1)
         Console.WriteLine(degisken.CompareTo(degisken2));
         Console.WriteLine(string.Compare(degisken,degisken2,true));
         Console.WriteLine(string.Compare(degisken,degisken2,false));
          //contains
          Console.WriteLine(degisken.Contains(degisken2));
          Console.WriteLine(degisken.EndsWith("Hoşgelniniz"));
          Console.WriteLine(degisken.StartsWith("Merhaba"));
         //indexof
         Console.WriteLine(degisken.IndexOf("CS"));
         Console.WriteLine(degisken.IndexOf("sasa"));
         //insert
         Console.WriteLine(degisken.Insert(0,"Merhaba"));
         //lastindexof
         Console.WriteLine(degisken.LastIndexOf("i"));
         //padleft,padright
         Console.WriteLine(degisken+degisken2.PadLeft(30));
         Console.WriteLine(degisken+degisken2.PadRight(30,'*'));
         

        }
    }
}
```
</details>
             
## :brain: Ödev 15 (Hazır Metotlar)

### :question: SORU 
Yeni bir console projesi açıp dersteki örnekleri yazınız ve ödevi tamamlayınız.
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
    
```csharp
using System;

namespace Metot
{
    class Program
    {
        static void Main(string[] args)
        {  
         Console.WriteLine(DateTime.Now);
         Console.WriteLine(DateTime.Now.Date);
         Console.WriteLine(DateTime.Now.Day);
         Console.WriteLine(DateTime.Now.Month);
         Console.WriteLine(DateTime.Now.Year);
         Console.WriteLine(DateTime.Now.Hour);
         Console.WriteLine(DateTime.Now.Minute);
         Console.WriteLine(DateTime.Now.Second);
         
         Console.WriteLine(DateTime.Now.DayOfYear);
         Console.WriteLine(DateTime.Now.DayOfWeek);

         Console.WriteLine(DateTime.Now.ToLongDateString());
         Console.WriteLine(DateTime.Now.ToShortDateString());
         Console.WriteLine(DateTime.Now.ToLongTimeString());
        }
    }
}
```
</details>
        
## :brain: Ödev 16 (Koleksiyonlar)

### :question: SORU 
Yeni bir console projesi açıp dersteki örnekleri yazınız ve ödevi tamamlayınız.
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
    
```csharp
using System;
using System.Collections.Generic;
namespace Koleksiyonlar
{
    class Program
    {
        static void Main(string[] args)
        {  
        //List<T> class
        //System.Collections.Generic
        //T=>object türünde
        List<int> sayiListesi=new List<int>();
        sayiListesi.Add(23);
        sayiListesi.Add(10);
        sayiListesi.Add(4);
        sayiListesi.Add(5);
        sayiListesi.Add(92);
        sayiListesi.Add(34);

        List<string> renkListesi=new List<string>();
        renkListesi.Add("Kırmızı");
        renkListesi.Add("Mavi");
        renkListesi.Add("Turuncu");
        renkListesi.Add("Sarı");
        renkListesi.Add("Yeşil");

        //count
        Console.WriteLine(renkListesi.Count);
        Console.WriteLine(sayiListesi.Count);
        foreach (var sayi in sayiListesi)
        {
            Console.WriteLine(sayi);
        }
        foreach (var renk in renkListesi)
        {
        Console.WriteLine(renk);
        }
        sayiListesi.ForEach(sayi=>Console.WriteLine(sayi));
        renkListesi.ForEach(renk=>Console.WriteLine(renk));


        }
    }
}
```
</details>
        
## :brain: Ödevleeerrrr2 

### :question: SORU 
Aşağıdaki 3 soruyu ayrı ayrı console uygulamaları açarak yazınız. Koleksiyonlar-Soru-1, Koleksiyonlar-Soru-2, Koleksiyonlar-Soru-3 isimlerini kullanınız.

Soru - 1: Klavyeden girilen 20 adet pozitif sayının asal ve asal olmayan olarak 2 ayrı listeye atın. (ArrayList sınıfını kullanara yazınız.)

Negatif ve numeric olmayan girişleri engelleyin.
Her bir dizinin elemanlarını büyükten küçüğe olacak şekilde ekrana yazdırın.
Her iki dizinin eleman sayısını ve ortalamasını ekrana yazdırın.
Soru - 2: Klavyeden girilen 20 adet sayının en büyük 3 tanesi ve en küçük 3 tanesi bulan, her iki grubun kendi içerisinde ortalamalarını alan ve bu ortalamaları ve ortalama toplamlarını console'a yazdıran programı yazınız. (Array sınıfını kullanarak yazınız.)

Soru - 3: Klavyeden girilen cümle içerisindeki sesli harfleri bir dizi içerisinde saklayan ve dizinin elemanlarını sıralayan programı yazınız.
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
    
```csharp
using System;
using System.Collections;

namespace koleksiyonlar1
{
    class Program
    {
        static void Main(string[] args)
        {
            ArrayList asal = new ArrayList();
            ArrayList noAsal = new ArrayList();

            for (int i = 0; i < 20; i++)
            {
                System.Console.Write("Lütfen "+ (i+1)+ ". sayıyı giriniz: ");
                int sayi = Convert.ToInt32(Console.ReadLine());
                if (negatifMi(sayi))
                {
                    int sayac = 0;
                    for (int k = 2; k < sayi; k++)
                    {
                        if (sayi % k == 0)
                        {
                            sayac++;
                        }

                    }
                    if (sayac == 0)
                    {
                        if(sayac==1){
                            noAsal.Add(sayi);
                        }
                        else
                            asal.Add(sayi);
                    }
                    else
                    {
                        noAsal.Add(sayi);
                    }


                }
                else
                {
                    System.Console.WriteLine("Lütfen Pozitif ve Numeric Bir sayı Giriniz");
                }

            }
            asal.Sort();
            asal.Reverse();
            noAsal.Sort();
            noAsal.Reverse();

            System.Console.WriteLine("----------Asal Sayılar----------");

            foreach (int item in asal)
            {
                System.Console.WriteLine(item);
            }
            System.Console.WriteLine("----------Asal Olmayan Sayılar----------");
            
            foreach (var item in noAsal)
            {
                System.Console.WriteLine(item);
            }

            int toplam1=0;
            int toplam2=0;
            foreach (int item in asal)
            {
                toplam1=toplam1+item;
                    
            }
             System.Console.WriteLine("Asal Sayıların Ortalaması=  " + toplam1/asal.Count+ "  Dizideki Eleman Sayısı= "+asal.Count );
            foreach (int item in noAsal)
            {
                toplam2=toplam2+item;
                    
            }
             System.Console.WriteLine("Asal Olmayan Sayıların Ortalaması=  " + toplam1/asal.Count+ "  Dizideki Eleman Sayısı= "+noAsal.Count );
        }

        private static bool negatifMi(int s)
        {
            bool sonuc = true;
            if (s < 0)
            {
                sonuc = false;
            }

            return sonuc;`

        }
    }

}
```
```csharp
using System;
using System.Collections;

namespace Koleksiyonlar2
{
    class Program
    {
        static void Main(string[] args)
        {
            ArrayList dizi = new ArrayList();
            int[] dizi= new int[20];

            for(int i=0;i<20;i++){
                System.Console.WriteLine("Lütfen" + (i+1) +". sayıyı giriniz: ");
                int sayi = Convert.ToInt32(Console.ReadLine());
                dizi.Add(sayi);

            }
            dizi.Sort();
            
            ArrayList enKucuk=new ArrayList();
            ArrayList enBuyuk=new ArrayList();
            int sayac=1;
            foreach (var item in dizi)
            {
                if(sayac==1 || sayac==2 || sayac==3){
                    enKucuk.Add(item);
                }

                else if(sayac==18|| sayac==19 || sayac==20){
                    enBuyuk.Add(item);
                }
                sayac++;

                
            }
            
            int toplam1=0,toplam2=0 ;
            foreach (var buyuk in enBuyuk)
            {
                toplam1=toplam1+Convert.ToInt32(buyuk);
            }
            System.Console.WriteLine("En Büyük Sayıların Ortalaması: " + (toplam1/3));

            foreach (var kucuk in enKucuk)
            {
                toplam2=toplam2+Convert.ToInt32(kucuk);
            }
            System.Console.WriteLine("En Küçük Sayıların Ortalaması: " + (toplam2/3));


        }
    }
}
```
```csharp
using System;
using System.Collections;

namespace Koleksiyon3
{
    class Program
    {
        static void Main(string[] args)
        {
            ArrayList dizi = new ArrayList();
            Console.Write("Lütfen bir cümle giriniz: ");
            string metin=Console.ReadLine();
            string sesli = "aeıioöuüAEIİOÖUÜ";
            int sayac = 0;
            for (int i=0;i<metin.Length;i++)
            {
                if (sesli.Contains(metin[i]))
                {
                    sayac++;
                    dizi.Add(metin[i]);
                }

            }

            Console.WriteLine("Kelime içerisinde toplam " + sayac + " tane sesli harf var.");
            Console.WriteLine("Bunlar Şöyledir.");
            foreach (var item in dizi)
            {
                Console.WriteLine(item);
            }
        }
    }
}
```
</details>
    
## :brain: PROJE-1 (Telefon Rehberi)

### :question: SORU 
Yeni bir console uygulaması açarak telefon rehberi uygulaması yazınız. Uygulamada olması gereken özellikler aşağıdaki gibidir.

1) Telefon Numarası Kaydet
2) Telefon Numarası Sil
3) Telefon Numarası Güncelle
4) Rehber Listeleme (A-Z, Z-A seçimli)
5) Rehberde Arama

### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
Contact.cs
    
```csharp
using System;

namespace contacts_app_csharp
{
    class Contact {
        private string _firstName;
        private string _lastName;
        private string _phone;
        public Contact(string f_name, string l_name, string phone) {
            this._firstName=f_name;
            this._lastName=l_name;
            this._phone=phone;
        }
        
        public string getFirstName () {
            return this._firstName;
        }
        public string getLastName () {
            return this._lastName;
        }
        public string getPhone () {
            return this._phone;
        }
        public void setFirstName( string name) {
            this._firstName=name;
        }
        public void setLastName( string name) {
            this._lastName=name;
        }
        public void setPhone( string phone) {
            this._phone=phone;
        }
        public void ContactDetails() {
            Console.WriteLine("İsim: " + this._firstName);
            Console.WriteLine("Soyisim: " + this._lastName);
            Console.WriteLine("Telefon Numarası: " + this._phone);
        }

    }

}
```
ContactsOperations.cs
```csharp
using System;
using System.Collections.Generic;
namespace contacts_app_csharp
{
    class ContactsOperations {
        public void ViewOptions() {
            Console.WriteLine();
            Console.WriteLine("Lütfen yapmak istediğiniz işlemi seçiniz :");
            Console.WriteLine("******************************************");
            Console.WriteLine("(1) Yeni Numara Kaydetmek");
            Console.WriteLine("(2) Varolan Numarayı Silmek");
            Console.WriteLine("(3) Varolan Numarayı Güncelleme");
            Console.WriteLine("(4) Rehberi Listelemek");
            Console.WriteLine("(5) Rehberde Arama Yapmak");
            Console.WriteLine("(6) Çıkış Yapmak");
            Console.WriteLine();
        }
        public void AddContact(List<Contact> contactList) {
            Console.WriteLine("Yeni Numara Kaydetmek");
            Console.WriteLine("Lütfen isim giriniz             :");
            string first_name = Console.ReadLine();
            Console.WriteLine("Lütfen soyisim giriniz          :");
            string last_name = Console.ReadLine();
            Console.WriteLine("Lütfen telefon numarası giriniz :");
            string phone = Console.ReadLine();
            Contact newContact = new Contact(first_name, last_name, phone);
            contactList.Add(newContact);
            Console.WriteLine("Kişi rehbere eklendi");
        }

        public void DeleteContact(List<Contact> contactList) {
            Console.WriteLine("Silmek istediğiniz kişinin adını ya da soyadını giriniz: ");
            Console.WriteLine("Lütfen isim giriniz   :");
            string first_name = Console.ReadLine();
            Console.WriteLine("Lütfen soyisim giriniz:");
            string last_name = Console.ReadLine();
            var contact = contactList.Find( 
                x => x.getFirstName() == first_name ||
                x.getLastName() == last_name  );
            if(contact != null) {
                Console.WriteLine(contact.getFirstName() + " " + contact.getLastName() 
                + " isimli kişi rehberden silinmek üzere, onaylıyor musunuz ?(y/n)");
                string confirmation = Console.ReadLine();
                if(confirmation == "y" || confirmation == "yes" ){
                    contactList.Remove(contact);
                    Console.WriteLine("Kişi rehberden silindi");
                }
            }
            else{
                Console.WriteLine("Aradığınız kriterlere uygun veri rehberde bulunamadı. Lütfen bir seçim yapınız.");
                Console.WriteLine("* Silmeyi sonlandırmak için : (1)");
                Console.WriteLine("* Yeniden denemek için      : (2)");
                int option = Convert.ToInt16(Console.ReadLine());
                if (option == 2) {
                    DeleteContact(contactList);
                } 
            }
        }

        public void UpdateContact(List<Contact> contactList) {
            Console.WriteLine(" Lütfen numarasını güncellemek istediğiniz kişinin adını ya da soyadını giriniz: ");
            Console.WriteLine("Lütfen isim giriniz    :");
            string first_name = Console.ReadLine();
            Console.WriteLine("Lütfen soyisim giriniz :");
            string last_name = Console.ReadLine();

            var contact = contactList.Find( 
                x => x.getFirstName() == first_name ||
                x.getLastName() == last_name  );

            if(contact != null) {
                Console.WriteLine("Bulunan kişi: ");
                Console.WriteLine();
                Console.WriteLine("İsim".PadRight(15, ' ') + "Soyisim".PadRight(15, ' ') + "Telefon".PadRight(15, ' ') );
                Console.WriteLine("*".PadRight(44, '*'));
                Console.WriteLine(
                    contact.getFirstName().PadRight(15, ' ') 
                    + contact.getLastName().PadRight(15, ' ') 
                    + contact.getPhone().PadRight(15, ' '));

                //Güncellenecek veri isteniyor
                Console.WriteLine("Lütfen yeni isim giriniz    :");
                string new_first_name = Console.ReadLine();
                Console.WriteLine("Lütfen yeni soyisim giriniz :");
                string new_last_name = Console.ReadLine();
                Console.WriteLine("Lütfen yeni numara giriniz :");
                string new_phone = Console.ReadLine();
                if (new_first_name != "" || new_last_name != "" || new_phone != "" ) {
                    if(new_first_name != "") {
                        contact.setFirstName(new_first_name); }
                    if(new_last_name != "") {
                        contact.setLastName(new_last_name); }
                    if(new_phone != "") {
                        contact.setPhone(new_phone);}

                    Console.WriteLine("Güncelleme tamamlandı");
                }
         }
         else {
            Console.WriteLine("Aradığınız kriterlere uygun veri rehberde bulunamadı. Lütfen bir seçim yapınız.");
            Console.WriteLine("* Güncellemeyi sonlandırmak için:(1)");
            Console.WriteLine("* Yeniden denemek için          :(2)");
            int option = Convert.ToInt16(Console.ReadLine());
                if (option == 2) {
                    UpdateContact(contactList);
                }
         }
        }

        public void ViewContacts(List<Contact> contactList) {
            Console.WriteLine("Rehberi Listelemek");
            Console.WriteLine("*".PadRight(44, '*'));
            Console.WriteLine("İsim".PadRight(15, ' ') + "Soyisim".PadRight(15, ' ') + "Telefon".PadRight(15, ' ') );
            Console.WriteLine();
            foreach (var item in contactList) 
                {
                    Console.WriteLine(
                        item.getFirstName().PadRight(15, ' ') 
                        + item.getLastName().PadRight(15, ' ') 
                        + item.getPhone().PadRight(15, ' '));
                }
        }

        public void ViewContact(List<Contact> contactList) {
            Console.WriteLine("Arama yapmak istediğiniz tipi seçiniz.");
            Console.WriteLine(" **********************************************");
            Console.WriteLine("İsim veya soyisime göre arama yapmak için: (1)");
            Console.WriteLine("Telefon numarasına göre arama yapmak için: (2)");
            int option = Convert.ToInt16(Console.ReadLine()); 
            if (option==1) {
                Console.WriteLine("Lütfen isim giriniz   :");
                string first_name = Console.ReadLine();
                Console.WriteLine("Lütfen soyisim giriniz:");
                string last_name = Console.ReadLine();

                var contact = contactList.Find( 
                x => x.getFirstName() == first_name ||
                x.getLastName() == last_name );
                if(contact!=null) {
                    Console.WriteLine("Bulunan Kişi: ");
                    Console.WriteLine();
                    Console.WriteLine("İsim".PadRight(15, ' ') + "Soyisim".PadRight(15, ' ') + "Telefon".PadRight(15, ' ') );
                    Console.WriteLine("*".PadRight(44, '*'));
                    
                    Console.WriteLine(
                    contact.getFirstName().PadRight(15, ' ') 
                    + contact.getLastName().PadRight(15, ' ') 
                    + contact.getPhone().PadRight(15, ' '));

                }
                else {
                    Console.WriteLine("Kişi bulunamadı");
                }
            }
            else if (option ==2) {
                Console.WriteLine("Lütfen telefon numarası giriniz:");
                string phone = Console.ReadLine();
                var contact = contactList.Find( 
                x => x.getPhone() == phone );
                
                if(contact!=null) {
                    Console.WriteLine("Bulunan kişi: ");
                    Console.WriteLine();
                    Console.WriteLine("İsim".PadRight(15, ' ') + "Soyisim".PadRight(15, ' ') + "Telefon".PadRight(15, ' ') );
                    Console.WriteLine("*".PadRight(44, '*'));
                    
                    Console.WriteLine(
                    contact.getFirstName().PadRight(15, ' ') 
                    + contact.getLastName().PadRight(15, ' ') 
                    + contact.getPhone().PadRight(15, ' '));
                }
                else {
                    Console.WriteLine("Kişi bulunamadı");
                }
            }
        }
    }   
}
```
Program.cs
```csharp
using System;
using System.Collections.Generic;
namespace contacts_app_csharp
{
    class Program
    {
        static void Main(string[] args)
        {   
            int operation=0;
            List<Contact> contactsList = new List<Contact>();
            ContactsOperations ops = new ContactsOperations();
            contactsList.Add(new Contact("Seda", "Demir", "05555555555"));
            contactsList.Add(new Contact("Gazihan", "Demir", "05555555455"));
            contactsList.Add(new Contact("Ece", "Demir", "05555555554"));
            contactsList.Add(new Contact("Nazlı", "Yılmaz", "05555555445"));

            do {
                ops.ViewOptions();
                operation = Convert.ToInt16(Console.ReadLine());
                switch(operation) {
                    case 1: 
                        ops.AddContact(contactsList);
                        break;
                    case 2: 
                        ops.DeleteContact(contactsList);
                        break;
                    case 3:
                        ops.UpdateContact(contactsList);
                        break;
                    case 4: 
                        ops.ViewContacts(contactsList);
                        break;
                    case 5: 
                        ops.ViewContact(contactsList);
                        break;
                }
        } while (Convert.ToInt16(operation) != 6 );
       

        }
    }
}
```
</details>
    
## :brain: Proje 2 (ToDo Uygulaması)

### :question: SORU 
Yeni bir console uygulaması açarak bir 3 kolondan oluşan bir TODO uygulaması yazınız. Uygulamada olması gereken özellikler aşağıdaki gibidir.

1) Kart Ekle
2) Kart Güncelle
3) Kart Sil
4) Kart Taşı
5) Board Listeleme
### :green_square: CEVAP

<details>
<summary>Kodu görmek için tıklayınız.</summary>
    
Duration.cs
```csharp
namespace todo_app_csharp{

    public enum Duration {
        XS =1,
        S =2, 
        M=3, 
        L=4, 
        X=5,
    }
    
}
```
Member.cs
```csharp

namespace todo_app_csharp
{
    class Member
    {
        //TODO: create a member collection
        private string _firstName;
        private string _lastName;
        private int _id;

        public Member(int id, string fname, string lname) {
            this._firstName = fname;
            this._lastName = lname;
            this._id = id;
        }
    }    
    
}
```
Program.cs
```csharp
using System;
using System.Collections.Generic;
namespace todo_app_csharp
{
    class Program
    {
        static void Main(string[] args)
        {   
            TodoOperations ops = new TodoOperations();

            //Constructor format: 
            // str title, str content, int duration, int member_id, int status)
            Todo todo1 = new Todo("todo app", "c sharp", 2, 1, 1);
            Todo todo2 = new Todo("contacts app", "c#", 1, 2, 2);
            Todo todo3 = new Todo("coderbyte challange", "c sharp", 1, 2);
            
            List<Todo> todoList = new List<Todo>();

            todoList.Add(todo1);
            todoList.Add(todo2);
            todoList.Add(todo3);

            int operation = 0;
            do {
                Console.WriteLine("Lütfen yapmak istediğiniz işlemi seçiniz:");
                Console.WriteLine("*****************************************");
                Console.WriteLine("(1) Board Listelemek");
                Console.WriteLine("(2) Board'a Kart Eklemek");
                Console.WriteLine("(3) Board'dan Kart Silmek");
                Console.WriteLine("(4) Kart Taşımak");
                Console.WriteLine("(5) Çıkış yapmak");
                
                operation = Convert.ToInt16(Console.ReadLine());
                switch(operation) {
                    case 1: 
                        ops.ViewTodoList(todoList);
                        break;
                    case 2: 
                        ops.AddTodo(todoList);
                        break;
                    case 3:
                        ops.DeleteTodo(todoList);
                        break;
                    case 4: 
                        ops.UpdateStatus(todoList);
                        break;
                }
        } while (Convert.ToInt16(operation) != 5  );
    
        }
    }
}
```
ToDo.cs
```csharp
using System;
using System.Collections.Generic;
namespace todo_app_csharp
{
    class Program
    {
        static void Main(string[] args)
        {   
            TodoOperations ops = new TodoOperations();

            //Constructor format: 
            // str title, str content, int duration, int member_id, int status)
            Todo todo1 = new Todo("todo app", "c sharp", 2, 1, 1);
            Todo todo2 = new Todo("contacts app", "c#", 1, 2, 2);
            Todo todo3 = new Todo("coderbyte challange", "c sharp", 1, 2);
            
            List<Todo> todoList = new List<Todo>();

            todoList.Add(todo1);
            todoList.Add(todo2);
            todoList.Add(todo3);

            int operation = 0;
            do {
                Console.WriteLine("Lütfen yapmak istediğiniz işlemi seçiniz:");
                Console.WriteLine("*****************************************");
                Console.WriteLine("(1) Board Listelemek");
                Console.WriteLine("(2) Board'a Kart Eklemek");
                Console.WriteLine("(3) Board'dan Kart Silmek");
                Console.WriteLine("(4) Kart Taşımak");
                Console.WriteLine("(5) Çıkış yapmak");
                
                operation = Convert.ToInt16(Console.ReadLine());
                switch(operation) {
                    case 1: 
                        ops.ViewTodoList(todoList);
                        break;
                    case 2: 
                        ops.AddTodo(todoList);
                        break;
                    case 3:
                        ops.DeleteTodo(todoList);
                        break;
                    case 4: 
                        ops.UpdateStatus(todoList);
                        break;
                }
        } while (Convert.ToInt16(operation) != 5  );
    
        }
    }
}
```
ToDoOperations.cs
```csharp
using System;
using System.Collections.Generic;
namespace todo_app_csharp
{
    class TodoOperations
    {   

        public void ViewTodoList(List<Todo> todoList) {
            Console.WriteLine();
            FindResults(todoList, 0); // View "Todo" line
            FindResults(todoList, 1); // View "In progress" line
            FindResults(todoList, 2); // View "Done" line
        }
        public void FindResults(List<Todo> todoList, int status) {
            // List todos based on their status (TODO, IN POGRESS, DONE)
            List<Todo> results = todoList.FindAll(todo=> todo.GetStatus() == status);
            if(status==0){
                Console.WriteLine("TODO Line");
                Console.WriteLine("************************");
            }
            else if(status==1) {
                Console.WriteLine("IN PROGRESS Line");
                Console.WriteLine("************************");
            }
            else if(status==2) {
                Console.WriteLine("DONE Line");
                Console.WriteLine("************************");
            }

            if (results.Count==0) {
                Console.WriteLine("~ BOŞ ~");
                Console.WriteLine();
            }
            else {
                foreach (var todo in results) {
                    todo.TodoDetails();
                    Console.WriteLine();
                }
            }

        }
    
        public void AddTodo(List<Todo> todoList) {
            Console.WriteLine();
            Console.Write("Başlık Giriniz                                  :");
            string title = Console.ReadLine();
            Console.WriteLine();
            Console.Write("İçerik Giriniz                                  :");
            string content = Console.ReadLine();
            Console.WriteLine();
            Console.Write("Büyüklük Seçiniz -> XS(1),S(2),M(3),L(4),XL(5)  :");
            int drtn = Convert.ToInt16(Console.ReadLine());
            Console.WriteLine();
            Console.Write("Kişi Seçiniz                                    :");
            try {
                int person = Convert.ToInt16(Console.ReadLine()); 
                todoList.Add(new Todo(title, content, drtn, person));
                Console.WriteLine();
                ViewTodoList(todoList);
            }
            catch {
                Console.WriteLine("Hatalı girişler yaptınız!");
            }      
        }
        public void UpdateStatus(List<Todo> todoList) {
            Console.WriteLine("Öncelikle taşımak istediğiniz kartı seçmeniz gerekiyor.");
            Console.Write("Lütfen kart başlığını yazınız: ");
            string input = Console.ReadLine();

            List<Todo> result = todoList.FindAll(x=> x.GetTitle() == input);

            if(result.Count != 0 ){
                Console.WriteLine();
                Console.WriteLine("Bulunan Kart Bilgileri:");
                Console.WriteLine("**************************************");
                Console.WriteLine();
                foreach (Todo item in result)
                {   
                    item.TodoDetails();
                    if(item.GetStatus()==0) {Console.WriteLine("Line        :" + "TODO");}
                    else if(item.GetStatus()==1) {Console.WriteLine("Line        :" + "IN PROGRESS");}
                    else if(item.GetStatus()==2) {Console.WriteLine("Line        :" + "DONE");}
                }
                Console.WriteLine();
                Console.WriteLine("Lütfen taşımak istediğiniz Line'ı seçiniz: ");
                Console.WriteLine("(1) TODO");
                Console.WriteLine("(2) IN PROGRESS");
                Console.WriteLine("(3) DONE");
                int option = Convert.ToInt16(Console.ReadLine());
                if(option == 1 || option==2 || option==3) { 
                    option--;
                    todoList.Find(x=> x.GetTitle() == input).SetStatus((option));
                    Console.WriteLine("Taşıma işlemi tamamlandı");
                    ViewTodoList(todoList);
                }
                else {Console.WriteLine("Hatalı bir seçim yaptınız!");}    
            }
            else {
                Console.WriteLine("Aradığınız kriterlere uygun kart board'da bulunamadı. Lütfen bir seçim yapınız.");
                Console.WriteLine("* İşlemi sonlandırmak için : (1)");
                Console.WriteLine("* Yeniden denemek için : (2)");
                int option = Convert.ToInt16(Console.ReadLine());
                if(option == 2) { UpdateStatus(todoList);}
                else {Console.WriteLine("Taşıma işlemi iptal edildi.");}
            }
        }

        public void DeleteTodo(List<Todo> todoList){
            Console.WriteLine("Öncelikle silmek istediğiniz kartı seçmeniz gerekiyor.");
            Console.Write("Lütfen kart başlığını yazınız: ");
            string input = Console.ReadLine();

            List<Todo> result = todoList.FindAll(x=> x.GetTitle() == input);

            if(result.Count != 0 ){
                foreach (Todo item in result)
                {
                    todoList.Remove(item);
                }
                Console.WriteLine("Silme işlemi tamamlandı");
            }
            else {
                Console.WriteLine("Aradığınız krtiterlere uygun kart board'da bulunamadı. Lütfen bir seçim yapınız.");
                Console.WriteLine("* Silmeyi sonlandırmak için : (1)");
                Console.WriteLine("* Yeniden denemek için : (2)");
                int option = Convert.ToInt16(Console.ReadLine());
                if(option == 2) { DeleteTodo(todoList);}
                else {Console.WriteLine("Silme işlemi iptal edildi.");}
            }
            
        }

    }
}
```
</details>
    

