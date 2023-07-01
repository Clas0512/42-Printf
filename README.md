# ft_printf

Bu proje C dilinde popüler olan `printf()` işlevinin in düşük bütçeli denebilecek bir kopyasıdır. Düşük bütçeli denebilir çünkü `ft_printf`'in `printf`'den azımsanmayacak farkları vardır. Örneğin, bu işlev `printf`'in aksine "Buffer Yönetimi" içermez. Başka bir örnek ise, bu işlev `printf`'in desteklediği "diouxXfFeEgGaAcsb" formatlar arasından sadece 8 tanesini destekler.

## Gereksinimler
- C Derleyicisi: Proje, C programlama diliyle yazılmıştır, bu nedenle bir C derleyicisi olan GCC (GNU Compiler Collection) veya benzeri bir derleyiciye ihtiyacınız vardır. GCC genellikle Linux ve diğer Unix tabanlı sistemlerde varsayılan derleyici olarak bulunur. [Buraya](https://www.mingw-w64.org/) tıklayarak indirebilirsiniz.
- Standart C Kütüphanesi: Projenin içerdiği işlevler ve veri türleri, C dilinin standart kütüphanesine bağımlıdır. Bu kütüphane, C derleyicinizin bir parçası olarak gelir ve genellikle sistemde zaten yüklüdür.
- Make: Projeyi derlemek ve çalıştırmak için Makefile adlı bir yapılandırma dosyası bulunmaktadır. Bu dosya, derleme sürecini otomatikleştirmek için Make aracını kullanır. Dolayısıyla, sisteminizde Make aracının yüklü olduğundan emin olmanız gerekmektedir.

Not: İlgili derleyici ve araçlar, çoğu Unix tabanlı işletim sisteminde varsayılan olarak gelir. Ancak Windows işletim sistemleri için GCC ve Make gibi araçları ayrıca yüklemeniz gerekebilir.

## Kurulum
1. Proje dosyalarını indirin veya bir dizinde oluşturun.
2. Terminali açın ve proje dizinine gidin.
3. Make komutunu kullanarak projeyi derleyin.

        make
   Bu komut, `libftprintf.a` adlı bir statik kütüphane dosyası oluşturacaktır.
4. Derleme başarılı olduğunda, projenizin kullanacağı C dosyasına ft_printf.h başlık dosyasını ekleyin.
5. Projeyi derleyin ve çalıştırın.

        gcc -o program_adi.c ft_printf.a
    Bu komut, `program_adi.c` adlı C dosyasını `ft_printf.a` adlı kütüphane dosyasıyla birleştirerek `program_adi` adında bir çalıştırılabilir dosya oluşturacaktır. Ayrıca çalıştırma komutu:

        ./program_adi

## Kullanım
`ft_printf` işlevi, biçimlendirme formatları ve değişken sayıda argümanlarla kullanılır. İşlev, biçimlendirme dizgisinde yer alan özel biçimlendirme belirteçlerini (%d, %s, %c vb.) işleyerek ekrana çıktı verir.

Örnek Kullanım:


    #include "ft_printf.h"

    int main()
    {
        char *str;
        int  i;

        str = "Dünya";
        i = 10;
        
        ft_printf("Merhaba, %s! Bugün %d. gün.", str, i);
        return 0;
    }
İşlev, biçimlendirme dizgisindeki yer tutuculara karşılık gelen değerleri alır ve sonucu konsola yazdırır.

### Make Komutları
- `make all`: Proje için varsayılan hedefi derler. Bu komut, `make` komutunu yalnızca çalıştırdığınızda otomatik olarak çalışır.
- `make clean`: Derleme süreciyle oluşan nesne dosyalarını temizler. Derleme dosyaları (*.o) silinir.
- `make fclean`: `make clean` komutunu çağırır ve ayrıca kütüphane dosyasını temizler. Tüm derleme dosyaları ve kütüphane (*.a) silinir.
- `make re`: `make fclean` komutunu çağırır ve ardından projeyi yeniden derler. Tüm dosyalar temizlenir ve projenin tamamı yeniden derlenir.

### Desteklenen Biçimlendirme Formatları

- `%d` veya `%i`: Tamsayıları yazdırır.
- `%u`: İşaretsiz tamsayıları yazdırır. (Unsigned)
- `%s`: Karakter dizilerini yazdırır.
- `%c`: Karakterleri yazdırır.
- `%p`: İşaretçileri (pointer) yazdırır.
- `%x`: Onaltılık (hexadecimal) tamsayıları küçük harflerle yazdırır.
- `%X`: Onaltılık (hexadecimal) tamsayıları büyük harflerle yazdırır.


# Kazanımlarım
Bu projeyi yaparken:
    `printf()` işlevini karşılaştırma yaparak daha detaylı inceledim ve Buffer Yönetiminin nasıl işlediğini gözlemledim.
    
Variadic Fonksiyonları kullanmak durumunda kaldım ve esnek ve genel amaçlı işlevler oluşturmanın nasıl mümkün olduğunu öğrendim.

---

Eğer herhangi bir sorunuz, öneriniz veya geri bildiriminiz varsa mrb.bn@hotmail.com mail adresinden bana ulaşabilirsiniz. Sorularınız için memnuniyetle yardımcı olurum :)
