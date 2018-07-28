# Hoan nghênh bạn đến với D

Nào cùng dạo chơi tìm hiểu về *ngôn ngữ lập trình D*.

{{#dmanmobile}}

Chúng ta sẽ tìm hiểu sơ lược về __sức mạnh__ và __sự truyền cảm__
của ngôn ngữ *D* với khả năng *biên dịch* trực tiếp mã nguồn sang __mã máy__ __hiệu quả__.

{{/dmanmobile}}

### D là gì?

D kết tinh hàng thập kỷ kinh nghiệm phát triển trình biên dịch ở
các ngôn ngữ khác nhau. D có điều đặc biệt như

{{#dmandesktop}}

- cấu trúc cấp cao với khả năng mô hình hóa tuyệt vời
- _hiệu năng cao_, ngôn ngữ biên dịch
- xác định kiểu tĩnh (static typing)
- giao tiếp trực tiếp với API của hệ điều hành hay phần cứng
- khả năng biên dịch _nhanh chóng_ mã nguồn
- một bộ phận của D với khả năng chống lỗi liên quan tới bộ nhớ (SafeD, memory-safe)
- mã nguồn _dễ hiểu_, _dễ bảo trì_
- giúp người học chiếm lĩnh từng bước (cú pháp giống C, tương tự với Java và vài ngôn ngữ khác)
- tương thích với giao diện ứng dụng C đã biên dịch thành mã máy
- tương thích _(có giới hạn)_ với giao diện ứng dụng C++ đã biên dịch thành mã máy
- triển khai nhiều ý niệm (mệnh lệnh theo thứ tự - imperative,
    cấu trúc - structured,
    hướng đối tượng - object oriented,
    đa hình tham số  - generic,
    lập trình hàm thuần túy - functional programming purity,
    và ở mức mã máy - assembly)
- có sẵn bộ dò lỗi (hợp đồng _(contracts)_, kiểm định mức đơn vị _(unittest)_)

... và thêm nhiều  [tính năng khác](http://dlang.org/overview.html).

{{/dmandesktop}}

### Giới thiệu về khúc dạo đầu

Mỗi mục kèm theo mã nguồn minh họa có thể sửa đổi được từ trình duyệt,
và cũng có thể được thi hành khi bạn chọn *Run* hay nhấn phím `Ctrl-enter`.

Để chuyển tới lui giữ các mục, hãy dùng phím "`<` trước" hoặc "sau `>`"
ở cuối trang, hoặc dùng các phím trái, phải. Bạn cũng có thể chọn ngay
các mục cần xem ở menu phía trên.

### Đóng góp

Bạn luôn có thể hoàn thiện tài liệu dạo đầu này bằng cách
tham gia vào dự án [https://github.com/dlang-tour](https://github.com/dlang-tour)
trên Github.

## {SourceCode}

```d
import std.stdio;
import std.algorithm;
import std.range;

void main()
{
    // Nào bắt đầu!
    writeln("Chào thế giới!");

    // Ví dụ  cho lập trình viên kinh nghiệm:
    // Tạo ra ba mảng số và sắp xếp các số trong
    // các mảng đó theo thứ tự tự nhiên
    // mà không cần yêu cầu thêm phần bộ nhớ nào
    int[] arr1 = [4, 9, 7];
    int[] arr2 = [5, 2, 1, 10];
    int[] arr3 = [6, 8, 3];
    sort(chain(arr1, arr2, arr3));
    writefln("%s\n%s\n%s\n", arr1, arr2, arr3);
    // Để hiểu hơn về ví dụ này, hãy xem phần
    // "Thuật toán đoạn" (Range algorithms)
    // ở phần "Gems"
}
```
