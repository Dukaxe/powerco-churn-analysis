# PowerCo Customer Churn (BCG X case study)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/dukehoangwrk/powerco-churn-analysis/blob/main/powerco_churn_analysis.ipynb)

PowerCo (điện và gas cho doanh nghiệp SME) cho rằng khách rời đi vì giá và muốn giảm giá 20% cho khách có nguy cơ rời đi. Dự án kiểm tra giả thuyết này và đánh giá đề xuất giảm giá.

## Kết quả chính
- 9,7% khách rời đi trong 3 tháng. Rủi ro cao ở khách 1–2 năm (15,4%) và khách có biên lợi nhuận phí công suất cao (15,8%).
- **Giá điện gần như không liên quan đến churn**: tỷ lệ churn 8–12% ở mọi mức giá; bỏ toàn bộ 8 biến giá khỏi mô hình thì AUC không giảm (dù importance của chúng cao nhất).
- Random Forest: accuracy 90,9% nhưng mốc "đoán tất cả ở lại" đã là 90,3%; recall ở ngưỡng 0,5 chỉ 7%. AUC 0,71; top 10% rủi ro churn 29%.
- Giảm giá 20% lỗ ở mọi phương án rộng hơn top 5% rủi ro, kể cả khi giữ được 100% khách sắp rời đi.

## Nội dung
| File | Mô tả |
|---|---|
| `powerco_churn_analysis.ipynb` | Notebook: EDA, kiểm tra giả thuyết giá, feature engineering, mô hình, phân tích giảm giá |
| `report/PowerCo_Churn_Report.pdf` | Báo cáo 9 trang |
| `data/` | `client_data.csv`, `price_data.csv` (BCG X Virtual Experience, Forage) |
| `figures/` | Biểu đồ |

## Cách chạy
- Máy cá nhân: `pip install -r requirements.txt` rồi mở notebook.
- Google Colab: bấm badge, Runtime → Run all, chọn cả 2 file trong `data/` khi được hỏi.
