[EN]
# Lasso Regression - L1 Regression

## Purpose
Lasso regression aims to find the coefficients that minimize the sum of squared errors. In this process, a penalty is applied to the coefficients to control the complexity of the model.

## Difference from Ridge Regression
- With sufficiently large λ (lambda) values, Lasso can bring some coefficients close to zero and even make them exactly zero.
- Ridge regression has the disadvantage of leaving all relevant and irrelevant variables in the model; thus, Lasso addresses this issue by performing variable selection.
- In Lasso, when the L1 norm (λ) is sufficiently large, some coefficients become zero. This is an advantage over L2 norm (Ridge), which only brings coefficients close to zero.
- The cross-validation method is used to improve the model's performance.

## λ (Lambda) and MSE
- The case where λ is zero corresponds to the Mean Squared Error (MSE). Our goal is to find the λ value that minimizes the MSE.
- A set of specific values for λ is selected, and the cross-validation test error is calculated for each.
- The λ value that gives the lowest cross-validation error is chosen as the tuning parameter.
- The model is then refitted with the selected λ value.

## R² Score
The R² score indicates how well the independent variable explains the dependent variable. Important points regarding the R² score:

- **R² = 0.0**: The model explains none of the variability in the data.
- **R² = 1.0**: The model explains all the variability in the data.
- **R² ≈ 0.7 and above**: The model explains a large portion of the variability in the data and generally shows good performance.
- **R² ≈ 0.5 - 0.7**: Medium performance; the model explains about half of the data.
- **R² < 0.5**: The model explains less than half of the variability in the data. This generally indicates that the model needs improvement.


[TR]

# Lasso Regresyonu - L1 Regresyon

## Amaç
Lasso regresyonu, hata kareler toplamını minimize eden katsayıları bulmayı hedefler. Bu süreçte, katsayılara bir ceza uygulayarak modelin karmaşıklığını kontrol ederiz.

## Ridge Regresyondan Farkı
- Yeterince büyük λ (lambda) değerleri ile Lasso, bazı katsayıları sıfıra yaklaştırabilir ve hatta sıfır yapabilir.
- Ridge regresyonu, ilgili ve ilgisiz tüm değişkenleri modelde bırakma dezavantajına sahiptir; bu nedenle Lasso, değişken seçimi yaparak bu durumu düzeltir.
- Lasso’da, L1 normu (λ) yeterince büyük olduğunda bazı katsayılar sıfır olur. Bu, L2 normunun (Ridge) katsayıları sıfıra yaklaştırdığı duruma göre bir avantajdır.
- Cross-validation yöntemi, modelin performansını artırmak için kullanılır.

## λ (Lambda) ve MSE
- λ'nın sıfır olduğu durum, Ortalama Kare Hata (MSE) değeridir. Amacımız MSE'yi minimize eden λ değerini bulmaktır.
- λ için belirli değerler içeren bir küme seçilir ve her biri için cross-validation test hatası hesaplanır.
- En düşük cross-validation hatasını veren λ değeri, ayar parametresi olarak seçilir.
- Seçilen λ değeri ile model yeniden fit edilir.

## R² Skoru
R² skoru, modelin bağımsız değişkenin bağımlı değişkeni ne kadar iyi açıkladığını ifade eder. R² skoru ile ilgili önemli noktalar:

- **R² = 0.0**: Model, verideki değişkenliği hiç açıklamıyor.
- **R² = 1.0**: Model, verideki değişkenliğin tamamını açıklıyor.
- **R² ≈ 0.7 ve üzeri**: Model verideki değişkenliğin büyük kısmını açıklıyor ve genellikle iyi bir performans gösteriyor.
- **R² ≈ 0.5 - 0.7**: Orta düzeyde bir performans; model verinin yaklaşık yarısını açıklıyor.
- **R² < 0.5**: Model, verideki değişkenliğin yarısından azını açıklıyor. Bu durum genellikle modelin geliştirilmeye ihtiyaç duyduğunu gösterir.
