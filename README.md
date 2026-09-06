# nn-zth-exercises

Решения упражнений к курсу Andrej Karpathy [«Neural Networks: Zero to Hero»](https://github.com/karpathy/nn-zero-to-hero) — нейросети, собранные с нуля: от автоматического дифференцирования до языковых моделей.

![Python](https://img.shields.io/badge/python-3.9-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)

## Содержание

- [Зачем это](#зачем-это)
- [Структура](#структура)
- [Прогресс по лекциям](#прогресс-по-лекциям)
- [Запуск](#запуск)
- [Источники и лицензия](#источники-и-лицензия)

## Зачем это

Курс разбирает нейросети снизу вверх: сначала пишется собственный движок автоградиента, потом на нём — языковые модели, и только затем появляется PyTorch. Смысл упражнений в том, чтобы ни один слой не оставался чёрным ящиком: backprop считается руками, инициализация весов выводится, а не берётся по умолчанию, батчнорм собирается из формулы.

Здесь лежат мои решения упражнений, а не конспект лекций.

## Структура

Один каталог на лекцию: ноутбук с решением и короткий `readme.md` с условиями упражнений.

| Каталог | Тема | Ноутбук |
|---|---|---|
| [`exercise-1/`](exercise-1) | micrograd: автоматическое дифференцирование, обратное распространение с нуля | [`ex_01.micrograd_exercises.ipynb`](exercise-1/ex_01.micrograd_exercises.ipynb) |
| [`exercise-2/`](exercise-2) | makemore: посимвольная языковая модель, биграммы и триграммы | [`ex_02.character-level-language-model.ipynb`](exercise-2/ex_02.character-level-language-model.ipynb) |
| [`exercise-3/`](exercise-3) | makemore part 2: многослойный перцептрон, эмбеддинги символов | [`ex_03.MLP.ipynb`](exercise-3/ex_03.MLP.ipynb) |
| [`exercise-4/`](exercise-4) | makemore part 3: функции активации, градиенты, батч-нормализация | [`ex_04.activation-and-gradients-and-batchnorm.ipynb`](exercise-4/ex_04.activation-and-gradients-and-batchnorm.ipynb) |

## Прогресс по лекциям

**Лекция 1** — [The spelled-out intro to neural networks and backpropagation: building micrograd](https://www.youtube.com/watch?v=VMj-3S1tku0)

- [x] Производные
- [x] Поддержка softmax

**Лекция 2** — [The spelled-out intro to language modeling: building makemore](https://www.youtube.com/watch?v=PaCmpygFfXo)

- [x] Триграммная модель
- [x] Разбиение на train / dev / test
- [x] Регуляризация
- [x] Отказ от one-hot векторов
- [x] Перекрёстная энтропия вместо ручной функции потерь

**Лекция 3** — [Building makemore Part 2: MLP](https://www.youtube.com/watch?v=TCH_1BHY58I)

- [x] Подбор гиперпараметров
- [x] Корректная инициализация весов
- [x] Реализация одной из идей статьи [Bengio et al., 2003](https://www.jmlr.org/papers/volume3/bengio03a/bengio03a.pdf)

**Лекция 4** — [Building makemore Part 3: Activations & Gradients, BatchNorm](https://www.youtube.com/watch?v=P6sfmUTpUmc)

- [x] Инициализация весов и смещений нулями
- [x] Батч-нормализация

**Лекция 5** — [Building makemore Part 4: Becoming a Backprop Ninja](https://www.youtube.com/watch?v=q8SA3rM6ckI)

- [ ] Обратное распространение через всю сеть вручную
- [ ] Backprop через cross entropy одним выражением
- [ ] Backprop через batchnorm одним выражением
- [ ] Сборка всего вместе

**Лекция 6** — [Building makemore Part 5: Building a WaveNet](https://www.youtube.com/watch?v=t3YJ5hKiMQ0) — упражнений нет

**Лекция 7** — [Let's build GPT: from scratch, in code, spelled out](https://www.youtube.com/watch?v=kCc8FmEb1nY)

- [ ] Объединить `Head` и `MultiHeadAttention` в один класс
- [ ] Обучить GPT на собственном датасете
- [ ] Предобучение на большом корпусе
- [ ] Реализовать одну дополнительную идею из статьи о трансформерах

## Запуск

```bash
git clone https://github.com/HasagiGr/nn-zth-exercises.git
cd nn-zth-exercises

python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt

jupyter notebook
```

Ноутбуки рассчитаны на CPU: модели небольшие, GPU не требуется.

## Источники

Лекции и постановки упражнений — [karpathy/nn-zero-to-hero](https://github.com/karpathy/nn-zero-to-hero). В этом репозитории лежат только мои решения.

