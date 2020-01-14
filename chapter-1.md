# INTRODUCTION TO SOFTWARE ARCHITECTURE

## Architecture
> Architecture is both the process and product of planning, designing, and construction, usually of buildings and other physical structures (Cấu trúc của sản phẩm, công trình vật lý)

__In software__  
#Nestcape Navigator  
#Browser  
#Google Chrome  
#Internet Explorer  
#ChromeOS  

## Software Architecture

___IEEE___ stands for ___Institute of Electrical and Electronics Engineers___ (Định nghĩa chuẩn)
> Thiết kế là cách tổ chức cơ bản

__Acrchitects__ use ___various design strategies___ in software construction:
- To divide and conquer the complexities of a problem domain  
#Micro service

___SAD is important___  
___A good software design___
- __Reduces risks__ in software production, 
- Coordinates development teams to work together orderly
- Makes the system traceable for implementation and testing
- Leads to software products have higher quality attributes

___Quy trình phát triển phần mềm___  
__Analysis__  
->  
__SRS__
- Functional
- Non-functional

->  
__Design__  
->  
__RDS__  
- Component
- Module in each components
- Detailed information

->  
__Implement__

___Architects Role___
> ___Sample outline of SDD (IEEE Std 1016)___  
> - __Design overview, purpose, scope__  
> - __Decomposition description__  
>   - Module
>   - Data
>   - Process
> - __Dependency and connection description__
>   - between modules, data, processes
> - Attributes
> - User interface description
> - Detailed design
>   - module and data

___Software design stage can be split into 2 steps___
- __Architectural design step__  
    - __we describe__
    > - user accessible components
    > - the interconnections among them
      > - visible to stakeholders
- __Detailed design step__
    - __we specify__
    > - The internal details of each component
    > - Might introduce new invisible components to the stakeholders

> Công việc phải làm là phải mô tả được cấu trúc hệ thống

___Architectural Style___
- Abstracts the common properties of a family of similar designs
- Also known as "architecture pattern"
> Cũng giống như thiết kế xậy dựng (Á Đông, Châu Âu) thì software cũng thế
- __Key components__
> - Elements
>   - that perform functions required by a system
> - Connectors
>   - that enable communication, coordination, and cooperation among elemnts
> - Constraints
>   - that define how elements can be integrated to form the system
> - Attributes
>   - that describe the advantages and disadvantages of the choosen structure
- __Các chương sau sẽ được giới thiệu hơn 20 kiểu kiến trúc từ cổ đến nay__

___Architecture Level___
__Enterprise Architecture__
> Những quyết định thay đổi về kiến trúc sẽ có sự ảnh hưởng rất lớn

__Segment Architecture__  
> Những thay đổi kiến trúc sẽ ảnh hưởng chung level nhánh
__Solution Architecture__

___Software architect___
__Sự quan tâm của từng nhóm người dùng:__
- Developer Organization Management Stakeholder
  > Low cost, Keeping people employed
- Marketing Stakeholder
  > Neat features, short time, to market, low cost, parity with competing products
- End-User Stakeholder (nhóm chính)
  > Behavior, performance, security, reliability, usablitiy (không đáp ứng được thì coi như sản phẩm vứt đi)
- Maintenance Organization Stakeholder
  > Modifiability
- Customer Stakeholder (người mua)
  > Low cost, timely delivery, not changed very often
- Architect
  > Căng đấy

___Software architect's tasks___
__Perform__
- System static paritioning (phân chia hệ thống)
> - System decomposition into sub-systems andcommunications between sub-systems
- Establish dynamic control relationships (thiết lập các điều khiển động)
> - between different sub-systems interms of
>   - Data flow
>   - Control flow orchestration
>   - Message dispathching
- Consider and evaluate (Có nhiều hơn 1 giải pháp và phân tích cái lợi hại của từng giải pháp)
- Perform trade-off analysis on quality attributes and other non-functional requirements (linh hoạt phải đưa ra sự đánh đổi dựa trên tình hình, biết phân tích tình huống)
> Trong quá trình design có rất nhiều câu hỏi -> đưa ra câu hỏi và trả lời hết  
> Kiến trúc sư và người kinh doanh có cái nhìn khác nhau, học thêm kinh doanh thì sẽ linh hoạt, có cái nhìn đa chiều hơn

