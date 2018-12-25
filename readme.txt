#Auto Activation Code

import string
import random
import os

BaseCode = string.digits + string.ascii_letters


def get_key(n):
    key = ''

    for i in range(1, n + 1):
        temp_key = random.choice(BaseCode)
        key += temp_key
        if i % 4 == 0 and i != n:
            key += '-'
    return key


def get_all_keys():
    temp = []
    for i in range(m):
        one_key = get_key(n)
        if one_key not in temp:
            temp.append(one_key)

    try:
        os.remove('D:/Auto Activation Code.txt')
    except:
        os.truncate('D:/Auto Activation Code.txt', length=0)

    for key in temp:
        with open('D:/Auto Activation Code.txt', 'a+') as f:
            f.write(key + '\n')


n = int(input('length your code: '))
m = int(input('number you want get code: '))
get_all_keys()

#########################################
with open('D:/Auto Activation Code.txt') as f:
    data = f.read()
f.close()

code = []
for i in data.split('\n'):
    if len(i) > 0:
        print(i, end = ';')