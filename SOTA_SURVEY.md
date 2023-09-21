# The Survey of SoTA Multimodal Architectures (2023).

За последний год мы стали свидетелями стремительного развития больших языковых моделей 
(Large Language Models, LLMs), которые продемонстрировали уникальные интеллектуальные способности такие как: 
понимание, логическое рассуждение и обучение новым навыкам, аналогично тому, как сами люди получают 
и анализируют знания, рассуждают и принимают решения.

Обладая высоким уровнем интеллекта и возможностью интерактивно взаимодействовать с человеком, 
языковые модели позволяют создавать универсальные диалоговые системы, выполняющие инструкции пользователя. 

Однако задачи, которые ставит перед диалоговой системой человек не всегда заключаются только в естественном языке. 
Для того, чтобы раскрыть потенциальные возможности применения LLM за пределами одного лишь естественного языка, 
в ряде исследований, опубликованных в последние годы, были предприняты успешные попытки наладить взаимодействие 
языковых моделей с множеством разнообразных сигналов других модальностей (например, изображениями, видео, речью и аудио).
Таким образом, были предприняты попытки построения куда более умных и разноплановых диалоговых систем.

Поэтому, в качестве идейного вдохновения для создания модели умного мультимодального Ассистента мы предлагаем 
участникам ознакомиться с собранной нами подборкой SOTA мультимодальных архитектур 
на основе больших языковых моделей (Multimodal Large Language Models, MLLMs) за последний 2023 год.
С более ранними обзорами за 2021 и 2022 годы можно ознакомиться по ссылкам: Survey MLLM 2021 и Survey MLLM 2022.


## Surveys

Для начала мы предлагаем участникам самостоятельно ознакомиться с комплексными и наиболее полными обзорами текущего 
“ландшафта” разработки мультимодальных архитектур, которые были опубликованы за последние годы:

