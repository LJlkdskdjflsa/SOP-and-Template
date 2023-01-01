# SOP Template

# Guideline
When you have a goal to research a project
don't wast your time read the whole project
just understand the minimal part that can reach your goal
- if you just need to do a little, you don't need to understand all
- when you have free time, you can deep dive as you wish

it is a process that
the more you understant the project, the smaller action you need to take to reach your goal

so keep asking you what you need to do to reach your goal, if you have a clear thought, than you don't need to keep deep dive

- it's better to read the minimal file/code to understand the part of the project you need to fix/change
- if you think project is to complex/complicate just draw a diagram
    - EX. need to understand code interact with what
        - draw a sequence diagram
- also you can imagine how it implenment than go to code to check if it metch your imagine or not

every step you need to smaller the zone you need to search the next

```plantuml
start

repeat :;
    :Understand the Business Logic of the Project;
    :Docs/Diagram that helps you understand quicker;
    :File structure;
    :Implementation;
backward:specified a more small zone to dive;
repeat while (can I figure it out what to do, or still need more info to structure wht to do?)
:hands on;
stop
```

# SOP

- Understand the Business Logic of the Project
- Docs/Diagram that helps you understand quicker
- File structure
- Implementation


# Template

## TODO
- [ ] Non Code (Goal: Understand What is the project for)
    - [ ] API docs
        - [ ] use postman to try
            - [ ] fork postman collection
            - [ ] test all apis
        - [ ] ...
    - [ ] ER diagram(DB)
        - [ ] ...
        - [ ] ...
- [ ] Code (Goal: Understand How the projects implement those function)
    - [ ] file structure
    - [ ] trace code(on feature demands)

## Non Code
### API docs
### ER diagram(DB)

## Code (Goal: Understand How the projects implement those function)
### file structure
### trace code(on feature demands)
 

## Other Info
## Meta
#
###### tags: `SOP` `Template`