___Quality Attributes___
- Are indentified in the requirement analysis process
- Are closely related to architectural styles
- An architectural style encapsulates tradeoffs among many conflicting quality attributes
> Ưu tiên yêu cầu chất lượng, yêu cầu phi chức năng -> nó sẽ quyết định những cái sau

- Cách phân loại về đặc điểm chất lượng phần mềm:
  > __Classifications__:
    > - Implementation attributes
    > - Runtime attributes
    > - Business attributes

__Implementation attributes:__
- __Interoperability(Tính tương hỗ)__: 
  - Hỗ trợ gọi, sử dụng được bởi mọi nền tảng, các ứng dụng khác dễ dàng truy xuất vào để sử dụng dịch vụ.
  - It needs loose dependency of infrastructure (Ít phụ thuộc vào nền tảng)
  - Ex: Web services
- __Maintainability & extensibility (Thêm, mở rộng về mặt chức năng)__
  - Refers to the ability to modify the system and extend it conveniently
- __Testability (Khả năng kiểm thử)__
  - Refers to the degree
- __Portability (Tính cơ động)__
  - Refers to the level of independence of the system on software and hardware platforms (Phản ánh mức độ độc lập của phần mềm với các nền tảng phần cứng)
    - Systems developed using high-level programming languages usually have good portability

- __Scalability (Tính mở rộng)__
  - Refers to the ability to adapt to an increase of user requests volumn (tính toán số lượng người dùng mở rộng trong tương lai, tránh nút cổ chai)  
- __Flexibility (Tính linh hoạt)__
  - Hệ thống dễ dàng sửa đổi để đáp ứng những sự thay đổi trong tương lai
  __#Component base__  
  __#Service Oriented__  
- __Availability (Tính sẵn sàng)__
  - Refers to the ability of a system to be avaiable 27x7 (Khả năng cung cấp dịch vụ 24/7) => Lưu ý khả năng __dễ bị tấn công gây thiệt hại__
  - Tạo các phương án backup dễ dàng thay thế khi hệ thống bị tấn công, duy trì 24/7
- __Security (Tính bảo mật)__
  - Refers to the abiluty to cope with malicious attacks from outside or inside of the system (Khả năng chống lại tấn công từ bên ngoài cũng như bên trong)  
  __#Firewall__  
  __#SSL__  
  __#Encryption__  
  __#Key logger__  
- __Performance (Hiệu năng)__
  - Refer to increasing efficiencies such as
    - Response time
    - Throughput
    - Generally resource utilizaiton
- __Usability (Tính tiện dụng)__
  - Refers to the level of "satisfaction" from a human perspective in using the system (Mức độ thỏa mãn của người dùng)
    - Includes:
      - completeness
      - correctness
      - compatibility
      - more critically user friendliness

__Business attributes__
- __Time to market__
  > Refers to the time it takes from requirement analysis to the date product is released
- __Cost__
  - Building
  - Maintaining
  - Operating the system
- __Lifetime__  
  __#ransomware__

__Trade-off analysis__
- __Tradeoff between space and time__
  - Ex: to increase the time efficiency of a __#hash table__ means to decrease its space efficiency
  > Được cái lọ mất cái chai
- __Tradeoff between reliability and performance__
- __Tradeoff between scalability and performance__

___Design Guidelines___
> Think of __WHAT__ to do before thinking of __HOW__ to do it
  > - Functional and non-functional requirements
  > - Using an abstract architectural design
> Think of __ABSTRACT__ design before thinking of __CONCRETE__ design
  > Thiết kế kiến trúc và thiết kế chi tiết rành mạch rõ ràng
> Think of __non-functional__ requirements __EARLIER__
  > - *we should consider non-functional requirements as well*
  > - *Communicates with stakeholders* and document their preferences of quality attributes
  > - *It is not possible to find a design that meets all quality attributes*
  > - Balance the quality attributes
> Think of software __reusability__ and __extensibility__ as much as possible
  > - New functionalities *will be added after they are desployed*
  > - How to *reuse existing software components*
> __Tolerate refinement__ of design (không nên quá cầu toàn)
  > - *Never expect* to have software design completely perfect *within one step*
  > - We may need to use *prototyping and iteration* to refine the software design
  > - *Avoid ambiguous design and over-detailed design*
> Try to __PROMOTE high conhesion__ within each element and __loose-coupling__ between elements
  > - A *highly conherent sub-system*
  > - Each architectural style should show a very *clear division*

___SUMMARY___
- Software architectural design
  - has emerged as an important part of software development
- 