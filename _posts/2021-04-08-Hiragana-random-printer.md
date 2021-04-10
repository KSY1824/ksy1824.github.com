---
layout: post
title: Hiragana random printer
date: 2021-04-08
excerpt: "I hate Japan ㅡㅡ"
tags: [random, code, list]
comments: true
---

#### I made it for Hiragana - Japanese exam.

### code

~~~

import random

A = ['a', 'i', 'u', 'e', 'o']
a = '0'

while a == '0':
    if len(A) == 0:
        break

    b = random.randint(0, len(A) - 1)

    print('The sound of hiragana letter that were picked : ' + A[b])
    del A[b]
    a = input('Continue? > ')

    if a == '0':
        print('-' * 50)
        continue
    else:
        break
    
~~~

### How to use
#### - press 0 and enter key to continue / press any key (Exclude 0) to end.
#### - You can change Contents of A to get other Hiragana's sound.
