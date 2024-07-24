Anchors (&) mark key-value pairs with a unique name.
Aliases (*) reference that same value elsewhere in the document.

**Define a YAML anchor for default person properties**
```
person_defaults: &person_defaults
  name: Default Name
  age: 25
```

**Define person1 using the anchor &person_defaults and override 'name' and add 'employed'**
```
person1:
  <<: *person_defaults  # This merges all keys from &person_defaults
  name: Alice           # Override 'name' from &person_defaults
  employed: true
```

**Define person2 using the same anchor &person_defaults and override 'name' and add 'employed'**
```
person2:
  <<: *person_defaults  # This merges all keys from &person_defaults
  name: Bob             # Override 'name' from &person_defaults
  employed: false
```

**Multi-line strings are represented using the '|' symbol, which preserves newlines.**
```
description: |
  This is a long description
  that spans multiple lines.
  It will be preserved as-is.
```
**Example demonstrating YAML Anchors and Aliases**
**Define a common structure for a person**
```
person_defaults: &person_defaults
  name: John Doe
  age: 30
  occupation: Developer
```
**Define specific persons using the above structure**
```
person1:
  <<: *person_defaults
  name: Alice
  age: 28
  occupation: Designer

person2:
  <<: *person_defaults
  name: Bob
  age: 32
  occupation: Manager
```

**Example demonstrating Multi-line Strings in YAML**
**Define a multi-line description for a product**
```
product:
  name: Example Product
  description: |
    This product is designed to showcase YAML features.
    It supports:
    - Anchors and Aliases for reusable data.
    - Multi-line strings for preserving formatting.
    Enjoy exploring YAML with this example!
```
**YAML Anchors and Aliases**
person_defaults is defined with &person_defaults, marking it as an anchor.
person1 and person2 use <<: *person_defaults to inherit name, age, and occupation from person_defaults. 
They override name, age, and occupation with specific values.

**Multi-line Strings**
product.description is defined with | to preserve newlines and formatting.
The description spans multiple lines, making it easier to maintain and read.
