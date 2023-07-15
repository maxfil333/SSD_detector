Для запуска на кастомном датасете:

1) в файле utils.py добавить классы в label_map
2) в файле create_data_lists.py указать папку с датасетом структуры:
BCCD/ # имя папки
-----Annotations/
-----ImageSets/
----------Main/
-----JPEGImages/
Пример: 
create_data_lists(path='BCCD', output_folder='./')
3) Запустить create_data_lists.py для создания json файлов.

Общий порядок действий
для запуска на BCCD датасесете:

libraries:
https://pytorch.org/get-started/locally/ - для установки pytorch с cuda

1) скачать и поместить в корневой каталог папку BCCD
https://github.com/Shenggan/BCCD_Dataset

2) запустить create_data_lists (если отсутствуют json файлы)
3) запустить train.py для создания и обучения модели SSD
4) запустить detect.py, который сохранит полученное выбранное изображение 
с детекцией в директорию detected_images
