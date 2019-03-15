# pokemon_image_generation
Генерация покемонов с помощью DCGAN и датасета с kaggle

Для генерации нового изображения покемона выбрал GAN (DCGAN).
https://ru.wikipedia.org/wiki/%D0%93%D0%B5%D0%BD%D0%B5%D1%80%D0%B0%D1%82%D0%B8%D0%B2%D0%BD%D0%BE-%D1%81%D0%BE%D1%81%D1%82%D1%8F%D0%B7%D0%B0%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%B0%D1%8F_%D1%81%D0%B5%D1%82%D1%8C#%D0%9C%D0%B5%D1%82%D0%BE%D0%B4 - кратко о GAN
<br>
https://medium.com/@jonathan_hui/gan-dcgan-deep-convolutional-generative-adversarial-networks-df855c438f - кратко о DCGAN
<br>
https://github.com/tensorflow/tensorflow/blob/r1.13/tensorflow/contrib/eager/python/examples/generative_examples/dcgan.ipynb - генерация рукописных чисел (1)<br>
https://github.com/gsurma/image_generator - генерация изображения симпсона (2)<br>
https://github.com/elcorto/imagecluster - кластеризация изображений (3)<br>


Отличие от датасетов (1) и (2) довольно существенные, а потому и результат хуже. 
## 2 глобальные причины, которые исправить не удалось: 
 * Небольшой датасет
 * Слишком разные картинки. Покемоны настолько разных форм и видов, что выделить хоть какие-либо общие признаки затруднительно. Даже глаза, которые есть почти у всех имеют разную форму, цвет и размер.

 ## Вариант решения 
 Пытаться синтезировать не покемона, похожего на всех сразу, а на сколько-нибудь схожую группу.
 Выделить с датасета невозможно - группы получаются слишком маленькие. (3) использовался именно для этого.

 ## Вариант решения 2
 Cобрать датасет одного и того же покемона с мультфильма и строить покемона похожего на данного.
 Мною не выполнялся, тк долго, ресурсозатратно и незачем.


 ## Итоговый результат:
 Силуэты, некоторые напоминают покемонов. <br>
![alt text](https://raw.githubusercontent.com/ipceeh/pokemon_image_generation/master/images/1.png?raw="True")
![alt text](https://raw.githubusercontent.com/ipceeh/pokemon_image_generation/master/images/2.png?raw="True")
![alt text](https://raw.githubusercontent.com/ipceeh/pokemon_image_generation/master/images/3.png?raw="True")
