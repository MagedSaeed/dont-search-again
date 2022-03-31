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
 
  
