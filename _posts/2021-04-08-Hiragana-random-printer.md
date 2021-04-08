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

A = ('a', 'i', 'u', 'e', 'o')
a = '0'

while a == '0':
    b = random.randint(0, len(A) - 1)
    print('The sound of hiragana letter that were picked : ' + A[b])
    a = input('Continue? > ')
    print('-' * 50)

    if a == '0':
        continue
    else:
        break
        
~~~

### How to use
#### - press 0 to continue.
#### - You can change Contents of A to get other Hiragana's sound.
