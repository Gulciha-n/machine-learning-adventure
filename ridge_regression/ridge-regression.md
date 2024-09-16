# Ridge Regression - L2 Regularization

## [EN]

Ridge regression is a type of linear regression used to prevent overfitting. While linear regression fits a line to understand the relationship between the dependent and independent variables, it can be affected by noise in the data. Ridge regression simplifies the model to correct this issue.

Ridge regression prevents overfitting by penalizing the regression coefficients. In standard linear regression, the error function tries to minimize only the prediction errors, but ridge regression minimizes both the errors and the size of the coefficients by adding an L2 penalty term to the error function. Mathematically, this penalty term is added to the sum of squared errors.

The goal is to find coefficients that minimize the sum of squared errors while applying a penalty to those coefficients. Ridge regression is resistant to overfitting and provides a solution to multicollinearity. It builds a model with all variables but shrinks the coefficients of irrelevant variables toward zero. Choosing a good value for `alpha` (penalty) is important, and cross-validation is used to determine it.

- **λ**: Tuning parameter, which needs to be set and optimized by the user (hyperparameter). When λ = 0, it results in Ordinary Least Squares (OLS). We are looking for the λ that minimizes the Sum of Squared Errors (SSE).
  
A set of predefined λ values is chosen, and the cross-validation test error is calculated for each one. The λ with the smallest cross-validation error is selected as the tuning parameter. Different λ values will result in different coefficients, and the models built with these coefficients will be evaluated based on their errors. The goal is to find the coefficients where the RMSE value is minimized.

- **Residual (Error, ei)**: Residual is the difference between the observed values and the predicted values. It indicates how well the model can make predictions and can be considered the model's error. Residual is calculated as:
  
  `ei = y - ŷ`

- **pd.get_dummies - L2 Regularization**: Dummy variables are created through "dummy encoding" or "one-hot encoding," a technique used to convert categorical variables into numerical data. This method represents each category as a separate column, indicating the presence of a category with 1 or 0.
  - `pd.get_dummies()`: A function in the Pandas library.
  - **One-Hot Encoding**: The process performed by `pd.get_dummies()`.

### Model Tuning
The `RidgeCV` function is a model that automatically selects the optimal alpha value for ridge regression using cross-validation (CV). It is the cross-validation version of ridge regression.

Example:
```python
RidgeCV(lambdas=lambdas2, scoring="neg_mean_squared_error", cv=10)
```

## [TR]
# Ridge Regresyon - L2 Regülarizasyonu

Ridge regresyon, doğrusal regresyon modelinin bir türüdür ve aşırı öğrenmeyi (overfitting) önlemek için kullanılır. Doğrusal regresyon, bağımlı değişken ile bağımsız değişkenler arasındaki ilişkiyi anlamak için bir çizgi çizer, ancak verilerdeki gürültüden (noise) etkilenebilir. Ridge regresyon, modeli daha basit hale getirerek bu durumu düzeltir.

Ridge regresyon, regresyon katsayılarını cezalandırarak aşırı öğrenmeyi önler. Normal doğrusal regresyonda hata fonksiyonu sadece tahmin hatalarını minimize etmeye çalışırken, ridge regresyon bu hatalara ek olarak katsayıların büyüklüğünü de minimize eder. Matematiksel olarak, hata fonksiyonuna bir L2 ceza terimi ekler.

Amaç, hata kareler toplamını minimize eden katsayıları, bu katsayılara bir ceza uygulayarak bulmaktır. Ridge regresyon, overfitting’e karşı dirençlidir ve çok boyutluluğa çözüm sunar. Tüm değişkenlerle model kurar, ancak ilgisiz değişkenlerin katsayılarını sıfıra yaklaştırır. `alpha` (ceza) için iyi bir değer bulmak önemlidir ve bunun için çapraz doğrulama (cross-validation) yöntemi kullanılır.

- **λ**: Ayar parametresi olup, kullanıcı tarafından ayarlanması ve optimize edilmesi gerekir (hiperparametre). λ = 0 iken Ordinary Least Squares (OLS) elde ederiz. Hata kareler toplamını (Sum of Squared Errors - SSE) minimum yapan λ’yı arıyoruz.
  
Belirli λ değerleri içeren bir küme seçilir ve her biri için çapraz doğrulama test hatası hesaplanır. En küçük çapraz doğrulama hatasını veren λ, ayar parametresi olarak seçilir. Farklı λ değerleri ile farklı katsayılar oluşacak ve bu katsayılar ile kurulan modellerin hataları incelenecektir. Bu katsayılar, hata ortalamasının karekökü (RMSE) en küçük olduğunda optimum noktada durmalıdır.

- **Rezidü (Hata, ei)**: Rezidü, gözlem değerleri ile tahmin edilen değerler arasındaki farktır. Bu fark, modelin ne kadar iyi tahmin yapabildiğini gösterir. Rezidü şu şekilde hesaplanır:
  
  `ei = y - ŷ`

- **pd.get_dummies - L2 Regülarizasyonu**: Kategorik değişkenlerin sayısal verilere dönüştürülmesi için "dummy encoding" veya "one-hot encoding" tekniği kullanılır. Bu yöntem, her bir kategoriyi ayrı bir sütun olarak temsil eder ve o kategorinin varlığını 1 veya 0 ile belirtir.
  - `pd.get_dummies()`: Pandas kütüphanesindeki bir fonksiyondur.
  - **One-Hot Encoding**: `pd.get_dummies()` ile gerçekleştirilen işlemin adıdır.

### Model Ayarı
`RidgeCV` fonksiyonu, Ridge regresyonu için çapraz doğrulama (CV) ile birlikte en uygun `alpha` değerini otomatik olarak seçen bir modeldir. Bu, Ridge regresyonunun çapraz doğrulama versiyonudur.

Örnek:
```python
RidgeCV(lambdas=lambdas2, scoring="neg_mean_squared_error", cv=10)

