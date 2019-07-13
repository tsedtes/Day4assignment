# Day4assignment

# -*- coding: utf-8 -*-
"""
Created on Fri Jul 12 22:46:27 2019

@author: Yonas
"""

import os

d = os.getcwd()
print(d)


##########  Spanish

with open('C:\\Users\\Yonas\\cherbonnel-mi-tio_SP.txt', encoding='utf-8') as f:
   content = f.read()
print(content)

########### German

with open('C:\\Users\\Yonas\\schloemp-tolle-koffer_DE.txt', encoding='utf-8') as f:
   content = f.read()
print(content)



############ English
with open('C:\\Users\\Yonas\\eaton-boy-scouts_EN.txt', encoding='utf-8') as f:
   content = f.read()
print(content)


############ Unknown

with open('C:\\Users\\Yonas\\unknown-lang.txt', encoding='utf-8') as f:
   content = f.read()
print(content)

##################

book = []
d =['cherbonnel-mi-tio_SP.txt','schloemp-tolle-koffer_DE.txt','eaton-boy-scouts_EN.txt','unknown-lang.txt']
for fname in d:
    with open('C:\\Users\\Yonas\\'+ fname, encoding='utf-8') as f:
        book.append(f.read())
print(book[0])

# split the string into words (use str.split).

store = str(book[0]).split()
print(store)
    
data = [word.strip('|©!@#$%^&*()-_=+,.;:?/<>\'\`[]') for word in store]
print(data)

############### ) create a word frequency table (we did it in PS02). 

data = str(book[0]).split()

vocublary = (str(book[0]).split())
print(vocublary)

counts = {}
for word in vocublary:
     counts[word] = 0
for word in vocublary:
     counts[word] += 1
print(counts)