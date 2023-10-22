# Yapay Öğrenmeyi Doğal Öğrenme Denemeleri

Andrej Karpathy'nin [makemore](https://github.com/karpathy/makemore) projesinden feci şekilde intihal yaparak (ve yetinmeyip [burada](https://www.youtube.com/playlist?list=PLAqhIrjkxbuWI23v9cThsA9GvCAUhRvKZ) anlattıklarından da _istifade_ ederek) konuyu öğrenmeye ve öğrenme sürecimi (yanlışlarımı ve yaşadığım sorunları da dahil ederek) belgelemeye çalışacağım.

## Ne Yapacağız Tam Olarak?

[Türkiye'deki yerleşim yerlerinin isimlerini](isimler.txt) kullanarak bir _harf seviyesi_ dil modeli oluşturacağız. Bu modeli kullanarak -eğer başarabilirsek- (bunlara benzer ama tamamen) yeni isimler üreteceğiz. Öncelikle _bigram_ ve basit bir _neural network_ ile başlayıp bu iki çözümü karşılaştıracağız; sonra da aynı işi _transformer_ kullanarak yapacağız. Temel mecramız [Jupyter Notebook](https://jupyter.org/) ve [Markdown](https://daringfireball.net/projects/markdown/) olacak.

## İçerik

1. [Hazırlık](./01/README.md): Kaynaktan aldığımız veriyi temizleyip kullanılabilir hale getireceğiz.
1. Veri İnceleme: Kullanacağımız veri setini istatistiksel olarak keşfetmeye çalışacağız.
1. Bigram Modeli: Harflerin birbirini takip etme olasılığını kullanacağız.
1. Basit Bir Neural Network: Tek katmanlı bir NN ile aynı işi yapacağız.
1. Karşılaştırma: Bigram ve NN modellerimizi karşılaştıracağız.
1. Transformer: [Bu](https://arxiv.org/abs/1706.03762) makaledeki modeli _mütevazice_ kullanacağız.
1. Sonuçlar: Yaptıklarımızı özetleyip değerlendireceğiz.

## Nasıl Kullanabilirsin?

Sadece [Docker](https://www.docker.com/) ve [VS Code](https://code.visualstudio.com/) yükleyebildiğin bir cihaz yeterli. Bu repo'yu klonladıktan sonra [devcontainer](https://code.visualstudio.com/docs/remote/containers) olarak çalıştırabilirsiniz (imaj 2.5 GB boyutlarında: ilk seferde biraz bekletebilir; bilenler [buradan](./.devcontainer/Dockerfile) ince ayar yapabilir).

## Metodolojik Natüralizm ve Sorumluluğun (ikisinin de 🫢) Reddi

Konu gayet akademik, nerede metodolojik natüralizm, neden bu sarkastik futbol yorumcusunun voleybol maçı anlatım üslubu derseniz: demeyin! Şimdilik böyle olsun, temize çekerken bir GPT vasıtasıyla yavanlaştırırız.

Buradaki bilgilerle kendinizi zarara uğratabilecek bir girişimde bulunmak gibi bir niyetiniz varsa benim bu zarara ortak olmak gibi bir [niyetim yok](LICENSE) ¯\\\_(ツ)\_/¯.
