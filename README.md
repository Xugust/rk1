#РК1

выполнил Макеенков Данила, ИУ8-23

ссылка на вариант 16: https://github.com/vkhorikov/CSharpFunctionalExtensions

1. Название проекта
```
CSharpFunctionalExtensionss
```

2. Краткое описание проекта (одной фразой). (Это скорее для вас может быть полезно, потому что некоторые из проектов интересны сами по себе - коснетесь в современных разработок)
```bash
библиотека в данном проекте помогает писать код более функциональным способом
```

3. Количество файлов
```bash
$ git ls-files | wc -l
```
```
595
```

4. Объем всех файлов
```bash
$ git ls-files | xargs wc -c | awk '{total += $1} END {print total}'
```
```
4140758
```


5. Объем исходного кода: cpp, c, h, hpp, cxx, py, pl, php, java, cs, rb, rs, hs
```bash
$ git ls-files | grep -E ".(cpp|c|h|hpp|cxx|py|pl|php|java|cs|rb|rs|hs)$" | xargs wc -c | awk '{total += $1} END {print total}'
```
```
3926306
```

6. Найти, если есть файл .clang-format
```bash
$ find . -type f -name ".clang-format"
```
```
пустой вывод - нет .clang-format
```

7. Если есть каталог src, то общее количество файлов в каталоге src
```bash
$ find src -type f | wc -l
```
```
нет такого файла или каталога
```

8. Выписать количество файлов, содержащих слово socket независимо от написания строчными или прописными буквами во всех файлах репозитория.
```bash
$ git grep -l -i "socket" | wc -l
```
```
0
```

9. Выписать количество файлов, содержащих слово select независимо от написания строчными или прописными буквами во всех файлах репозитория.
```bash
$ git grep -l -i "select" | wc -l
```
```
81
```

10. Выписать количество раз, сколько, содержится слово Microsoft, Google или Intel независимо от написания строчными или прописными буквами во всех файлах репозитория.
```bash
$ git grep -i -e "Microsoft" -e "Google" -e "Intel" | wc -l
```
```
10
```

11. Найти расположение файла LICENSE относительно начала репозитория.
```bash
$ find . -name LICENSE*
```
```
./LICENSE
```

12. Вывести строку для файла LICENSE (если он есть), содержащую следующие подпоследовательности символов: BSD, GNU, MIT, APSL, Apache, GPL, AGPL, LGPL
```bash
$ grep -e "BSD" -e "GNU" -e "MIT" -e "APSL" -e "Apache" -e "GPL" -e "AGPL" -e "LGPL" LICENSE.txt
```
```
The MIT License (MIT)
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
```
