# Yapay Öğrenmeyi Doğal Öğrenme Denemeleri

[Türkiye'deki yerleşim yerlerinin isimlerini](isimler.txt) kullanarak bir _harf seviyesi_ dil modeli oluşturacağız. Bu modeli kullanarak (bunlara benzer ama tamamen) yeni isimler üreteceğiz.

## Rehber - Yöntem - Edevat

Andrej Karpathy'nin [makemore](https://github.com/karpathy/makemore) projesinden feci şekilde intihal yaparak (ve yetinmeyip [burada](https://www.youtube.com/playlist?list=PLAqhIrjkxbuWI23v9cThsA9GvCAUhRvKZ) anlattıklarından da _istifade_ ederek) konuyu öğrenirken belgelemeye ve uygulamaya çalışacağım.

Temel mecramız [Jupyter Notebook](https://jupyter.org/) ve [Markdown](https://daringfireball.net/projects/markdown/) olacak. [Python](https://www.python.org/) dışında sadece [PyTorch](https://pytorch.org/) kütüphanesini kullanıyoruz.

## İçerik

1. [Hazırlık](./01_hazirlik.md): Kaynaktan aldığımız veriyi kullanacağımız şekle evirip ön temizlik yapacağız. [Soransında](./01a_inceleme.ipynb), bu veri setini istatistiksel olarak keşfetmeye çalışacağız, başka sorunlar bulursak onları da giderip veriyi [nihai](isimler.txt) hale getireceğiz.
1. [Bigram](./02_bigram.ipynb): Harflerin birbirini takip etme olasılığını kullanacağız. Ve [kaliteye](./02a_kalite.ipynb) bakacağız.
1. [Basit Bir Neural Network](./03_basitNN.ipynb): olabilecek en basit NN ile aynı işi yapmaya çalışacağız ama önce [nöron nedir](./03_0_neron.ipynb) bakmak gerek.
1. [MLP](./04_mlp.ipynb): Çok katmanlı mimariye tek katmandan gireceğiz: bunun da bir sebebi var: [disiplin](./04a_disiplin.ipynb).
1. Transformer: [Bu](https://arxiv.org/abs/1706.03762) makaledeki modeli _mütevazice_ kullanacağız. TODO
1. Sonuçlar: TODO

## Kodu Çalıştırmak İstersen

- Halihazırda PyTorch ve Jupyter (yüklü ya da) yükleyebileceğin bir ortam varsa tek yapman gereken klonlamak/kopyalamak.
- Yoksa; sadece [Docker](https://www.docker.com/) ve [VS Code](https://code.visualstudio.com/) yükleyebildiğin bir cihaz yeterli. Bu repo'yu klonladıktan sonra [devcontainer](https://code.visualstudio.com/docs/remote/containers) olarak çalıştırabilirsin (imaj 2.5 GB boyutlarında: ilk seferde biraz bekletebilir; bilenler [buradan](./.devcontainer/Dockerfile) ince ayar yapabilir).
- Github hesabın varsa [codespaces](https://github.com/codespaces) üzerinde de çalıştırabilirsin.

## Metodolojik Natüralizm ve Sorumluluğun (ikisinin de 🫢) Reddi

Konu gayet akademik, nerede metodolojik natüralizm, neden bu sarkastik futbol yorumcusunun voleybol maçı anlatım üslubu derseniz: demeyin! Şimdilik böyle olsun, temize çekerken bir GPT vasıtasıyla yavanlaştırırız.

Buradaki bilgilerle kendinizi zarara uğratabilecek bir girişimde bulunmak gibi bir niyetiniz varsa benim bu zarara ortak olmak gibi bir [niyetim yok](LICENSE) ¯\\\_(ツ)\_/¯.
