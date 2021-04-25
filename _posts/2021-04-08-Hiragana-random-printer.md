---
layout: post
title: Hiragana random printer
date: 2021-04-08
excerpt: "I hate Japan ㅡㅡ"
tags: [random, code, list, HW]
comments: true
---

#### I made it for Hiragana - Japanese exam.

### code

~~~

import random

A = ['ta', 'ti', 'tu', 'te', 'to']
a = '0'

while a == '0':

    print(('-' * 50))
    b = random.randint(0, len(A) - 1)

    print('The sound of hiragana letter that were picked : ' + A[b])
    del A[b]

    if len(A) < 1:
        print('Finish!' + '\n' + ('-' * 50))
        break
    else:
        a = input('Continue? > ')

    if a == '0':
        continue
    else:
        print('-' * 50)
        break
    
~~~

### How to use
#### - press 0 and enter key to continue / press any key (Exclude 0) and enter key to end.
#### - You can change Contents of A to get other Hiragana's sound.
