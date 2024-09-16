# ElasticNet Regression

## [EN]

ElasticNet Regression combines Lasso (L1 regularization) and Ridge (L2 regularization) techniques. The goal is to find coefficients that minimize the sum of squared errors while applying a penalty to these coefficients. It provides a more effective smoothing process, performing variable selection like Lasso and penalization like Ridge.

The parameter controlling the effect of these two techniques on the functional structure is `l1_ratio`, which by default is set to 0.5. The `l1_ratio` determines how much contribution each regularization method makes to the model. For example, `l1_ratio=0.7` gives 70% weight to Lasso and 30% to Ridge. The `alpha` parameter controls the strength of both regularizations.

- `l1_ratio = 0`: Only Ridge (L2 regularization) is applied, and the model behaves entirely like Ridge regression.
- `l1_ratio = 1`: Only Lasso (L1 regularization) is applied, and the model behaves entirely like Lasso regression.

---

## [TR]

ElasticNet Regresyonu, Lasso (L1 regülarizasyonu) ve Ridge (L2 regülarizasyonu) tekniklerini birleştirir. Amaç, hata kareler toplamını minimize eden katsayıları bu katsayılara bir ceza uygulayarak bulmaktır. Daha etkin bir düzgünleştirme işlemi sağlar, Lasso tarzı değişken seçimi yaparken Ridge tarzı cezalandırma uygular.

Bu iki tekniğin fonksiyonel yapı üzerindeki etkilerini kontrol eden parametre `l1_ratio` parametresidir ve varsayılan olarak 0.5'e ayarlıdır. `l1_ratio`, hangi regülarizasyon türünün modele daha fazla katkıda bulunacağını belirler. Örneğin, `l1_ratio=0.7`, Lasso'ya %70 ve Ridge'e %30 ağırlık verir. `alpha` parametresi ise her iki regülarizasyonun gücünü kontrol eder.

- `l1_ratio = 0`: Sadece Ridge (L2 regülarizasyonu) uygulanır ve model tamamen Ridge regresyonu gibi davranır.
- `l1_ratio = 1`: Sadece Lasso (L1 regülarizasyonu) uygulanır ve model tamamen Lasso regresyonu gibi davranır.
