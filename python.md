# Installing python from source
when installing a python version from source, most probably, it comes without pip installed. To install this dependencies and fix wierd stuff, run:

```bash
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python3.7 get-pip.py --force-reinstall # in case I installed python3.7 and put it in PATH
pip install -U setuptools
```
### related links:
- https://stackoverflow.com/a/67886408/4412324

# Python Lists

remove duplicates from list perserving the list order, use dict keys. This is for Python3.7+
```python
list = [1,1,2]
unique_list = list(dict.fromkeys(list))
```
A drawback of this solution is that your list items should be hashable. Otherwise, this would not work.

### related links:
- https://stackoverflow.com/a/17016257/4412324
