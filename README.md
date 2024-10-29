*Versiyon Kontrol Sistemi Nedir? 
Bir dosya ya da kümedeki değişiklikleri takip edebilmek için bir yöntemdir. Herhangi bir anda üzerinde çalıştığımız dosyaların o anki hallerini kaydedip istediğimiz zaman o ana geri dönme imkanı verir. Git dediğimiz olayda bu yapılan değişikliklerin içeriğini biim için takip edip kaydeder.

*Git Nedir ve Neden Kullanmalıyız?
Git, yazılım geliştirme süreçlerinde kullanılan bir versiyon kontrol sistemidir. Git sayesinde yapacağımız projelerin adım adım versiyonlarının kopyalarını alarak daha sonra ihtiyaç duyduğumuzda aldığımız kopyalara yani versiyonlara kolayca dönebiliyoruz.Farklılıklar değil anlık pozlar.Git’in diğer herhangi bir VCS’den (Subversion ve benzerleri dahil olmak üzere) en büyük farkı, Git’in veriler hakkında düşünme şeklidir. Diğer çoğu sistem bilgileri dosya-bazlı değişim listesi şeklinde saklar. Bu diğer sistemler (CVS, Subversion, Perforce, Bazaar vd.) bilgileri dosya setleri ve o dosyalara zaman içinde yapılan değişiklikler şeklinde saklar. Peki neden Git kullanmalıyız şöyleki diyelim week1 diye bir projemiz var ve bu proje üstünde yenilikler veya değişiklikler yapmak istiyoruz o zaman direkt bu proje üstünden değil de week1-copy üzerind yani orijinal projenin kopyası üzerinde değişiklik yaptığımızı söyleyebiliriz böyle yaptığımız zaman bir hata ile karşılaştığımızda ilk sürüm olan orijinal projemize (week1) dönüş yapabiliriz. Böylece projemizi risklere karşı korumuş oluruz. Bu işlemleri tekrar tekrar uygulayarak proje geliştirme sürecimizi bu şekilde tamamlarız.

*Git Commands
•Dit Brunch: Bu komut sayesinde projemizi dallara ayırabiliriz. Diyelim ki; yayında olan bir projemiz var ve bu projede yenilikler yapmamız gerekiyor. Yayına çıkan kısımda hiç değişiklik yapmadan ekleyeceğimiz sürüm çalışıyor mu denemek istedik. İşte bu tarz durumlarda “branch” komutu devreye girecektir. Böylece yayında olan bir projeyi riske atmadan yeniliklerin çalışıp çalışmadığını görüntüleyebiliriz.
Kullanımı: git brunch git brunch [brunch bame]  = teni bir dal oluşturur
git brunch -d [brunch name]   = oluşturulan özellik dalını siler
•Git Init (initializing repositories): Git init komutu bilgisayarda oluşturmuş olduğumuz bir klasörün Git'e tanımlanması için kullanılır. Kullanımı: git init [repository name]
•Git Add (adding changes to staging): Projemizi ya da belirlediğimiz bir dosyayı çalışma dizinine eklemek amacıyla kullanılır. Kullanımı: git add [file]  = bir tane ekleme  
git add .  = toplu ekleme işlemi
•Git Commit (commiting changes): Commit ‘in kelime anlamı işaretlemedir. Git‘e eklediğimiz dosyaları kalıcı olarak veri tabanında işaretlemenizi sağlar. Bu komut ile hazırlama alanına aldığımız değişiklikleri yerel depoya yüklemek için kullanılır. Değişiklikleri yüklerken commit’e mesaj eklemek yararımıza olacaktır. Bu sayede üzerinden belli bir zaman geçse bile yaptığımız değişiklikleri anlamamıza ve işlemlerinizi hızlandırmamıza yardımcı olur. 
Kullanımı: git commit -m "[type in the commit message]"
•Git Reset: Buradaki reset işlemi ile bilgilerimiz silinmeden ve yeni bir commit üretmeden değişiklikleri geri alabiliriz. Dosya aşamasını kaldırır fakat aynı zamanda içeriğini korur.
Kullanımı: git reset [file] git reset [commit]  =belirtilen committen sonrakileri geri alır ve değişiklikleri yerel olarak korur. 
git reset -hard [commit]  =local tüm commitleri silerek geri alma işlemi yapar bu yüzden dikkatli kullanmak gerekir.
•Git Merge: Üzerinde çalışmış olduğumuz iki parçayı birleştirir 
Kullanımı: git merge [branch name]
 •.gitignore: Gitignore dosyası sayesinde biz istemediğimiz dosyaları iptal edebiliyoruz. 
 Örneğin gitignore javascript dedik ve;
 # compiled output