1. [Foundations and Trends in Multimodal Machine Learning: Principles, Challenges, and Open Questions](https://arxiv.org/abs/2209.03430) (```Paul Pu Liang, Amir Zadeh, Louis-Philippe Morency, Sep. 2022```) — эта статья предлагает верхнеуровневый обзор теоретических и практических основ мультимодальных языковых моделей через определение трех основополагающих аспектов объединения модальностей: гетерогенности (heterogeneity), связанности (connections) и взаимосвязи (interactions). Также предлагается таксономия из шести основных задач: представление данных (representation), согласованность между представлениями модальностей (alignment), рассуждение (reasoning), генерация (generation), способности к генерализации на новые задачи (transference) и масштабируемость модели на новые модальности (quantification), охватывающую исторические и последние тенденции.
2. [A Survey on Multimodal Large Language Models](https://arxiv.org/abs/2306.13549) (```Yin et. al., June 2023```) — в этой статье подробно описываются последние достижения в области MLLM (Multimodal Large Language Models) в разрезе четырех основных техник реализации подобных архитектур: Multimodal Instruction Tuning (M-IT), Multimodal In-Context Learning (M-ICL), Multimodal Chain of Thought (M-CoT), и LLM-Aided Visual Reasoning (LAVR). К каждому из описанных направлений собрана детальная таксономия с примерами реализа
3. [Multimodal Learning with Transformers: A Survey](https://arxiv.org/abs/2206.06488) (```Peng Xu, Xiatian Zhu, David A. Clifton, May 2023```) — эта статья предоставляет читателю полноценный обзор применения трансформерных моделей к мультимодальным данным. Она включает как основополагающее описание разнообразных трансформерных архитектур (от Vanilla Transformer и Vision Transformer  до более комплексных мультимодальных Transformers) и методов их предобучения, так и перечень возможных практических задач в рамках применения мультимодальных моделей.
4. [Multi-modal Machine Learning in Engineering Design: A Review and Future Directions](https://arxiv.org/abs/2302.10909) (```Binyang Song, Rui Zhou, Faez Ahmed, Feb. 2023```) — в данной статье подробно исследуются наиболее современные задачи применения мультимодальных моделей машинного обучения (Multimodal Models of Machine Learning, MMML) в разрезе пяти фундаментальных задач мультимодального обучения: мультимодальное представление данных (multi-modal information representation), объединение различных источников данных (fusion), согласованность между представлениями модальностей (alignment), перенос информации в рамках модальностей (translation), и объединенное обучение моделей на нескольких источниках сигналов разной природы (co-learning).

## SoTA Мультимодальные архитектуры

Далее, приводится краткий обзор основных опубликованных работ по теме мультимодальности (за период 2023 года), которые либо показали выдающееся качество решений по ряду задач и модальностей, либо привнесли в это поле исследований новые принципы построения архитектуры моделей.

1. [BLIP-2: Bootstrapping Language-Image Pre-training with Frozen Image Encoders and Large Language Models](https://arxiv.org/abs/2301.12597) (```Junnan Li, Dongxu Li, Silvio Savarese, Steven Hoi, 30 January 2023```)
2. [FROMAGe: Grounding Language Models to Images for Multimodal Inputs and Outputs](https://arxiv.org/abs/2301.13823) (```Jing Yu Koh, Ruslan Salakhutdinov, Daniel Fried, 31 January 2023```)
3. [Kosmos-1: Language Is Not All You Need Aligning Perception with Language Models](https://arxiv.org/abs/2302.14045) (```Huang et. al., 1 March 2023```)
4. [MiniGPT-4: Enhancing Vision-Language Understanding with Advanced Large Language Models](https://arxiv.org/abs/2304.10592) (```Deyao Zhu, Jun Chen, Xiaoqian Shen, Xiang Li, Mohamed Elhoseiny, 20 April 2023```)
5. [LLaVA: Visual Instruction Tuning](https://arxiv.org/abs/2304.08485) (```Haotian Liu, Chunyuan Li, Qingyang Wu, Yong Jae Lee, 30 April 2023```)
6. [LLaMA-Adapter: Efficient Fine-tuning of Language Models with Zero-init Attention](https://arxiv.org/abs/2303.16199) (```Zhang et. al., 28 March 2023```)
7. [LLaMA-Adapter V2: Parameter-Efficient Visual Instruction Model](https://arxiv.org/abs/2304.15010) (```Gao et. al., 28 April 2023```)
8. [Otter: A Multi-Modal Model with In-Context Instruction Tuning](https://arxiv.org/abs/2305.03726) (```Li et. al., 5 May 2023```)
9. [ONE-PEACE: Exploring One General Representation Model Toward Unlimited Modalities](https://arxiv.org/abs/2305.11172) (```Wang et. al., 18 May 2023```)
10. [GILL: Generating Images with Multimodal Language Models](https://arxiv.org/abs/2305.17216) (```Jing Yu Koh, Daniel Fried, Ruslan Salakhutdinov, 26 May 2023```)
11. [ImageBind: One Embedding Space To Bind Them All](https://arxiv.org/abs/2305.05665) (```Girdhar et. al., 31 May 2023```)
12. [InstructBLIP: Towards General-purpose Vision-Language Models with Instruction Tuning](https://arxiv.org/abs/2305.06500) (```Dai et. al., 15 June 2023```)
13. [BuboGPT: Enabling Visual Grounding in Multi-Modal LLMs](https://arxiv.org/abs/2307.08581) (```Zhao et. al., 17 July 2023```)
14. [IDEFICS & OBELICS: An Open Web-Scale Filtered Dataset of Interleaved Image-Text Documents](https://arxiv.org/abs/2306.16527) (```Laurencon et. al., 21 August 2023```)
15. [ImageBind-LLM: Multi-modality Instruction Tuning](https://arxiv.org/abs/2309.08637) (```Li et. al., 7 September 2023```)
16. [TextBind: Multi-turn Interleaved Multimodal Instruction-following in the Wild](https://arxiv.org/abs/2309.03905) (```Han et. al., 14 September 2023```)


