# img2text

## Структура данных
### В контейнер помещается папка images, в которой находятся изображения, на которых необходимо сделать предсказания. Модель должна сформировать файл предсказания формата json, который содержит предсказания для каждого изображения из папки images. Пример содержимого json файла, который должен быть сгенерирован:
```
{
"img_0.jpg": {
        "predictions": [
            {
                "polygon": [
                    [0, 0],
                    [0, 1],
                    [1, 0],
                    [1, 1]
                ],
                "text": "test"
            }
        ]
    }
    "img_1.jpg": {
    "predictions": [
    ...
    ]
    }
}
```
### Пути к данным для изображений (полный путь к папке images) и путь, куда необходимо сохранить результат (файл формата .json) передаются как первые два аргумента при запуске вашего решения. Их можно считать с помощью sys.argv[1:].
