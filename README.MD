## Использование DevTools для анализа загрузки сайта

telegram для связи @geek_py

### Network
**1. На вкладке Network**
* [Записать и сохранить в HAR архив профиль загрузки ресурсов при открытии страницы](./Network/www.gd.ru.har)
### Найти неоптимальные места
1) Дублирование ресурсов
   <img src="./images/Screenshot_71.png" width=90%>
   <img src="./images/Screenshot_73.png" width=90%>
   <img src="./images/Screenshot_75.png" width=90%>
   <img src="./images/Screenshot_76.png" width=90%>
   <img src="./images/Screenshot_77.png" width=90%>
   <img src="./images/Screenshot_80.png" width=90%>
   <img src="./images/Screenshot_82.png" width=90%>
   <img src="./images/Screenshot_85.png" width=90%>

2) Лишний размер ресурса. Были выбраны файлы с лишними комментариями/большими отступами
   <img src="./images/Screenshot_68.png" width=90%>
   <img src="./images/Screenshot_69.png" width=90%>
   <img src="./images/Screenshot_70.png" width=90%>
   <img src="./images/Screenshot_72.png" width=90%>
   <img src="./images/Screenshot_74.png" width=90%>
   <img src="./images/Screenshot_78.png" width=90%>
   <img src="./images/Screenshot_79.png" width=90%>
   <img src="./images/Screenshot_81.png" width=90%>
   <img src="./images/Screenshot_83.png" width=90%>
   <img src="./images/Screenshot_84.png" width=90%>

3) Медленно загружающиеся ресурсы
   <img src="./images/Screenshot_66.png" width=90%>

4) Ресурсы, блокирующие загрузку
   <img src="./images/Screenshot_65.png" width=90%>

5) Что-то ещё (ресурсы которые упали с ошибкой)
   <img src="./images/Screenshot_67.png" width=90%>

1) [Записать и сохранить в файл профиль загрузки страницы](./Perfomance/Trace-20230618T015119.json)
2) Измерить время в миллисекундах от начала навигации до событий First Paint (FP), First Contentful Paint (FCP), Largest Contentful Paint (LCP), DOM Content Loaded (DCL), Load
   <img src="./images/Screenshot_87.png" width=90%>
   <img src="./images/Screenshot_88.png" width=90%>
   <img src="./images/Screenshot_89.png" width=90%>
   <img src="./images/Screenshot_90.png" width=90%>
   <img src="./images/Screenshot_92.png" width=90%>

3) Определить, на каком DOM-элементе происходит LCP
   <img src="./images/Screenshot_91.png" width=90%>

4) Измерить, сколько времени в миллисекундах тратится на разные этапы обработки документа (Loading, Scripting, Rendering, Painting)
   <img src="./images/Screenshot_86.png" width=90%>

### На вкладке Coverage
1) Cохранить скриншот вкладки после загрузки страницы
   <img src="./images/Screenshot_93.png" width=90%>

2) Измерить в килобайтах объём неиспользованного CSS в ходе загрузки страницы
   <img src="./images/Screenshot_94.png" width=90%>

3) Измерить в килобайтах объём неиспользованного JS в ходе загрузки страницы
   <img src="./images/Screenshot_95.png" width=90%>


## Дополнительное задание
**Использовать сеть Slow 3G и CPU 4x slowdown**
### Найти неоптимальные места
Slow полностью совпадает с анализом неоптимальных мест выше по тексту
1) [Записать и сохранить в HAR архив профиль загрузки ресурсов при открытии страницы](./SlowNetwork/www.gd.ru.har)
### На вкладке Performance
1) [Записать и сохранить в файл профиль загрузки страницы](./SlowNetwork/Trace-20230618T020748.json)
2) Измерить время в миллисекундах от начала навигации до событий First Paint (FP), First Contentful Paint (FCP), Largest Contentful Paint (LCP), DOM Content Loaded (DCL), Load
   <img src="./images/Screenshot_101.png" width=90%>
   <img src="./images/Screenshot_99.png" width=90%>
   <img src="./images/Screenshot_98.png" width=90%>
   <img src="./images/Screenshot_97.png" width=90%>
   <img src="./images/Screenshot_100.png" width=90%>
3) Определить, на каком DOM-элементе происходит LCP
   <img src="./images/Screenshot_105.png" width=90%>
4) Измерить, сколько времени в миллисекундах тратится на разные этапы обработки документа (Loading, Scripting, Rendering, Painting)
   <img src="./images/Screenshot_102.png" width=90%>

### На вкладке Coverage
1) Cохранить скриншот вкладки после загрузки страницы
   <img src="./images/Screenshot_96.png" width=90%>
2) Измерить в килобайтах объём неиспользованного CSS в ходе загрузки страницы
   <img src="./images/Screenshot_104.png" width=90%>
3) Измерить в килобайтах объём неиспользованного JS в ходе загрузки страницы
   <img src="./images/Screenshot_103.png" width=90%>