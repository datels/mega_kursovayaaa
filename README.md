Практическая часть курсовой работы по распознаванию эмоций по изображениям лиц.

## Что сделано

- Использован бенчмарк-набор данных FER-2013.
- Использована легковесная архитектура MobileNetV2 из библиотеки `torchvision`.
- Проведены три эксперимента:
  1. MobileNetV2, learning rate = 0.001;
  2. MobileNetV2, learning rate = 0.0001;
  3. MobileNetV2, learning rate = 0.001, weight decay = 1e-4.
- Качество оценено по accuracy и macro F1-score.
- Построены кривые обучения и confusion matrix.

## Лучшие результаты

| Эксперимент | Модель | Learning rate | Weight decay | Best test accuracy | Best test macro F1 |
|---|---|---:|---:|---:|---:|
| 1 | MobileNetV2 | 0.001 | 0 | 0.6567 | 0.6302 |
| 2 | MobileNetV2 | 0.0001 | 0 | 0.6215 | 0.5892 |
| 3 | MobileNetV2 | 0.001 | 1e-4 | 0.6527 | 0.6338 |

## Запуск

Файл .ipynb рассчитан на Google Colab с GPU T4.

Как запустить:
1. Открыть файл в формате `*.ipynb` из репозитория в Google Colab.
2. Выбрать GPU: `Runtime -> Change runtime type -> T4 GPU`.
3. Загрузить `kaggle.json` через ячейку загрузки.
4. Последовательно выполнить ячейки ноутбука.

