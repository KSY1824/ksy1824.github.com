---
layout: post
title: XY location code
date: 2021-04-04
excerpt: "I used tuple."
tags: [XY, code, tuple]
comments: true
---

### code

~~~

class point:
    def __init__(self, xy):
        self.xy = xy

    def set(self, xy):
        self.xy = xy

    def get(self):
        return(self.xy)

    def move(self, xy1):
        self.xy = (self.xy[0] + xy1[0], self.xy[1] + xy1[1])

A = point((8,9))
print(A.get())
A.set((1,2))
print(A.get())
A.move((9,8))
print(A.get())

~~~
