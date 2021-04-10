---
layout: post
title: Hiragana random printer
date: 2021-04-08
excerpt: "I hate Japan ㅡㅡ"
tags: [random, code, tuple]
comments: true
---

#### I made it for Hiragana - Japanese exam.

### code

~~~

import random

A = ['a', 'i', 'u', 'e', 'o', 'ka', 'ki', 'ku', 'ke', 'ko']
a = '0'

while a == '0':
    if len(A) == 0:
        break

    b = random.randint(0, len(A) - 1)

    print('The sound of hiragana letter that were picked : ' + A[b])
    del A[b]
    a = input('Continue? > ')
    print('-' * 50)

    if a == '0':
        continue
    else:
        break
~~~

### How to use
#### - press 0 to continue / press any key (Excluding 0) to end.
#### - You can change Contents of A to get other Hiragana's sound.
