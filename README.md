# indy.cody- Oct. 19th, 2022
Notes from 2022 Indy.Code()

# Typescript (By Eric Potter from Sweetwater)

## IntersectionTypes

    Programmer = boolean & string

## Union Types

    type Person = Programmer | Tester

    Common Use Case:
        - Dealing with Errors

## String Literals

    export type Grade = "A" | "B" | "C"

## Template Literals

    type GradeModifiers = "+" | "" | "-"
    export type expandedGrades = `${Grade}${GradeModifiers}`

## Utility Types

    - Allows me to modified other types

## Indexed Access Types

    - Handy for staying in sink with a changing dataset

## General

    - A lot of things you can do but shouldn't
    - Code: https://github.com/pottereric/Typescriptbeyondthebasics
    - Eric: https://humbletoolsmith.com/



# Building Event-Driven  Microservices (by Chad Green)

    EDA = event-driven architecture

## When do I use this

    - Multiple subsystems
    - Real-time Processing
    - Complex Event Processing
    - High Volumne/Veloity Data

## Denefits

    - Decoupling
    - Encapsulation
    - Responsive
    - Scalable/Distributed
    - Independence

## Drawbacks

    - Steep learning curve
    - Complexity

## Limitations

    - Guaranteed Delivery (if you one of your subscribers goes down you aren't going to receive it)
    - Sequencing

## Implementation Options

    - Azure Event Hubs
        1] works well with Kafka
        2] Partitions
        3] Throughput units
    - Azure Service Bus

# Funtional-Flavored Javascript (by Dave Fancher)
​
## Tenets of Func. Prgoramming

    1) Purity/Controlling side-effects
    2) Favor expressions over statements
    3) Functions as Data

## Immutability
    - Immutable.js
    - Object.freeze()
    - Defineproperty
    - Arrow functions
        - Functions as data

## Built in Functions
    - learn about reduce
    - Currying
    PFA - Partial Function Addition

## Composability

    - 

## ES6 symbols
    - Contact free extension point

## Extending Object / Model-Based Validation

    - 

# Knowing Your Limitations: The Key to improving your softwared design devisions (by Eric Potter)

## Humility != Self Description

Edimology of Humility - grounded (*)

List of Cognitive biases: https://en.wikipedia.org/wiki/List_of_cognitive_biases

## Admitting the possibility of error leads to:
    - Better testing
    - Better code reviews
    - Asking for help appropriately
    - better naming and documentation

## Admitting that others may know mores leads to:

    - Use of better solutions
    - Use of better methods
    - Use of better architectures

## Admitting that we need to learn leads to:

    - Lifelong learning
    - Asking better questions

## Self-accurate Thinking:

    - Dunning-Kruger Effect
    - Book: The Programmer's Brain by Felienne Hermans
        - (Book Link)[https://www.amazon.com/Programmers-Brain-every-programmer-cognition/dp/1617298670/ref=sr_1_1?crid=2E5SPCV7EITPW&keywords=the+programmers+brain&qid=1666197734&qu=eyJxc2MiOiIxLjg3IiwicXNhIjoiMS43NCIsInFzcCI6IjEuODUifQ%3D%3D&sprefix=the+programmers%2Caps%2C159&sr=8-1]
    - The Magic Number Seven, Plus or Minues Two ( by George A Miller)
        - Thinnk about this as far as refactoring and chunking into smaller chunks... aka reorganizing into smaller units
    - The Checklist Manifesto by Atul Gawande
        - https://www.amazon.com/Checklist-Manifesto-How-Things-Right-ebook/dp/B0030V0PEW/ref=sr_1_1?crid=290RQRELQNGAM&keywords=the+checklist+manifesto&qid=1666197957&qu=eyJxc2MiOiIxLjgyIiwicXNhIjoiMS4zMyIsInFzcCI6IjEuNDEifQ%3D%3D&sprefix=The+Checklist+%2Caps%2C186&sr=8-1
    - Humility is the New Smart by Edward D Hess & Katherine Ludwig
    - Be in the the rethinking cycle versus the overconfident cycle
    - "Humility is not thinking less of yoruself, but thinking of yourself less"
## **Humility is OTHERS oriented

## Focus of helping:
    - Teammates
    - Users

## GOAL of software development:

    - 

## As software developers, we build tools:

    Help our users:
    - Work faster
    - Know more

# Javascript Metaprogramming (by Dave Francher)

## What is metaprogramming?
    - Programming about programming/code about code
    - 3 Categories:
        1) Code generatin
        2) Reflection
        3) Intercession

    - Consider lodash for type detection

## Simple (Classic) Reflection

```
    const myObject = {
        firstName: "Austin",
        lastName: "Bearden"
    }

    Reflect.has(myObject, "age"); // false

    Reflect.defineProperty(
        myObject,
        "age",
        {
            configurable: true,
            enumerable: true,
            writable: true,
            value: 42
        }
    ); // true
```

    - Reflect will return whether or not the defineProperty was successful for onot
    - Object will return the object

## Symbols - Collision-Free Extension Points
- Kinda like an OOO Interface
- Guaranteed conflict free

    Defining symbols
    ```
    // no label
    const greet = Symbol("greet")

    ```
## Intercession

# Ship Accessability by Dale Sande from Alaska Airlines

**To-do: interact with a website with black screen and only use screen reader as a blind person**

**To-do: watch a video or sit in session where a blind person is using screen reader on website**

Tools:

1) blind
2) only keyboard interaction
3) Color blindness

Section 508:
    
**Anyone who touches frontend code is responsible to make accessable**

    Companies to solve Accessability:

        - Level access

- Web AIM - group of people who are accessability advocites

## Evaluate the invisible spec

## ARIA <-- learn more about it

## HTML Custom Elements

LIT - Google library: https://lit.dev/

Template literals

Tagged template literals

-- Look up the html `<slot></slot>` element

# Securing a WebAPI with JWT Token Role-Based Authentication by Victor Pudelski

## JWT Structures

    1) Header - 
    2) Payload - The Claims of information of the JSON obbject
    3) Signature - A cryptographic signature to validate the integrity of the payload

## Storing on local or session

    - session is only stored on one tab
    - local is across tabs
        - If multiple tabs required do local storage
        - Either way use refresh tokens so JWt isn't just sitting there exposed
        - If we are not logged in, don't store it in session storage

    (consider this for PMI authentication implementation)

# General Notes

## mocks and unit test by Duane Newman (didn't attend)
https://autofixture.github.io/#

## For presentations
https://revealjs.com/


