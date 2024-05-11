# Введение в инженерную деятельность

## Практическое занятие №4
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1GmfK3PgY3ekoFYO_LrC9QwYfiszYk8F7?usp=sharing)

### Установка и настройка CUDA и PyTorch
Работает только для видеокарт NVIDIA. Для этой практической работы, хватит и 4 гб видеопамяти.

1. Устанавливаем свежие [драйвера](https://www.nvidia.com/download/index.aspx?lang=ru) на видеокарту.

2. Скачиваем и устанавливаем подходящую [версию CUDA](https://developer.nvidia.com/cuda-toolkit-archive). **<u>Главное не старше 12.1</u>**.

3. Проверяем, что установка CUDA прошла успешно. Возможно, придется перезагрузить компьютер, а затем запустить в командной строке
```
nvcc -V
```
если всё установилось корректно, то вы увидите установленную версию CUDA.

4. Устанавливаем версию PyTorch под установленную версию CUDA.
Например, под версию 12.1 будет команда:
```
pip install torch torchvision --index-url https://download.pytorch.org/whl/cu121
```
вместо cu121 можно подобрать нужную вам версию.

5. Проверяем, что PyTorch установился и видит CUDA, для этого в командной строке запускаем
```
python

import torch
torch.cuda.is_available()
```
если вывелось `True`, значит всё хорошо и можно работать.

### Список необходимых библиотек:
* torch
* facenet-pytorch
* Pillow
* ultralytics
* timm
* scikit-learn
* roboflow