/dist
/tmp
/out-tsc       bu tarz dosyaları tutmayabiliriz     

*Forking Repository Nedir?
Fork, bir Github deposunun tam bir kopyasını oluşturur. Bu kopya, orijinal depo ile aynı kod tabanına sahip olur ancak bağımsız bir şekilde değişiklikler yapmamıza olanak tanır.Forking, genellikle açık kaynak projelerinde kullanılır. Kullanıcılar, projeyi kendi ihtiyaçlarına göre değiştirmek, geliştirmek veya yeni özellikler eklemek için bu kopyayı oluştururlar. Böylece orijinal projeyi etkilemeden denemeler yapabilirler.
Forking Süreci
Fork Etme:
GitHub’da ilgilendiğiniz projeye gidin.
Sağ üst köşede bulunan "Fork" butonuna tıklayın. Bu, projeyi kendi hesabınıza kopyalar.
Kendi Kopyanız Üzerinde Çalışma:
Fork edilen depoyu bilgisayarınıza klonlayabilirsiniz. Bu sayede yerel bir kopya üzerinde çalışabilirsiniz.
Gerekli değişiklikleri yapın, yeni özellikler ekleyin veya hataları düzeltin.
Değişiklikleri GitHub’a Gönderme:
Değişikliklerinizi yerel repoda yaptıktan sonra, bunları GitHub’daki forkunuza "commit" ve "push" ederek yükleyebilirsiniz.
Pull Request Oluşturma:
Eğer yaptığınız değişikliklerin orijinal projeye dahil edilmesini istiyorsanız, orijinal depoya bir "Pull Request" (PR) gönderirsiniz.
PR, projenin sahibi veya diğer katkı yapan kişiler tarafından incelenir. Değişikliklerin kabul edilip edilmeyeceğine karar verilir. Bir örnek vermek gerekirse: Diyelim ki bir JavaScript kütüphanesi geliştiren bir projeye katkıda bulunmak istiyorsunuz. Projeyi fork edersiniz, yerel bilgisayarınıza klonlarsınız ve yeni bir özellik ekleyip test edersiniz. Sonra bu değişiklikleri GitHub’a gönderir ve orijinal projeye PR oluşturursunuz. Proje yöneticisi değişikliklerinizi inceler ve uygun görürse, bunları orijinal projeye ekler.

