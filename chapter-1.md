# Android programming

## Feature of Android
- UI & UX
- Connectivity
- Storage

## Android Architecture
### Linux kernel
### Hardware Abstraction Layer (HAL)
### Libraries
> Contain C/C++ libraries used by components of Android Systems
### Android Runtime (ART)
> Designed to run apps in a contrained evironment that has limited muscle power in terms of battery, processing and memory
### Application Framework (Java API)
> Access to the complete feature set of Android OS
> There are 4 database be used
### Applications

## Application Components
### Android Activities
- A subclass of Activity class
- A single user interface screen
- Reuseable
### Android Intents
> Cơ chế gọi từ activity này sang activity khác

- Explicit intent (call mở activity khác)
- Implicit intent (giả sử call activity app phone)
<pre><code>Intent intent = new Intent.ACTION_DIAL, Uri.parse("tel: 9999");
startActivity(intent);
</code></pre>

### Android Services
> Không có user interface, chạy ngầm phục vụ mục đích gì đó
### Content Providers
- Content Providers (có thể chia sẻ CSDL với các app khác)
> Implement a mechanism for the sharing of data between applications
- SQLite database
### Application Manifest
> Tổng hợp các thành phần source của app để quản lý
### Application Resource
- resource file
- file non-code
### Application Context
> Cho phép giao tiếp giữa file giao diện với file code
## Activity Lifecycles
### Android Process States
> Phân cấp process theo ranking
- Foreground Process (app chạy trên màn hình)
- Visible Process (app chạy ngầm)
- Service Process (service phục vụ cho các app chạy)
- Background Process (app dạng đã kill)
- Empty Process
> A hit a time

### Inter-Process Dependency
> Nếu service process phục vụ cho foreground process thì sẽ có độ ưu tiên ngang foreground process

### The Activity Lifecycle
### The Activity Stac
### Configuration Changes
## Handling Activity State Changes
### Handling State Changes
> Ngăn chặn dữ liệu bị destroy
<pre><code>android:configChanges=""
</code></pre>
- Foreground Lifetime
- Visible Lifetime
- 
### Saving the State
- Automatic saving and restoring
### Restoring the State

## Understanding Android Views, View Groups and Layouts
### Android Layout Managers
> Thiết kế giao diện trong Android OS
- ContraintLayout(Hiện tại được sử dụng nhiều nhất)
- LinearLayout
- TableLayout
- FrameLayout
- RelativeLayout
- AbsoluteLayout
- GridLayout
- CoordinateLayout

### The Android Studio Layout Editor
> Có 2 loại mode design
- Design Mode
- Text Mode (XML)

