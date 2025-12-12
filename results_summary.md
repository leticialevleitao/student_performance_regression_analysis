## Results Summary

### Quantitative Performance

| Model | MAE ↓ | MSE ↓ | R² ↑ | MAPE ↓ | Training Time ↓ |
|------|------|------|------|------|----------------|
| **Linear Regression** | **4.32** | **29.55** | **0.894** | **0.068** | ~0.09s |
| Support Vector Regressor | 5.17 | 42.16 | 0.849 | 0.082 | ~0.40s |
| Decision Tree Regressor | 7.54 | 91.15 | 0.673 | 0.119 | ~0.07s |
| KNN Regressor | 11.53 | 210.25 | 0.250 | 0.194 | ~0.07s |

**Best overall model:** **Linear Regression**

## Key Insights

- Academic performance behaves largely as a **linear and additive function** of student habits and contextual factors.
- Incremental improvements (e.g., additional study hours or better diet quality) result in consistent gains in exam scores.
- Simpler models, when well-specified, can outperform more complex alternatives.
- Linear Regression achieved the **best balance between accuracy, stability, and computational efficiency**.


