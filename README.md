# Titanic Survival Prediction

Bu proje, Kaggle'ın ünlü Titanic veri seti üzerinde makine öğrenmesi modelleri kullanarak yolcu hayatta kalma tahmini yapmayı amaçlamaktadır.

## Proje Yapısı

```
Titanic_Data/
├── Data/
│   └── Raw/
│       ├── train.csv      # Eğitim verisi
│       └── test.csv       # Test verisi
├── Src/
│   └── baseline.ipynb     # Temel analiz ve model notebook'u
└── Submissions/
    ├── submission_lr_baseline.csv  # Logistic Regression sonuçları
    └── submission_rf.csv           # Random Forest sonuçları
```

## Veri Seti

Titanic veri seti şu özellikleri içerir:
- **PassengerId**: Yolcu kimlik numarası
- **Survived**: Hayatta kalma durumu (0: Hayır, 1: Evet)
- **Pclass**: Bilet sınıfı (1, 2, 3)
- **Name**: Yolcu adı
- **Sex**: Cinsiyet
- **Age**: Yaş
- **SibSp**: Gemideki kardeş/eş sayısı
- **Parch**: Gemideki ebeveyn/çocuk sayısı
- **Ticket**: Bilet numarası
- **Fare**: Bilet ücreti
- **Cabin**: Kamara numarası
- **Embarked**: Binme limanı (C, Q, S)

## Kullanılan Modeller

1. **Logistic Regression**: Temel sınıflandırma modeli
2. **Random Forest**: Ensemble yöntemi ile gelişmiş tahmin

## Çalıştırma

1. Gerekli kütüphaneleri yükleyin:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

2. Jupyter notebook'u çalıştırın:
```bash
jupyter notebook Src/baseline.ipynb
```

## Sonuçlar

Model performansları `Submissions/` klasöründe CSV formatında saklanmıştır.

## Katkıda Bulunma

1. Bu repository'yi fork edin
2. Yeni bir branch oluşturun (`git checkout -b feature/AmazingFeature`)
3. Değişikliklerinizi commit edin (`git commit -m 'Add some AmazingFeature'`)
4. Branch'inizi push edin (`git push origin feature/AmazingFeature`)
5. Bir Pull Request oluşturun

## Lisans

Bu proje MIT lisansı altında lisanslanmıştır.
