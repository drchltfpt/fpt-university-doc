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

## Acctualment Design space

## Guidlines for Mapping Runtime Elements
### Cách tổ chức của các thành phần phần mềm
> If an element is __reentrant__, it can be implemented by a thread or a process

> If an element is __not reentrant__ and __multiple threads__ or processes may need to communicate with it  
=> It must be run on separate threads or processes so they can be thread-safe

> If an element has __high multiplicity__ and its __performance is important__ to the global system performance  
=> An application server should be used for its implementation

#### Các thành phần quan trọng cần được phục vụ riêng với performance cao hơn

> If there are __heavy computations__ in the elements for deployment at a particular location __a cluster of processors__ should be considered for added CPU data processing power

> If an element is assigned __complex__ but well-defined functions similar to those of some commercial off-the-shelf software components and the performance of this element is not critical  
=> then it is more cost-effective to use an existing software component to implement the element's functions

> A complex element can be transformed into __a sequence of__
  - __vertical layered elements__  
    Chiều dọc, các thành phần bên trên không biết các thành phần bên dưới ntn, chỉ call các function ở tầng dưới
  - __horizontally tiered elements__
    Chiều ngang  
  => Tùy đặc điểm của dự án, chia đến khi nào không còn phức tạp nữa thì thôi

### Liên kết các phần mềm
- __The connectors__ of a software architecture should be
    - refined within the design process
    => Tùy vào platform

- During the refinement of the software architecture
  - A single process -> mapped to a local method invocation
  - Two different process on the same computer -> local message queue or a pipe
  - Two different elements -> remote method invocation of Web service invocation

- Based on connector's synchroniztion mode
  - Blocking 
    - Wait for a response
  -Non-blocking
    - Continue its execution

- Based on the connector's initiator
  - An initiator is an incident element of a connector that can make a request to its partner
  - __one-initiator connectors__
  - __two-initiator connectors__
    > Call back

- Based on connector's information carrier
  - Variable
  - Environment resource
  - Method
  - Message

- Based on connector's implementation type
  - Signature-based
  - Protocol-based

- Based on connector's active time
  - Programmed
    - Kết nỗi sẵn, tuần tự
  - Event-driven

- Based on connector span
  - Local
  - Networked

- Based on connector fan-out (độ xòe)
  - 1-1
    - for connecting two elements only
  - 1-*

- Based on connector environment
  - Homogenous
  - Heterogeneous
