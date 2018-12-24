# Auto-Activative-Code

import string
import random
import os

BaseCode = string.digits + string.ascii_letters

def get_key(n):
    key = ''
    for i in range(1,n+1):
        key += random.choice(BaseCode)
        if i % 4 ==0 and i != n:
            key += '-'
    return key
