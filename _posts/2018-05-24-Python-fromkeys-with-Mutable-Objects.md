---
layout: post
title: Python Problem Using dict.fromkeys() to Create a Dictionary
---
I had this bug somewhere in the code and I couldn't figure out where it was. After isolating some code I came across this behavior that I didn't expect.

    my_list = ['dic1', 'dic2']
    my_dic = dict.fromkeys(mylist, {})
    >>> my_dic
    {'dic1': {}, 'dic2': {}}
    my_dic['dic1']['entry1'] = 1
    >>> my_dic
    {'dic1': {'entry1': 1}, 'dic2': {'entry1': 1}}

It turns out that if the default value is a dictionary then each entry in the newly created dictionary will have a reference to that dictionary. This happens for every mutable object we put as default argument. Simply put, change one entry in the base dictionary and all nested dictionaries will update. It seems like a lot of people went into this trap judging from the numerous [StackOverflow Questions](https://stackoverflow.com/questions/15516413/dict-fromkeys-all-point-to-same-list)


We can fix this by writing,

    my_list = ['dic1', 'dic2']
    new_dic = dict((key,{}) for key in my_list)
    new_dic
    >>> {'dic1': {}, 'dic2': {}}
    new_dic['dic1']['entry1'] = 1
    >>> new_dic
    {'dic1': {'entry1': 1}, 'dic2': {}}
