DICTIONARIES 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ 

A dictionary is an object that holds from 0 to many {key, value} pairs. 

We say that it 'maps' keys to values. 
You put in a key and get a value back. 

Key Value 

'ID002' -> 'John Smith' 
'ID000' -> 'Test Student' 
'ID021' -> 'Arnold Finkler' 

The syntax for dictionary lookups is similar to that of a single index lookup in a list. 

With lists you can access the items by index: squares[4]. 
With dictionaries you access the items by key: students['ID002']. 

RULES REGARDING DICTIONARY KEYS 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ 

You can't use slice syntax with a dictionaries because objects aren't located by position. In fact, they are added to a dictionary in an arbitrary order, so you should never depend on Python's built in DICT for order. 

What can a key be, you might ask? 
A key can be any immutable type, which means that it has to be a type that can't change. Without getting into the details of how a dictionary works (if you're interested, look up 'hash function'). 

A dictionary key can be an integer, a string, a boolean value (which just means it can be True or False). 
Thus, a dictionary key CANT be a list, another dictionary, a set. 
A dictionary can have dictionaries or mutable data types as its VALUES (this is quite useful). 
Can you take a guess at why the keys can't be immutable? 


WORKING WITH DICTIONARIES 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ 

We create an empty dictionary like this: 

d = {} 
or 
d = dict() 

or even 

l = [ ['a',1],['b',2],['c',3] ] 
d = dict(l) 


We add a new {key, value} pair to it like this: 

d['bicycle'] = 'a human-powered, pedal-driven, single-track vehicle, having two wheels attached to a frame, one behind the other. A bicycle rider is called a cyclist, or bicyclist.' 

As I tacitly implied above, we can also turn any sequence of pairs into a dictionary: 

l = [ ['a',1],['b',2] ] 
d = dict(l) 
print d 
{'a': 1, 'b': 2} 

note that this won't work: 

l = ['a',1] 
d = dict(l) 
TypeError: cannot convert dictionary update sequence element #0 to a sequence 

why? Because l is not a sequence of pairs. It's a sequence of individual items. 

THE IMPORTANCE OF DICTIONARIES 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ 

The inner workings of dictionaries are somewhat complex but they reflect a concerted effort to make lookups very fast. 

They also take a lot of the mental load off the programmer. 

If you recall, with a list you need to remember the position that something is in. 

Imagine parsing breaking a text file up into sentences and then words in order to do some processing to it. 

It is doable with lists, but it may make you think much more than necessary because you will have to remember which numbers correspond to which objects you've created by splitting the text up. 

With dictionaries, you can assign these objects meaningful names like textFile['lines'] = [l for l in f.split('.')]. You can use things with meaning to you to identify the location of important data. 
