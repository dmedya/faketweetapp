React JS Kurulumu
Online olarak katılmayı deneyin ya da local geliştirme ortamınızı oluşturun.

Online Kod Ortamı
React’i online kod ortamında denemek istiyorsanız, CodePen ya da CodeSandbox sitelerini kullanabilirsiniz.

React HTML Şablonu
Kendi text editörünüzü kullanmayı tercih ederseniz, bu HTML dosyasını indirebilir, düzenleyebilir ve tarayıcınızdaki local dosya sisteminden açabilirsiniz. Kod dönüştürmesini yavaş yapar, bu nedenle sadece öğrenme aşamasında kullanın, projeleriniz için kullanmayın.

Hızlı Başlangıç
React kavramlarına adım adım bir giriş için hızlı başlangıç bölümüne gidin.

Bir örnek üzerinden eğitim için uygulamalı eğitim bölümünü deneyin.

Geliştirme Ortamı
Yukarıdaki hafif çözümler, React’a yeni başladıysanız ya da denemek için en uygun yöntemlerdir.

React JS’i bilgisayarınıza kurup, localinizde proje geliştirmeye başlamak istiyorsanız aşağıdaki adımları inceleyin.

Not:

Olası uyumsuzluk sorunlarını önlemek için tüm React paketleri aynı sürümü kullanmalıdır. (react, react-dom vs.)

NodeJS Kurulumu
NodeJS sitesine girip aşağıda görüldüğü gibi soldaki butona tıklayıp nodejs’i indiriyoruz.



Ardından klasik kurulumu tamamladıktan sonra Node.js command prompt programını çalıştırıp, kurulumlarımızı bu konsol üzerinden yapacağız.

Yeni bir React projesine başlamak için en kolay yol, bir başlangıç kiti kullanmaktır.

React ekibi tarafından önerilen çeşitli başlangıç kitleri bulunmakta; Create React App, Next.js, Gatsby, nwb, razzle, Neutrino. React projesi başlatmak için resmi olarak desteklenen Create React App’ı detaylı açıklayalım.

Create React App
Create React App, yeni bir React single page application’a başlamanın en iyi yoludur. Geliştirme ortamınızı, en yeni JavaScript özelliklerini kullanabilmenizi, güzel bir geliştirici deneyimi yaşamanızı ve uygulamanızı üretim için optimize etmenizi sağlar. NodeJS 6 veya daha üst sürümünün bilgisayarınızda kurulu olması gerekir (Sunucuda gerekli değildir).

Create React App’i özetlemek gerekirse bu, React uygulamaları oluşturmanız için ihtiyacınız olan birçok şeyi içerisinde barındıran bir pakettir.

İçerisine neler dahil edilmiştir?

React, JSX, ES6, Flow syntax desteği
Autoprefixed CSS ile otomatik olarak düzeltilen CSS’ler (-webkit veya diğer ön eklere gerek yoktur)
Genel hatalar konusunda uyaran bir canlı geliştirme sunucusu
Kod üzerinde yaptığımız değişiklikleri kaydettiğimiz anda arayüze yansıması için hot reloading
JavaScript kod standartlarına uygun yazmanız için ESLint vs
İlk olarak nodejs kurup, ardından aşağıdaki adımları gerçekleştirerek ilk uygulamamızı oluşturmaya başlayalım.

npm install -g create-react-app


Ardından my-app adında bir proje oluşturuyoruz.

create-react-app my-app
Kurulum başarılı olduğunda aşağıdaki gibi bir çıktı ile kaşılacaksınız.



Eğer npm 5.2.0+ sürümü yüklüyse, bunun yerine npx kullanabilirsiniz.

npx create-react-app my-app
Bu komutlar geçerli klasörde my-app isimli bir dizin oluşturacaktır. Bu dizinin içinde, proje yapısını oluşturacak ve geçişli bağımlılıkları kuracaktır.

Projenin klasör yapısı aşağıdaki gibi olacaktır. Yapılandırma veya karmaşık klasör yapıları yok, sadece uygulamanızı oluştururken gereken dosyaları içerir.

my-app                             
├── README.md
├── package-lock.json
├── package.json
├── .gitignore
├── public
│   └── favicon.ico
│   └── index.html
│   └── manifest.json
│   └──logo192.png
│   └──logo152.png
└── src
    └── App.css
    └── App.js
    └── App.test.js
    └── icons.js
    └── index.css
    └── index.js
    └── logo.svg
    └──...
    


Kurulum tamamlandıktan sonra aşağıdaki komutlar ile proje klasörünüze girebilirsiniz. Ardından npm start ya da yarn start komutu ile projenizi localde açabilirsiniz.

cd my-app
npm start
Otomatik olarak localhost sayfası açılacaktır. Kodda değişiklik yaparsanız, sayfa otomatik olarak yeniden yüklenir. Konsolda ise hata uyarılarını görürsünüz. Kod yazmaya başlamak için src/App.js dosyasını düzenleyin ve kaydedin.

Projeyi Build Etmek
Kodunuzu yazdınız ve sunucunuza yüklemek istiyorsunuz, o halde npm run build komutu ile üretim için gerekli klasörler hazırlanır. React’ı düzgün bir şekilde paketler ve yapıyı en iyi performans için optimize eder. CSS ve JavaScript kodlarını minified eder (sıkıştırır) ve rastgele isimlendirir.

npm run build
Oluşturulan build klasörünün içerisindeki dosyaları sunucunuza atarak test edebilirsiniz.

