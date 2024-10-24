### Layers in Software Architecture

- Layers essentially describes the horizontal functionality.
- A layer consist of 3 areas
  1. Expose User Interface/API
  2. Execute Logic
  3. Retrieve/Save Data


| Layers                    | Detailed Layering                            |
|---------------------------|----------------------------------------------|
| Expose User Interface/API | User Interface (Web)/Service Interface (API) |
| Execute Logic             | Business Logic                               |
| Retrieve/Save Data        | Data Access Layer                            |


#### Purpose of Layers

1. Forces well-formed and focused code.
2. Modular (Building Block)
3. Loose Coupling

### Dependency Injection

- Interfaces has better mechanism for communicating between classes in order to make the code more modular and flexible.
- How to **perform implementation for instances** --> Dependency Injection/Construction Injection (it essentially removes the strong coupling between the classes)