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


############# a combined book list for three Spanish, German, English

book = []
d =['cherbonnel-mi-tio_SP.txt','schloemp-tolle-koffer_DE.txt','eaton-boy-scouts_EN.txt']
for fname in d:
    with open('C:\\Users\\Yonas\\'+ fname, encoding='utf-8') as f:
        book.append(f.read())
print(book[0])


# split the string into words (use str.split).


store = str(book[0]).split()
print(store)
    

#remove punctuation and other special characters from the words. You can do something like
###word.strip('|©!@#$%^&*()-_=+,.;:?/<>'`[]')

data = [word.strip('|©!@#$%^&*()-_=+,.;:?/<>\'\`[]') for word in store]
print(data)



############### ) most frequent words in the Spanish, German, English text

data = str(book[0]).split()

vocublary = (str(book[0]).split())
print(vocublary)


count = {}
for word in vocublary:
     count[word] = 0 
for word in vocublary:
     count[word] = 1
for word in vocublary:
     count[word] = 2
for word in vocublary:
     count[word] = 3
print(count)

len(vocublary)

count = {}
for word in count.keys():
     count[word] = count[word]/len(vocublary)
print(count)


############# Out of the word frequency table, only retain a small number (say 10) of the most common
##words. There are several ways to pull out the largest counts. I recommend to follow this
##example:


pairlist = sorted(count.items(), key=lambda kv: kv[1], reverse=True)
print(pairlist)

mostFrequent = dict(pairlist[:10]) 
print(mostFrequent) 

print(mostFrequent.get("Project"))


##############   most frequent words in the unknown text.
ubook = []
u =['unknown-lang.txt']
for fname in u:
    with open('C:\\Users\\Yonas\\'+ fname, encoding='utf-8') as f:
        ubook.append(f.read())
print(ubook[0])


udata = str(ubook[0]).split()

uvocublary = (str(ubook[0]).split())
print(uvocublary)


ucount = {}
for word in uvocublary:
     ucount[word] = 0 
for word in vocublary:
     ucount[word] = 1
for word in vocublary:
     ucount[word] = 2
for word in vocublary:
     ucount[word] = 3
print(ucount)

len(uvocublary)

ucount = {}
for word in ucount.keys():
     ucount[word] = ucount[word]/len(uvocublary)
print(ucount)

ucount = {}
for word in ucount.keys():
     ucount[word] = ucount[word]/len(uvocublary)
print(ucount)


upairlist = sorted(ucount.items(), key=lambda kv: kv[1], reverse=True)
print(upairlist)

umostFrequent = dict(upairlist[:10]) 
print(umostFrequent) 



print(umostFrequent.get(""))

#########
######    Result

##  the unkown word has less frequency which is zero (umostFrequent  {})
##   print(umostFrequent.get(""))  &  print(mostFrequent.get("Project"))