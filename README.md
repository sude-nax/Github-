Versiyon Kontrol Sistemi Nedir? 
Bir dosya ya da kümedeki değişiklikleri takip edebilmek için bir yöntemdir. Herhangi bir anda üzerinde çalıştığımız dosyaların o anki hallerini kaydedip istediğimiz zaman o ana geri dönme imkanı verir. Git dediğimiz olayda bu yapılan değişikliklerin içeriğini biim için takip edip kaydeder.

Git Nedir ve Neden Kullanmalıyız?
Git, yazılım geliştirme süreçlerinde kullanılan bir versiyon kontrol sistemidir. Git sayesinde yapacağımız projelerin adım adım versiyonlarının kopyalarını alarak daha sonra ihtiyaç duyduğumuzda aldığımız kopyalara yani versiyonlara kolayca dönebiliyoruz.Farklılıklar değil anlık pozlar.Git’in diğer herhangi bir VCS’den (Subversion ve benzerleri dahil olmak üzere) en büyük farkı, Git’in veriler hakkında düşünme şeklidir. Diğer çoğu sistem bilgileri dosya-bazlı değişim listesi şeklinde saklar. Bu diğer sistemler (CVS, Subversion, Perforce, Bazaar vd.) bilgileri dosya setleri ve o dosyalara zaman içinde yapılan değişiklikler şeklinde saklar. Peki neden Git kullanmalıyız şöyleki diyelim week1 diye bir projemiz var ve bu proje üstünde yenilikler veya değişiklikler yapmak istiyoruz o zaman direkt bu proje üstünden değil de week1-copy üzerind yani orijinal projenin kopyası üzerinde değişiklik yaptığımızı söyleyebiliriz böyle yaptığımız zaman bir hata ile karşılaştığımızda ilk sürüm olan orijinal projemize (week1) dönüş yapabiliriz. Böylece projemizi risklere karşı korumuş oluruz. Bu işlemleri tekrar tekrar uygulayarak proje geliştirme sürecimizi bu şekilde tamamlarız.

Git Commands
•Git Init (initializing repositories): Git init komutu bilgisayarda oluşturmuş olduğumuz bir klasörün Git'e tanımlanması için kullanılır. Kullanımı: git init [repository name]
•Git Add (adding changes to staging): Projemizi ya da belirlediğimiz bir dosyayı çalışma dizinine eklemek amacıyla kullanılır. Kullanımı: git add [file]  = bir tane ekleme  
git add .  = toplu ekleme işlemi
•Git Commit:

