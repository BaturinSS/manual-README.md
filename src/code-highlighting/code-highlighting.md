
## Подсветка кода

### ![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+) Если нужно `выделить` слово или фразу `внутри строки, то используются одинарные` обратные кавычки:

```
Это `слово` выделется.
В этом предложении `нужно выделить часть` предложения.
```
### _Пример:_

Это `слово` выделется.    
  
В этом предложении `нужно выделить часть` текста.

![#c5f015](https://via.placeholder.com/1100x5/c5f015/000000?text=+)

#### ![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+) Для выделения в блоки - тройные обратные ковычки:

    ```
    Сдесь выделено несколько строк.
    Это `слово` выделется.    
    В этом предложении `нужно выделить часть` текста.
    Как вы уже обратили внимание в нутри выбеления блока НЕЛЬЗЯ выделить слово или часть предложения.
    ```
    
### _Пример:_

 ```
Сдесь выделено несколько строк.
Это `слово` выделется.    
В этом предложении `нужно выделить часть` текста.
Как вы уже обратили внимание в нутри выбеления блока НЕЛЬЗЯ выделить слово или часть предложения.
```

![#c5f015](https://via.placeholder.com/1100x5/c5f015/000000?text=+)

#### ![#c5f015](https://via.placeholder.com/15/c5f015/000000?text=+) Дополнительно можно задавать язык кода внутри блока, указав его после первых трех кавычек:

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
    
    ```javaScript
         setItem(element, createdSubmit) {
           createdSubmit
             ? this._container.prepend(element)
             : this._container.append(element)
    }
    ```
### _Пример блока для `javaScript`_:

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

### _Пример блока для `C#`_:

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

### _Пример блока для `Python`_:

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

![#c5f015](https://via.placeholder.com/1100x5/c5f015/000000?text=+)

## [:arrow_up:  Оглавление](https://github.com/BaturinSS/manual-README.md/blob/main/README.md#оглавление)
