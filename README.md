# talkfilters
A simple Python wrapper around GNU Talkfilters.

Requires the talkfilters binaries (also available in this repo, convenience!) to be compiled and available in PATH somewhere.

## Example Usage
```sh
kaiz0r@playground:~/Playground/Python$ python3
Python 3.8.1 (default, Feb  5 2020, 12:40:00) 
[GCC 8.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import tf
>>> tf.send("pirate", "how are you doing today?!")
"how be ye doing t'day?!"
>>> tf.send("warez", "how are you doing today?")
'h0\\/\\/ r j00 d0YNg t0|)4y?'
>>> f = tf.send("drawl", "how are you doing today?")
>>> print(f)
hyeru doin' tuhday?
>>> tf.send("etc", "this filter doesnt exist")
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "/home/kaiz0r/Playground/Python/tf.py", line 40, in send
    raise ValueError(f"Talkfilter {filter_name} not found.")
ValueError: Talkfilter etc not found.
>>> 
```
Also available is:
print_filters() which prints a table of the filters and a description

filter_info() returns the same as print_filters as a string

list_filters() returns a list object containing the names of all available filter binaries