*Cloning Repository Nedir?
Cloning repository (depo klonlama), bir GitHub deposunun tam bir kopyasını yerel bilgisayarımıza indirme işlemidir. Bu işlem, geliştiricilerin projeler üzerinde çalışabilmesi ve değişiklikler yapabilmesi için önemlidir.Klonlama, geliştiricilerin projeleri yerel ortamlarında çalışarak, geliştirme yapabilmelerini sağlar. Bu, değişikliklerin daha hızlı ve verimli bir şekilde yapılmasına yardımcı olur.
Klonlama:
Github'da klonlamak istediğiniz depoyu seçin.Depo sayfasına gidin.
Sağ üst köşede "Code" butonuna tıklayın.HTTPS veya SSH bağlantısını kopyalayın.
Bilgisayarınızda terminal (Linux/macOS) veya komut istemcisini (Windows) açın.
Klonlama Komutu:
Aşağıdaki komutu kullanarak depoyu yerel bilgisayarınıza klonlayın:
git clone [Klonlama Bağlantısı]
Örneğin:  git clone https://github.com/kullaniciadi/projeadi.git
Klonlanan Depo Üzerinde Çalışma:
Klonlama işlemi tamamlandıktan sonra, klonladığınız proje dizinine gidin:
cd projeadi
Burada, projeyi inceleyebilir, düzenlemeler yapabilir ve geliştirmeler gerçekleştirebiliriz.
Bir örnek verelim;diyelim ki bir Python projesi geliştiren bir açık kaynak projesine katkıda bulunmak istiyorsunuz. Öncelikle projeyi Github üzerinden klonlarsınız. Yerel bilgisayarınıza indirdikten sonra, projeyi çalıştırır, yeni bir özellik ekler veya hataları düzeltirsiniz. Daha sonra değişikliklerinizi yerel repoda kaydeder ve isterseniz orijinal projeye geri göndermek için bir pull request oluşturabilirsiniz.

*Pull Request Nedir?
Pull request, bir kullanıcının yaptığı değişikliklerin orijinal projeye entegre edilmesi için gönderdiği bir talep veya öneridir. Kullanıcı, kendi fork’ladığı veya üzerinde çalıştığı bir depodaki değişiklikleri, orijinal depoya eklenmesi için teklif eder.
GitHub Üzerinde Pull Request Oluşturma:
GitHub’a gidin ve fork ettiğiniz veya çalıştığınız projeye gidin.
Sayfanın üst kısmında “Compare & pull request” veya “New pull request” butonuna tıklayın.
Hangi branch’inizi karşılaştırmak istediğinizi seçin. Genellikle bu, değişikliklerinizi içeren branch ile orijinal depodaki ana branch (genellikle main veya master) arasında bir karşılaştırmadır.Açılan sayfada, pull? request’iniz için bir başlık ve açıklama girin. Açıklama kısmında, yaptığınız değişikliklerin neden önemli olduğunu, hangi sorunları çözdüğünü veya hangi yeni özellikleri eklediğinizi belirtin.
Gerekirse etiketler (labels) ekleyebilir ve ilgili kişileri (assignees) atayabilirsiniz.Tüm bilgileri doldurduktan sonra “Create pull request” butonuna tıklayarak pull request’inizi gönderin.

*Pushing Changes Nedir?
GitHub’da pushing changes ifadesi, yerel (local) depodaki değişikliklerin GitHub gibi uzak (remote) bir depoya gönderilmesi anlamına gelir. Bu işlem, projede yapılan güncellemeleri herkesin erişebileceği şekilde depolamak ve başkalarıyla paylaşmak için kullanılır.
Push işlemi:
Değişiklik Yapma: Projende kod ya da dosya değişiklikleri yaparsın.
Staging: Yaptığın değişiklikleri bir sonraki adıma hazırlamak için "git add" komutuyla staging alanına eklemen gerekir.
Commit: Yaptığın değişiklikleri bir mesajla (commit message) kaydedersin. Bu işlem, değişiklikleri yerel depoda kalıcı hale getirir.
Push: Son olarak, "git push" komutunu kullanarak, bu commit’leri uzak depoya gönderirsin.

*Pulling Changes Nedir?
GitHub’da pulling changes ifadesi, uzak bir depoda (örneğin, GitHub’da) yapılmış olan değişiklikleri yerel (local) depoya almak anlamına gelir. Böylece, projeyi güncel tutmak ve başkalarının yaptığı değişikliklere erişmek mümkün olur.
Pull nasıl yapılır: git pull origin branch_adı
origin: Uzak deponun adı (genellikle origin olarak adlandırılır).
branch_adı: Çalıştığın dalın (branch) adı, genellikle main veya master olur.















