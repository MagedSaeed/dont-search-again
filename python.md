# Installing python from source
when installing a python version from source, most probably, it comes without pip installed. To install this dependencies and fix wierd stuff, run:

```bash
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python3.7 get-pip.py --force-reinstall # in case I installed python3.7 and put it in PATH
pip install -U setuptools
```
This example for an installed version of Python3.7. Please make sure that Python3.7 is in your PATH, i.e. it should return something other than `command not found` when you type `python3.7 -V` in your terminal.

### related links:
- https://stackoverflow.com/a/67886408/4412324

# Python Lists

To remove duplicates from list, you just convert it to set then list again. However, in some cases, order should be perserved. Set operations does not maintain the order. Hence you can use dict keys to maintain it while removing duplicates. This works for Python3.7+. Example:
```python
my_list = [1,1,2]
my_unique_list = list(dict.fromkeys(my_list))
```
A drawback of this solution is that your list items should be hashable. Otherwise, this would not work. If the items of your list are also lists, i.e. your list is a list of lists, a trick might be to convert the lists to tuples then convert back to lists for consistency. This is because tuples are hashable objects. Something like this shuold work:

```python
my_list = [[1],[2],[3],[3]]
my_unique_list = list(map(list,dict.fromkeys(map(tuple,my_list))))
```

### related links:
- https://stackoverflow.com/a/17016257/4412324

## General code snippets

### Extract the domain of a url:

```python
from urllib.parse import urlparse
domain = urlparse('http://www.example.test/foo/bar').netloc
print(domain) # --> www.example.test
```

#### related links:
- https://stackoverflow.com/a/56476496/4412324


# Python requests library

Sometimes, while making a requests via `requests` pachage, the default headers needs to be extended. To find the default headers:

```python
from requests.utils import default_headers
```

# Recursion Depth Management

To show the maximum limit of recursion in Python:

```python
import sys
print(sys.getrecursionlimit())
```

To increase the default recursion depth:

```python
import sys
sys.setrecursionlimit(1500)
```

# Disabling SSL verification

In some cases, you may need to disable ssl globally for experimental purposes:
```python
import ssl

ssl._create_default_https_context = ssl._create_unverified_context
```

