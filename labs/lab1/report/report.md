---
## Front matter
title: "Отчёт по лабораторной работе №2" 
subtitle: "Дисциплина: Математическое моделирование"
author: "Лушин Артём Андреевич"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: false
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Построение математической модели решения задачи о погоне катера за браконьерской лодкой. 

# Выполнение лабораторной работы

1) Я определил свой вариант: (1132226520 mod 70)+1 = 41.

2) Принимаем за t0=0, Xл = 0 - место нахождения лодки браконьеров в момент обнаружения. За Хк = 17.4 - место нахождения катера береговой охраны относительно лодки браконьеров в момент обнаружения. Вводим полярные координаты. Считаем, что полюс Хл0 - это точка обнаружения лодки браконьеров, а полярная ось r проходит через точку нахождения катера береговой охраны. Траектория движения катера должна быть такой, чтобы и катер, и лодка всё время были на одном расстоянии от полюса. Только в этом случае траектоория катера пересекается с траекторией лодки. Поэтому для начала катер береговой охраны должен двигаться прямолинейно, а затем двигаться вокруг полюса с той же скоростью что и лодка. Чтобы найти расстояние х, необходимо составить уравнение. Пусть через время t катер и лодка окажутся на одном расстоянии х от полюса. За это время лодка пройдет х, а катер k-x или k+x (т.к. надо рассмотреть два варианта развития событий). Время за которое они пройдут это расстояние, вычисляется как x/v или к-x/4.7v. Так как время одно и тоже, то эти величины одинаковые. Тогда неизвестное расстояние х можно найти из следующего уравнения: 

![Нахождение расстояния](/home/aalushin1/report/image/1.png){#fig:001 width=70%}

3) После того, как катер окажется на одном расстоянии, что и лодка, он должен сменить траекторию и начать двигаться вокруг полюса удаляясь от него со скоростью лодки. Для этого скорость катера расскладываем на две составляющие: v_r - радиальная скорость и v_t - это тангенциальная скорость. Радиальная скорость v_r = dr/dt. Тангенциальная скорость равна произведению угловой скорости на радиус. Решение исходной задачи сводится к решению системы из двух диф. уравнений: 

![Решение диф. уравнений](/home/aalushin1/report/image/2.png){#fig:002 width=70%}

4) Строим траекторию движения катера первого случая. 

![Код для построения траектории катера](/home/aalushin1/report/image/3.png){#fig:003 width=70%}

![Графическое построение траектории](/home/aalushin1/report/image/10.png){#fig:004 width=70%}

5) Строим траекторию движения для катера и лодки в первом случае. 

![Код для построения пересечения](/home/aalushin1/report/image/4.png){#fig:005 width=70%}

![Графическое пересечение лодки и катера](/home/aalushin1/report/image/11.png){#fig:006 width=70%}

6) С помощью вычислительных мощностей находим точку пересечения катера и лодки. Для этого прописали функцию, которая является решение диф. уравнения. 

![Точка пересечения лодки и катера](/home/aalushin1/report/image/5.png){#fig:007 width=70%}

7) Расчёты и построение траектории для второго случая выполняются аналогично. Поэтому строим траекторию движения катера для второго случая. 

![Код траектории катера во 2 случаи](/home/aalushin1/report/image/6.png){#fig:008 width=70%}

![Графическое построение катера для 2 случая](/home/aalushin1/report/image/12.png){#fig:009 width=70%}

8) Затем построили пересечение катера и лодки для 2 случая. 

![Код траектории пересечения во 2 случаи](/home/aalushin1/report/image/7.png){#fig:010 width=70%}

![Графическое пересечение катера и лодки](/home/aalushin1/report/image/13.png){#fig:011 width=70%}

9) Как и в первом случаи, нашли точку пересечения катера и лодки. 

![Код для нахождения пересечения](/home/aalushin1/report/image/8.png){#fig:012 width=70%}

# Вывод 

Я построил математическую модель решения задачи о погоне катера за браконьерской лодкой. 


