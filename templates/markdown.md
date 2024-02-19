# Markdown template

This file contains useful information to know when writing a Markdown file.  
This document follows Markdown best practices in term of formatting.  

## Table of Contents

A simple way of making your documentation more attractive is to add a table of contents.  
It can be generated automatically by writing `[[_TOC_]]`.

[[_TOC_]]

## Text format

Text can be **bold**, *italic*, or ***bold and italic***. Always use an asterisk `*`.  
You can also insert headings, in order of priority:

- `#` Main document title
- `##` Main section
- `###` Sub-section
- `####` Specific point
- `#####` More specific point
- `######` Most specific point

## Code insertions

Use backticks to insert a block of code:

```python
  # Don't forget to specify the language when you insert code in a markdown file:
  print("This is a colored line.")
```

Or to mention other technical informations: `path/to/file.csv`.

## Quote

Blockquotes are used to add notes to a paragraph.

>This is a quote.
>>This is a nested blockquote.

## Lists

Unordered list:

- Banana
- Apple
- Pear

Ordered list:

1. Strawberry
2. Grape
3. Blueberry

To Do list:

- [x] Task 1
- [x] Task 2
- [ ] Task 3

## Links

Links can be inserted [as follows](www.google.com "Direct link to Google.com"): `click [here](www.site.com "Don't forget the placeholder!")`.

You can also insert [mailto links](mailto:user@outlook.com "Mail to user"), to create a shortcut to an e-mail application (e.g. Outlook): `contact [Mr Doe](mailto:johndoe@outlook.com "Mail to Mr Doe")`.

## Contributing

It's important to maintain a consistency within the project when you contribute to it.  
This is why the Commits and Branches naming conventions have been created.

### Commits

All commits must follow the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) syntax.  

|  **Type** |           **Description**           |
|:---------:|:-----------------------------------:|
|   feat:   | Implement new application features. |
|    fix:   |       Correct code, fix bugs.       |
| refactor: |  Optimize existing code structure.  |
|   docs:   |        Update documentation.        |
|   style:  |         Improve code format.        |
|   perf:   |         Enhance performance.        |
|   test:   |         Add or update tests.        |

Example commit message: `docs: update Commits section`

### Branches

All branches must follow the [Git Branch Naming Convention](https://dev.to/couchcamote/git-branching-name-convention-cch).

#### Code Flow branches

| **Name** |       **Description**       |
|:--------:|:---------------------------:|
|  master  |    Main stable codebase.    |
|    dev   |   Active development work.  |
|   test   |  Testing new code changes.  |
|  staging | Pre-production environment. |

Example branch name: `dev`

#### Temporary branches

|   **Name**   |       **Description**       |
|:------------:|:---------------------------:|
|    feature   |   New feature development.  |
|    bugfix    |   Regular bug corrections.  |
|    hotfix    |      Urgent bug fixes.      |
| experimental |    Testing new concepts.    |
|     build    |      Compilation tasks.     |
|    release   | Stable version preparation. |
|    merging   |   Branch integration work.  |

Example branch name: `feature/new-feature`

## Files Structure

Displaying the file structure in the documentation is a good way of ensuring project transparency.  
Use [nathanfriend.io](https://tree.nathanfriend.io/, "ASCII Tree") to generate file structures:

```bash
.
├── project/
│   ├── src/
│   │   ├── module1.py # You can also add comments
│   │   └── module2.py
│   └── tests/
│       ├── test1.py
│       └── test2.py
└── README.md
```

## Tables

Tables are very useful for highlighting important information.  
Use [tablesgenerator.com](https://www.tablesgenerator.com/markdown_tables#) to generate Markdown tables:

|  **Software**  | **Version** |
|:--------------:|:-----------:|
|     Python     |     3.8     |
|     Ansible    |     2.9     |
|     Docker     |   24.0.9    |

## Placeholders

Placeholders can be used to insert images stored online. I mainly use it to insert colors.   
Use [place-hold.it](https://place-hold.it/) to insert hexadecimal color codes:

- ![008000](https://place-hold.it/10/008000/008000 "Green") This is a 10 pixels green square.
- ![FFA500](https://place-hold.it/15/FFA500/FFA500 "Orange") This is a 15 pixels orange square.
- ![FF0000](https://place-hold.it/20/FF0000/FF0000 "Red") This is a 20 pixels red square.

## Reflinks

If the link you cant to add is so long that it makes the Markdown code difficult to read, you can use [reflinks][like this].

[like this]: www.google.com/ThisIsAnUsefulFeature/EspeciallyWhenTheLinkIs4LinesLong/ThisLinkIsVeryLongIsntIt/? "Placeholder can also be inserted in reflinks !"

## Graphs

Displaying a graph can be used for many purposes (explaining algorithmic logic, visualising a process flow, creating a diagram, etc.).  
The syntax may seem a little complex at first, but once you understand it, the tool comes in very handy:  

```mermaid
graph TD; %% Defines the graph orientation (Top Down)
  A[Start Here] --> B{Is it clear?}; %% A node with text leading to a decision node
  B -- Yes --> C[End]; %% Option Yes from decision node to end
  B -- No --> D[Try Again]; %% Option No leading to another step
  D --> B; %% Loop back to the decision node
```
