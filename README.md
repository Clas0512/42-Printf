# ft_printf

Bu proje C dilinde popüler olan `printf()` işlevinin in düşük bütçeli bir kopyasıdır. Düşük bütçeli diyorum çünkü `ft_printf`'in `printf`'den azımsanmayacak farkları var. Örneğin, bu işlev `printf`'in aksine "Buffer Yönetimi" içermez. Başka bir örnek ise, bu işlev `printf`'in desteklediği "diouxXfFeEgGaAcsb" formatlar arasından sadece 8 tanesini destekeler.

## Gereksinimler

Bu projeyi başarıyla derleyip çalıştırabilmek için aşağıdaki gereksinimlere ihtiyacınız olacaktır:

- C Derleyicisi: Proje, C programlama diliyle yazılmıştır, bu nedenle bir C derleyicisi olan GCC (GNU Compiler Collection) veya benzeri bir derleyiciye ihtiyacınız vardır. GCC genellikle Linux ve diğer Unix tabanlı sistemlerde varsayılan derleyici olarak bulunur.
- Standart C Kütüphanesi: Projenin içerdiği işlevler ve veri türleri, C dilinin standart kütüphanesine bağımlıdır. Bu kütüphane, C derleyicinizin bir parçası olarak gelir ve genellikle sistemde zaten yüklüdür.
- Make: Projeyi derlemek ve çalıştırmak için Makefile adlı bir yapılandırma dosyası bulunmaktadır. Bu dosya, derleme sürecini otomatikleştirmek için Make aracını kullanır. Dolayısıyla, sisteminizde Make aracının yüklü olduğundan emin olmanız gerekmektedir.

Yukarıdaki gereksinimlere sahip olduğunuzda, `make` komutunu kullanarak projeyi derleyebilirsiniz. Oluşturulan libftprintf.a adlı kütüphane dosyasını, projenizde kullanmak istediğiniz C dosyalarına bağlayabilir ve ft_printf işlevini kullanabilirsiniz.

Not: İlgili derleyici ve araçlar, çoğu Unix tabanlı işletim sisteminde varsayılan olarak gelir. Ancak Windows işletim sistemleri için GCC ve Make gibi araçları ayrıca yüklemeniz gerekebilir.
