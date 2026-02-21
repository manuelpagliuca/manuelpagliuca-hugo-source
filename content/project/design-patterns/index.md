---
title: Design Patterns in C++
summary: Personal project
tags:
  - Software Engineering
  - Programming
date: "2023-12-26T14:17:20Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption:
  focal_point: Smart

links:

url_code: "https://github.com/manuelpagliuca/design-patterns-cpp"
# url_pdf: "uploads/MANUEL_PAGLIUCA_ANISOTROPIC_MM_Master_s_Thesis__Integral_.pdf"
url_slides: ""
url_video: ""
# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.

#slides: example
---
Personal project, December 2023

Between November and December, I wanted to dive deeper into software engineering, so I decided to study and implement some design patterns. In particular the fundamental ones from the *Gang of Four* (GoF).

I created a [repository](https://github.com/manuelpagliuca/design-patterns-cpp) that serves as a collection of C++ implementations of these patterns. All the GoF patterns are present, but in the future I plan to add the "extra" patterns as well (currently only the *null object* is included).

## Creational
| Design Pattern          | Description                                                                                     |
|-------------------------|-------------------------------------------------------------------------------------------------|
| Abstract Factory        | Provides an interface for creating families of related or dependent objects without specifying their concrete classes. |
| Builder                 | Separates the construction of a complex object from its representation, allowing the same construction process to create different representations. |
| Factory Method          | Defines an interface for creating an object but leaves the choice of its type to the subclasses. |
| Prototype               | Creates new objects by copying an existing object, known as the prototype.                       |
| Singleton               | Ensures a class has only one instance and provides a global point of access to that instance.    |

## Structural
| Design Pattern          | Description                                                                                     |
|-------------------------|-------------------------------------------------------------------------------------------------|
| Adapter                 | Allows classes with incompatible interfaces to work together by wrapping its own interface around that of an already existing class.|
| Bridge                  | Decouples an abstraction from its implementation so that the two can vary independently.         |
| Composite               | Composes zero-or-more similar objects so that they can be manipulated as one object.              |
| Decorator               | Dynamically adds/overrides behavior in an existing method of an object.                           |
| Facade                  | Provides a simplified interface to a large body of code.                                          |
| Flyweight               | Reduces the cost of creating and manipulating a large number of similar objects.                  |
| Proxy                   | Provides a placeholder for another object to control access, reduce cost, and reduce complexity.  |

## Behavioral
| Design Pattern             | Description                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------|
| Chain of Responsibility    | Delegates commands to a chain of processing objects.                                             |
| Command                    | Creates objects that encapsulate actions and parameters.                                         |
| Interpreter                | Implements a specialized language.                                                               |
| Iterator                   | Accesses the elements of an object sequentially without exposing its underlying representation. |
| Mediator                   | Allows loose coupling between classes by being the only class that has detailed knowledge of their methods. |
| Memento                    | Provides the ability to restore an object to its previous state (undo).                           |
| Observer                   | Is a publish/subscribe pattern, which allows some observer objects to see an event.        |
| State                      | Allows an object to alter its behavior when its internal state changes.                            |
| Strategy                   | Allows one of a family of algorithms to be selected on-the-fly at runtime.                          |
| Template Method            | Defines the skeleton of an algorithm as an abstract class, allowing its subclasses to provide concrete behavior. |
| Visitor                    | Separates an algorithm from an object structure by moving the hierarchy of methods into one object.|

During this exploration, I discovered many interesting aspects of software engineering, especially the concept of scope-level design patterns. Some design patterns can be applied directly to the codebase (code level, or micro), such as the GoF patterns or *concurrency patterns* for multi-threaded paradigms.

Other design patterns act on a higher level of abstraction, and these are called **architectural patterns**. Some of them are widely known, such as MVC (Model-View-Controller) or n-tier architecture, but most are new to me.

In the future, I would like to write a blog post about them with diagrams and explanations. It seems like a good idea for studying them in a fun way 😁
