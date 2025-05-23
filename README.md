# Deep-Learning-Based-Reconstruction-of-the-Geometric-Structure-of-Architectural-Space
Master's thesis, HSE

## Структура

| Этап | Назначение | Технологии |
|------|------------|------------|
| **0 Urban Generation** | Генерация планарной геометрии городской застройки | `Rhinoceros`, `Grasshopper` |
| **1 Scene Generation** | Обработка геометрии, генерация точек обзора и создание карт глубины и масок объектов | `VTK`, Python |
| **2 Image Generation** | Создание фотореалистичных синтетических изображений на основе SDXL и ControlNet | `Stable Diffusion XL`, `ControlNet`, `Depth Anything` |
| **3 Segmentation** | Сегментация зданий и их фасадов на изображениях | `YOLOv11-Seg` |
| **4 Planarization** | Создание планарных представлений зданий из карт глубины, калибровка камеры | `PCA`, `DBSCAN`, `Powell` |
| **5.1 Floors Regression** | Регрессия количества этажей зданий | `ResNet-152` |
| **5.2 Control Points Detection** | Детекция контрольных точек зданий на изображениях | `CNN`, `Transformer` |
| **6.1 Simple Matcher** | Алгоритм простого сопоставления планарных моделей зданий с разных видов | Python |
| **6.2 Record Planar Data** | Подготовка данных для обучения модели глубокого сопоставления | Python |
| **6.3 Deep Matcher** | Глубокая модель (иерархический Transformer) для сопоставления планарных моделей зданий с разных видов | `Transformer` |
