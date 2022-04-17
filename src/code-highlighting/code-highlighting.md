## Подсветка кода

#### Если нужно `выделить` слово или фразу `внутри строки, то используются одинарные` обратные кавычки:

```
Это `слово` выделется.
В этом предложении `нужно выделить часть` предложения.
```
#### Пример выделения слова или предложения:

Это `слово` выделется.    
  
В этом предложении `нужно выделить часть` текста.

#### Для выделения в блоки - тройные:

```
Сдесь выделено несколько строк.
Это `слово` выделется.    
В этом предложении `нужно выделить часть` текста.
Как вы уже обратили внимание в нутри выбеления блока НЕЛЬЗЯ выделить слово или часть предложения.
```

#### Дополнительно можно задавать язык кода внутри блока, указав его после первых трех кавычек:

    ```html
        <input type="text">
    ```

    ```css
        body {
            margin: 0;
            padding: 0;
        }
    ```

    ```php
        <?php phpinfo();?>
    ```
Пример блока для `javaScript`:

```javaScript

export class Section {
  constructor(renderer, containerSelector) {
    this._renderer = renderer;
    //this._container = document.querySelector(containerSelector);
  };

  rendererItems(initialArray) {
    initialArray.forEach((item) => {
      this._renderer(item);
    });
  };

  setItem(element, createdSubmit) {
    createdSubmit
      ? this._container.prepend(element)
      : this._container.append(element)
  };
};

```

Пример блока для `C#`:

```C#
using MarkdownSharp;
using MarkdownSharp.Extensions.Mal;

Markdown mark = new Markdown();

// Short link for MAL - 
// http://myanimelist.net/people/413/Kitamura_Eri => mal://Kitamura_Eri
mark.AddExtension(new Articles()); 
mark.AddExtension(new Profile());

mark.Transform(text);
```

Пример блока для `Python`:

```Python
from timeit import Timer

tmp = "Python 3.2.2 (default, Jun 12 2011, 15:08:59) [MSC v.1500 32 bit (Intel)] on win32."

def case1(): # А. инкрементальные конкатенации в цикле
    s = ""
    for i in range(10000):
        s += tmp

def case2(): # Б. через промежуточный список и метод join
    s = []
    for i in range(10000):
        s.append(tmp)
    s = "".join(s)

def case3(): # В. списковое выражение и метод join
    return "".join([tmp for i in range(10000)])

def case4(): # Г. генераторное выражение и метод join
    return "".join(tmp for i in range(10000))

for v in range(1,5):
    print (Timer("func()","from __main__ import case%s as func" % v).timeit(200))
```
___

## [:arrow_up:  Оглавление](https://github.com/BaturinSS/manual-README.md/blob/main/README.md)
