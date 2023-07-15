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
