# Данные
Ниже приведено подробное описание разнообразных наборов данных, 
которые мы предлагаем использовать для обучения мультимодальной модели.

Основная задача мультимодального обучения - заложить в модели способность 
извлекать полезный сигнал как из унимодальных данных любой природы, 
так и из любой пары или группы модальностей. В последнем случае крайне важно наладить 
понимание связей между данными разной природы и научить ассистента составлять общую картину на их основе.


Поэтому предлагаемые наборы данных мы разделили на несколько категорий по типу 
и числу модальностей: 

* **[Бимодальные](#бимодальные)**:
  * [Текстово-картиночные датасеты](#текстово-картиночные-датасеты)
  * [Текстово-аудио датасеты](#текстово-аудио-датасеты)
* **[Мультимодальные](#мультимодальные)**

Так же мы специально собрали ряд **[мультимодальных диалоговых наборов данных](#мультимодальные-диалоговые-датасеты)**.


| Датасет                        | Текст  📝      | Изображения    🎨 | Аудио 🎼                                                       | Задача(и)                                                          |                                                 Объем |
|--------------------------------|--------------|-------------------|----------------------------------------------------------------|--------------------------------------------------------------------|------------------------------------------------------:|
| VQA v2.0              |     ✔️     | ✔️                |                                                                | Visual Question Answering (VQA)                                    |               265 тыс. изображений, 795 тыс. вопросов |
| OK-VQA                         |  ✔️   | ✔️                |                                                                | Visual Question Answering (VQA)                                    |                                       14 тыс. вопрсов |
| Visual Genome                  |   ✔️   | ✔️                |                                                                | Visual Question Answering (VQA)                                    |                101,174 изображений,  1.7 млн вопросов |
| MiniGPT-4 Dataset              |  ✔️   | ✔️                |                                                                | Visual Question Answering (VQA), Image Captioning, Instruct tuning |                                                5 тыс. |
| LLaVA Instruct Dataset         |  ✔️   | ✔️                |                                                                | Conversation, Image Captioning, Visual Reasoning, Instruct tuning  |                                              158 тыс. |
| AudioSet                       |    ✔️    |                   | ✔️                                                             | Audio Classification                                               |                                              1.7 млн. |
| AudioCaps                      |   ✔️    |                   | ✔️                                                             | Audio Captioning                                                   |                                               46 тыс. |
| VGG-Sound                      |   ✔️     |                   | ✔️                                                             | Audio Classification                                               |                                              200 тыс. |
| Clotho                         |    ✔️    |                   | ✔️                                                             | Audio Captioning                                                   |                          4981 записей, 24,905 текстов |
| VGG-SS                         |   ✔️     | ✔️                | ✔️                                                             | Audio-Visual Grounding                                             |                                        5 тыс. записей |
| Multi-modal Instruction Dataset |  ✔️     | ✔️             |   | ️    Multi-modal Instruction tuning                            | 109 тыс. пар изображение-инструкция                                |                                                       
| MIMIC-IT                       |    ✔️    | ✔️                | ️     |      Multi-modal Instruction tuning                                | 2.8 млн. изображения, 2.2 млн. инструкций                          |                                                       
| Visual Dialog v1.0             |    ✔️    | ✔️                | | Conversation, Image Captioning, Visual Question Answering (VQA) | 130 тыс. изображений                                               |                                                       
| CLEVR-Dialog                   |     ✔️   | ✔️        |        | Conversation, Visual Reasoning                                 | 4.25 млн. диалогов                                                 |                                                       
| Image-Chat                     |   ✔️       | ✔️      |          | Conversation,   Visual Question Answering (VQA)                | 201 тыс. пар изображение-диалог                                    |                                                       


## Бимодальные

### Текстово-картиночные датасеты

#### Visual Question Answering v2.0 (VQA v2.0)
##### Описание
Visual Question Answering v2.0 - это набор данных, предназначенный для генерации ответов на открытые вопросы на естественном языке
по изображениям. Что бы ответить на задаваемые вопросы потребуется понимание как естественного языка и визуального контента, 
так и наличие навыков зравого смысла и некоторой эрудированности.

<div align="center">
  <img src="https://visualqa.org/static/img/vqa_examples.jpg" alt="examples" width="600">
</div>

Датасет состоит из 265,016 изображений, часть из которых была выбрана из датасета [СOCO](https://cocodataset.org/#home), а часть собрана из открытых источников.
К каждой картинке задается как минимум 3 вопроса (в среднем 5.4 вопроса на изображение). 
К каждому вопросу собран список из 10 правильных ответов в различной формулировке, 
а также трех композиционно и стилистически правильно составленных, однако не верных по смыслу ответов. 

📄 <a href="https://arxiv.org/pdf/1612.00837v3.pdf" style="color: black; text-decoration: bold;"> Статья </a>    
🗃️ <a href="https://visualqa.org/" style="color: black; text-decoration: bold"> Датасет </a> 

#### OK-VQA (Outside Knowledge Visual Question Answering)
##### Описание
Outside Knowledge Visual Question Answering (OK-VQA) - это набор данных, который также предназначен для генерации ответов на открытые вопросы на естественном языке
по изображениям. Однако, в данном случае, одного лишь визуального содержания не достаточно для того, что бы решить задачу - 
все вопросы в данном датасете требуют либо исключительной эрудированности модели, 
либо доступа к внешним базам знаний (преимущественно к Википедии).

<div align="center">
  <img src="https://okvqa.allenai.org/static/img/Dataset_Example_Categories_v2.jpg" alt="examples" width="600">
</div>

Датасет состоит из 14,055 вопросов, которые требуют знаний о мире, и соответствующих им изображений.
К каждому вопросу собрано по 5 правильных ответов в различной формулировке. 
Из набора данных исключены вопросы с наиболее популярными и очевидными ответами.

📄 <a href="https://arxiv.org/pdf/1906.00067.pdf" style="color: black; text-decoration: bold;"> Статья </a>    
🗃️ <a href="https://okvqa.allenai.org/" style="color: black; text-decoration: bold"> Датасет </a> 

#### Visual Genome
##### Описание

Visual Genome - это набор данных для решения задачи Visual Question Answering в формате множественного выбора ответа (multi-choice setting).
Относительно ранее описанного Visual Question Answering Dataset, Visual Genome предоставляет более сбалансированное 
распределение вопросов по 6 основным формулировкам: 'Что?', 'Где?', 'Когда?', 'Кто?', 'Почему?' и 'Как?'.

<div align="center">
  <img src="https://production-media.paperswithcode.com/datasets/Visual_Genome-0000000087-aaf04589_6fjxO1x.jpg" alt="examples" width="600">
</div>

Датасет состоит из 101,174 изображений, собранных из MSCOCO, и 1.7 млн. пар "вопрос-ответ". 
В среднем, к каждой картинке подобрано по 17 вопросов. 
Кроме того, в рамках датасета представлен еще набор из 108 тыс. изображений с размеченными сегментами визуальных сцен, 
включающих в себя объекты и их отношения.

📄 <a href="https://arxiv.org/pdf/1602.07332v1.pdf" style="color: black; text-decoration: bold;"> Статья </a>    
🗃️ <a href="https://homes.cs.washington.edu/~ranjay/visualgenome/index.html" style="color: black; text-decoration: bold"> Датасет </a> 


#### MiniGPT-4 Instruct Dataset
##### Описание

MiniGPT-4 Instruct Dataset - это небольшой набор мультимодальных визуально-текстовых данных, направленный на обучение модели мультимодальному 
следованию инструкциям. Генерация датасета была разделена на два этапа и проходила в атоматизированном режиме, без ручной разметки.

Датасет состоит из 5,000 пар "изображение - подробное текстовое описание", 
где визуальная часть была отобрана из Conceptual Caption dataset.
Детальное текстовое описание содержания изображения было сгенерировано с помощью модели MiniGPT-4 
(в том числе представлненной авторами датасета) и проверено на корректность с использованием ChatGPT.

📄 <a href="https://arxiv.org/pdf/2304.10592" style="color: black; text-decoration: bold;"> Статья </a>    
🗃️ <a href="https://minigpt-4.github.io/" style="color: black; text-decoration: bold"> Датасет </a> 

#### LLaVA Instruct Dataset
##### Описание
LLaVA Instruct Dataset - это набор мультимодальных визуально-текстовых данных, который был создан 
автоматизированно с использованием разметки от ChatGPT/GPT-4. 
Он предназначен для обучения моделей следованию инструкциям (instruction-following) на основе мультимодального контекста. 

<div align="center">
  <img src="https://llava-vl.github.io/images/cmp_ironing.png" alt="examples" width="600">
</div>

В рамках следования инструкциям пользователя, в датасете выделены три основные постановки задачи:
* **Диалог** (conversation) - представляет собой обсуждение между умным ассистентом и пользователем содержания визульного контента.
* **Подробное описание изображения** - направлена на проверку способностей мультимодального ассистента детально описывать изображения.
* **Многоступенчатое логическое рассуждение** - требует от мультимодального ассистента продемонстрировать навык логического рассуждения и здравого смысла в рамках диалога с пользователем.

📄 <a href="https://arxiv.org/pdf/2304.08485" style="color: black; text-decoration: bold;"> Статья </a>    
🗃️ <a href="https://llava-vl.github.io/" style="color: black; text-decoration: bold"> Датасет </a>


### Текстово-аудио датасеты

#### AudioSet
##### Описание

AudioSet - это крупный набор текстово-звуковых данных, 
включающий в себя: видеофайлы, прилагающиеся к ним аудио дорожки и текстовые метки, определяющие категории звуков, 
присутствующих в звукозаписях. Датасет использует видеозаписи из разнообразных доменов и классифицирует звуки на более чем 600 категорий 
(к данным также прилагается онтология всех возможных звуков), представляемых в виде иерархии. 
Например: “Sounds of things” - “Vehicle” - “Motor vehicle” - “Emergency vehicle” - “Siren” - “Ambulance (siren)”.

<div align="center">
  <img src="https://research.google.com/audioset/resources/histogram.svg" alt="examples" width="500">
</div>

📄 <a href="https://research.google/pubs/pub45857.pdf" style="color: black; text-decoration: bold;"> Статья </a>    
🗃️ <a href="https://research.google.com/audioset/download.html" style="color: black; text-decoration: bold"> Датасет </a> 

#### AudioCaps
##### Описание

AudioCaps - это набор текстово-звуковых данных, состоящий из 46 тыс. пар аудио файл - текстовое описание звука. 
Аудио записи были получены из набора данных AudioSet 
(включающего 1.7 млн. 10-ти секундных Youtube видео клипов и используемого для классификации на 527 категорий звуков), 
путем извлечения только звуковой дорожки из видео. 
Было проведено существенное сокращения числа экземпляров путем исключения мало ресурсных и сложно распознаваемых 
человеком классов (в итоговом наборе оставлено 75 категорий звуков). Описание для звуков было получено 
через разметку в Amazon Mechanical Turk со строгим контролем качества текста.

<div align="center">
  <img src="https://production-media.paperswithcode.com/datasets/Screenshot_2021-07-26_at_13.35.26.png" alt="examples" width="400">
</div>

📄 <a href="https://aclanthology.org/N19-1011.pdf" style="color: black; text-decoration: bold;"> Статья </a>    
🗃️ <a href="https://audiocaps.github.io/" style="color: black; text-decoration: bold"> Датасет </a>

#### VGG-Sound
##### Описание
VGG-Sound - это набор визуально-звуковых данных, состоящий из коротких клипов и соответствующих звуковых дорожек, которые были выгружены с YouTube. 
Все аудио/визуальные элементы датасета были отнесены к одному из 300+ классов. В общей сложности, набор данных включает более 550 часов и более 200 тыс. 
видео-аудио записей.

📄 <a href="https://arxiv.org/pdf/2004.14368v2.pdf" style="color: black; text-decoration: bold;"> Статья </a>    
🗃️ <a href="https://www.robots.ox.ac.uk/~vgg/data/vggsound/" style="color: black; text-decoration: bold"> Датасет </a> 


#### Clotho
##### Описание

Clotho - это набор аудио-текстовых данных, направленный на решение задачи описания аудио записей на естественном языке.
Он состоит из 4981 аудио дорожек, длительностью от 15 до 30 секунд. 
К каждой из записей создано порядка 5 текстовых описаний (в общей сложности 24,905 текстов), длиной от 8 до 20 слов.

📄 <a href="https://arxiv.org/pdf/1910.09387" style="color: black; text-decoration: bold;"> Статья </a>    
🗃️ <a href="https://zenodo.org/record/3490684" style="color: black; text-decoration: bold"> Датасет </a> 

## Мультимодальные 

#### VGG-SS (VGG-Sound Source)
##### Описание

VGG-SS (VGG Sound Source)  - это набор аудио-визуально-текстовых данных, основной задачей которого 
является проверка способностей мультимодальной модели локализовать источник звука на видео записи.

Датасет состоит из более 5 тыс. видео записей распределенных на 200 категорий. 
Аудио-визуальная часть с текстовыми тегами категории записи была собрана из вышеописанного [VGG-Sound dataset](#vgg-sound).
Каждый ролик был размечен таким образом, что бы источник основного звука был легко различим и локализуем в кадре 
путем охватывающего прямоугольника из точек.

<div align="center">
  <img src="https://www.robots.ox.ac.uk/~vgg/research/lvs/data/vggss_s.png" alt="examples" width="500">
</div>

📄 <a href="https://www.robots.ox.ac.uk/~vgg/publications/2021/Chen21/chen21.pdf" style="color: black; text-decoration: bold;"> Статья </a>    
🗃️ <a href="https://www.robots.ox.ac.uk/~vgg/research/lvs/" style="color: black; text-decoration: bold"> Датасет </a> 

#### Multi-modal Instruction Dataset
##### Описание

Multi-modal Instruction Dataset - это набор данных, состоящий из коротких диалогов (вопрос и одна реплика) 
на основании изображения и его текстового описания. 
Разметка диалогов была реализована через отправку текстовых запросов на генерацию вопроса по описанию изображения языковой модели GPT-3.5-Turbo, 
причем текстом были описаны как изображения, так и видео. 
По результатам данных автоматически созданных диалогов проводилась ручная валидация разметчиками.
Изображения (всего 69 тыс.) для визуальных диалогов были собраны из [COCO Dataset image captions](https://cocodataset.org/#home) и 
[VQA Dataset](https://visualqa.org/download.html) датасета, а видео из [Charades](https://allenai.org/plato/charades/) 
и [Video Dialog captions](https://video-dialog.com/) (всего 50 тыс.). 

<div align="center">
  <img src="https://github.com/lyuchenyang/Macaw-LLM/blob/main/assets/dataset_table.png" alt="examples" width="500">
</div>

📄 <a href="https://arxiv.org/pdf/2306.09093" style="color: black; text-decoration: bold;"> Статья </a>    
🗃️ <a href="https://github.com/lyuchenyang/Macaw-LLM#new-multi-modal-instruction-dataset-" style="color: black; text-decoration: bold"> Датасет </a> 


#### MIMIC-IT
##### Описание

Набор данных MultI-Modal In-Context Instruction Tuning (MIMIC-IT) состоит из 2.8 млн. пар изображения (-ий, в случае видео запроса) 
и инструкции (2.2 млн. уникальных инструкций). Визуальная составляющая датасета была собрана из разнообразных источников 
и доменов (всего использовано 7 визуальных датасетов), включая общие сцены, RGB-D, TV видео, видео с egocentric камер (AR) 
и т. п. Отличительная черта набора - формулировка инструкций не только к единичному изображению, 
но и к нескольким или последовательности кадров видео, подаваемым на вход в едином семпле. 
Каждый семпл включает в себя как минимум одну мультимодальную пару и одну исключительно языковую пару контекста/инструкции.

<div align="center">
  <img src="https://camo.githubusercontent.com/95426e8fa0af2c75a31563bc535a55ff810f8690b318a26d8de5d9db6be8a919/68747470733a2f2f692e706f7374696d672e63632f34783636674868772f6d696d69632d69742e6a7067" alt="examples" width="700">
</div>

📄 <a href="https://arxiv.org/pdf/2306.05425" style="color: black; text-decoration: bold;"> Статья </a>    
🗃️ <a href="https://github.com/Luodian/Otter/tree/main/mimic-it" style="color: black; text-decoration: bold"> Датасет </a>

## Мультимодальные диалоговые датасеты

#### Visual Dialog v1.0
##### Описание

Visual Dialog - это набор данных, состоящий из диалогов на основе визуальной составляющей картинки. 
Каждый диалог включает в себя изображение с описанием и 10 вопросно-ответных пар, направленный на описание его содержания. 
В основе визуальной части датасета использовались картинки и описания из COCO и Flickr 
(~130 тыс. изображений из COCO-train2014, COCO-val2014 и Flickr).

<div align="center">
  <img src="https://production-media.paperswithcode.com/datasets/VisDial-0000003368-deeb9b6d.jpg" alt="examples" width="500">
</div>

📄 <a href="https://arxiv.org/pdf/1611.08669.pdf" style="color: black; text-decoration: bold;"> Статья </a>    
🗃️ <a href="https://visualdialog.org/" style="color: black; text-decoration: bold"> Датасет </a> 

#### CLEVR-Dialog
##### Описание

CLEVR-Dialog - это набор данных, состоящий из визуальных диалогов, который направлен на оценку способностей мультимодальных моделей 
проводить несложные причинно-следственные рассуждения на основании истории диалога и визуального контента. 
Датасет состоит 85 тыс. изображений и диалогов из 10 пар реплик на их основе (всего 4.25 млн. пар "вопрос-ответ").

<div align="center">
  <img src="https://i.imgur.com/mwC1mVC.png" alt="examples" width="600">
</div>

📄 <a href="https://arxiv.org/pdf/1903.03166" style="color: black; text-decoration: bold;"> Статья </a>    
🗃️ <a href="https://github.com/satwikkottur/clevr-dialog/tree/master" style="color: black; text-decoration: bold"> Датасет </a> 

#### Image-Chat
##### Описание

Image-Chat - это набор данных, состоящий из коротких (до 3-х реплик) визуальных диалогов: 
изображение, один или пара интентов (настроение, стиль речи для каждого из участников диалога, или исключительно для ответов модели) 
и от одной до трех реплик относящихся к содержанию картинки. 
Изображения для датасета были выбраны из [YFCC100MDataset](https://multimediacommons.wordpress.com/yfcc100m-core-dataset/).

<div align="center">
  <img src="https://production-media.paperswithcode.com/datasets/53147161-e87e-4307-9a36-0a561db487fd.jpg" alt="examples" width="600">
</div>

Диалог строился следующим образом: для каждого изображения случайным образом выбирались два интента для каждого из участника А и B, 
далее двух разметчиков просили составить обсуждение к изображению с учетом выданных им черт характера (интентов). 

📄 <a href="https://aclanthology.org/2020.acl-main.219.pdf" style="color: black; text-decoration: bold;"> Статья </a>    
🗃️ <a href="https://parl.ai/projects/image_chat/" style="color: black; text-decoration: bold"> Датасет </a>

