# SOFTWARE ARCHITECTURAL DESIGN SPACE

## Managing Static Structural Representations
- Static Structural play a critical role
- System are developed incrementally
  - increases the need for tight control of this structure in the physical software element
- Managing static structural representations
  - involves dealing with layers of abstraction and levels of refinements

## Software Management Structure
- A large software project
  - is normally designed and implemented by several project teams
- In this structure, each element consists of
  - specific manipulation (design, implementation, debugging, etc)

- At runtime elements are
  - threads
  - processes
  - functional units
  - and data units

- These elements may run on
  - the same computer or
  - multiple computers across a network

- Runtime connectors inherit attributes
  - from their source-code structure counterparts, with a few extra attributes
    - Muilplicity
    - Distance and connection media
    - Universally invokable
    - Seft-descriptive
      > - Liên kết có đặc điểm tự mô tả
      > - Ex: Các service có thể gọi lẫn nhau khi cần

## Tóm lại trong chương này
### Acctualment Design space