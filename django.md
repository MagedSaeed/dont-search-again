# Django Template

This list below contains fast shortcuts for the commands frequently used in django templates.

- capitalize string:
  `'string1'|title`

- convert to uppercase:
  `'string1'|upper`

- convert to lowercase:
  `'string1'|lower`

- concatenate strings:
  `'string1'|add:'string2'`
  - variables already defined in the get_context_data can be added as well
    `'string1'|add:myvar|add:'just another string'`
  - even some operations can be applied on these variables.
    `'string1'|add:myvar|title|add:'just another string'`
- line breaks, replacing newlines (\n) by `<br>`:
    `'string1'|linebreaksbr`
 
# Creating super user

Creating superuser can happen in various ways. The easist way is to run `python manage.py createsuperuser` in shell. For a more advanced method, it can be embedded in shell as follows:
```python
from django.contrib.auth import get_user_model
from getpass import getpass

User = get_user_model()

new_user = User(username='username')
new_user.set_password(getpass())
new_user.is_superuser = True
new_user.is_staff = True
new_user.save()

```
Note the use of `getpass` module to cover the password in shell. Also, `set_pass` method sets a hashable password unlike settinging in the User initializer where the password wont be hashed.
