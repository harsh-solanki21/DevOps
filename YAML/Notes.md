# YAML Notes

## Introduction

- YAML (YAML Ain't Markup Language) is a data serialization language often used for configuration files.
- It's similar to XML and JSON but designed for data, not documents.
- Key features:
  - Case-sensitive
  - Requires proper indentation (use spaces, not tabs)
  - File extensions: .yaml or .yml
  - Data stored in key-value pairs

## Key Concepts

- Data is stored in key-value pairs.
- `---` denotes the start of a new document.
- `...` indicates the end of a document.
- Add data in key-value pairs.

<br />

## Data Types

### Simple Data Types

**YAML automatically detects Datatype if not specified**

```yml

# Strings
name: Harsh Solanki
description: "Software Engineer"
multiline: |
  This is a
  multiline string
folded: >
  This will be
  in one line

# Numbers
integer: 42
float: 3.14
scientific: 6.023E23

# Boolean
boolean: true

# Specifying Types
zero: !!int 0
positiveNum: !!int 45
negativeNum: !!int -45
binaryNum: !!int 0b11001
octalNum: !!int 06574
hexa: !!int 0x45
commaValues: !!int +540_000  # 540,000
exponential numbers: 6.023E56

marks: !!float 56.63
infinite: !!float .inf
not a num: .nan
boolean: !!bool false
string: !!str the string value

# Null
empty: null
~: this is a null key

# Date & Time
date: !!timestamp 2002-12-14
india time: 2001-12-15T02:59:43.10 +5:30
no time zone: 2001-12-15T02:59:43.10
```

<br />

### Advanced Data Types

```yml
# List (Sequences)
student: !!seq
 - name
 - roll_no
 - marks

# Alternative syntax
student: [name, roll_no, marks]

# Sparse sequence
sparse seq:
 - hey
 - how
 -
 - null
 - good

# Nested sequence
-
 - mango
 - apple
 - banana
-
 - marks
 - roll_no
 - date


# Maps (Dictionaries)
!!map

# Nested mappings
name: Harsh Solanki
role:
 age: 22
 job: student

# Alternative syntax
name: Harsh Solanki
role: { age: 22, job: student }


# Ordered Maps
People: !!omap
 - Harsh:
    name: Harsh Solanki
    age: 22
    height: 180
 - Kunal:
    name: Kunal Kushwaha
    age: 22
    height: 190


# Pairs
pair example: !!pairs
 - job: student
 - job: teacher

# Alternative syntax
pair example: !!pairs [job: student, job: teacher]


# Sets
names: !!set
 ? Harsh
 ? Kunal
 ? Nisarg


# Nested Structures
employees:
  - name: Alice
    role:
      title: Manager
      department: Sales
  - name: Kunal
    role:
      title: Developer
      department: IT


# Anchors and Aliases
defaults: &defaults
  OS: Linux
  version: 2.2.1

machine1:
  <<: *defaults
  name: test-server

machine2:
  <<: *defaults
  name: prod-server
```

<br />

## Best Practices

1. Use consistent indentation
2. Prefer block style for readability
3. Use quotes for strings with special characters
4. Leverage YAML's data types for accurate representation
5. Use comments to explain complex structures
