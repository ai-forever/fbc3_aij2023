# FusionBrain Challenge 3.0: Multimodal model for Gigachat

## Общее описание задачи
В рамках данного соревнования участникам предстоит построить модель, способную вести полноценный мультимодальный диалог с пользователем. Модель должна уметь принимать на вход данные **трех модальностей: тексты, изображения и аудио**, анализировать их, учитывая контекст, и выводить ответ на естественном языке. В данном соревновании мы заранее не определяем конкретные задачи, с которыми предстоит справиться моделям участников. Вместо этого мы предлагаем решить все возможные задачи, которые могут возникать в процессе мультимодального диалога с использованием трех модальностей, и решение которых может быть сформулировано на естественном языке. Цель соревнования - проверить, насколько успешно модели, предложенные участниками смогут справиться с извлечением информации и связыванием трех модальностей, а также поддержанием контекста на протяжении всего диалога. 

Основным навыком, на основе корого будут сравниваться модели участников соревнования, будет **умение вести мультимодальный диалог с пользователем**, в котором модель выступает в виде полезного, вежливого и правдивого "Ассистента".
Однако, поскольку данная задача очень обширна, мы разделили все диалоги в ее рамках на несколько типов:
* **Текст-текст** <br>
Это стандартные унимодальные диалоги, в которых как вопросы пользователя, так и ответы ассистента выражены в текстовом виде. Вопросы могут требовать от модели обладание знаниями о мире, а также способность учитывать контекст диалога.
* **Изображение-текст**  <br>
Это первый тип бимодальных диалогов, в которых обязательно присутствует одно или несколько изображений и текстовые вопросы, для ответа на которые требуется произвести анализ изображения.
* **Аудио-текст** <br>
Это второй тип бимодальных диалогов, в которых обязательно присутствует один или несколько аудиозаписей и текстовые вопросы, для ответа на которые требуется произвести анализ аудио.
* **Изображения-аудио-текст** <br>
Это полностью мультимодальный тип диалогов, который объединяет все модальности, рассматриваемые в соревновании. В диалоге может встретиться одно или несколько изображений, а также одна или несколько аудиозаписей. Текстовые вопросы могут быть заданы по изображениям и аудио, присутствующим в диалогах. Вопрос может быть задан только к одной модальности или сразу к обеим.


### Примеры диалогов

## Описание формата решения

### Формат решения

### Метрики

Оценка ответов участников производится по двум метрикам: генеративной и некоторой *скрытой* метрике. 
* Метрику оценки генерации ответов модели предлагается рассчитывать с применением **METEOR**, которая умножается на весовой коэффициент, в зависимости от типа диалога, к которому относится реплика. 
* Скрытая метрика основывается на **внутренней оценке уверенности модели в ответе**. Участникам предлагается, в рамках вычисления данной метрики, предоставлять численное значение перплексии модели в ответ на входные данные. В дальнейшем, показатель перплексии будет использоваться в расчете скрытой метрики.

Финальный результат участника и распределение мест будет оцениваться в соответствии с **интегральной метрикой**. <br>
Подробное описание метрик и их расчета можно почитать тут.

### Ограничения

## Baseline решение

## Данные для обучения

Подробное описание предложеных для обучения датасетов можно почитать тут.

### Текстовые датасеты

### Картиночные датасеты

### Аудио датасеты

### Мультимодальные датасеты