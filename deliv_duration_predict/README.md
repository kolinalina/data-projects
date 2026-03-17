# delivery duration predict

**tujuan**:
untuk memprediksi waktu predict dan waktu actual.

**assignment:**
build model untuk memprediksi estimasi waktu delivery , durasi total delivery dalam satuan detik, time didapatkan dari:
- start: konsumen submit order (created_at)
- end: ketika order delivered to konsumen (actual_delivery_time)

**model:**
fokus meggunakan 3 model yaitu linier regression, random forest, and gradient boosting
Linear Regression              | RMSE: 912.4s | MAE: 695.3s | R²: 0.2009
Random Forest                  | RMSE: 867.9s | MAE: 660.2s | R²: 0.2771
Gradient Boosting              | RMSE: 864.2s | MAE: 655.6s | R²: 0.2831

hasilnya R2 nya sangat low, ini dikarenakan bukan modelnya yang salah tetapi dataset asli nya yang menyebabkan hasilnya low. 

kenapa tidak menyalahkan hasil dari model? karena setelah  melakukan pengecheckan features menunjukan output seperti ini:

outstanding_ratio                  0.293193
subtotal                           0.229502
total_outstanding_orders           0.192144
hour                               0.177377
num_distinct_items                 0.165934
price_per_item                     0.152157
max_item_price                     0.141942
total_items                        0.122963
total_busy_dashers                 0.103261
total_onshift_dashers              0.083266
order_protocol                     0.074754
is_weekend                         0.072194
store_primary_category_pizza       0.058613
store_primary_category_mexican     0.053002
store_primary_category_japanese    0.050375
market_id                          0.045941
store_primary_category_fast        0.045127
store_primary_category_sandwich    0.039609
busy_ratio                         0.036732
items_diff                         0.033573
Name: duration, dtype: float64