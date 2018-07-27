# Hoan nghênh bạn đến với D

Mừng bạn dạo chơi tìm hiểu về *ngôn ngữ lập trình D*.

{{#dmanmobile}}

Chuyến dạo chơi này giúp bạn hiểu sơ lược về __sức mạnh__
và __sự truyền cảm__ của ngôn ngữ *D* với khả năng dịch trực tiếp
mã nguồn sang __mã máy__ __hiệu quả__.

{{/dmanmobile}}

### D là gì?

D is the culmination of _decades of experience implementing compilers_
for many diverse languages and has a unique set of features:

{{#dmandesktop}}

- _high level_ constructs for great modeling power
- _high performance_, compiled language
- static typing
- direct interface to the operating system API's and hardware
- blazingly fast compile-times
- memory-safe subset (SafeD)
- _maintainable_, _easy to understand_ code
- gradual learning curve (C-like syntax, similar to Java and others)
- compatible with C application binary interface
- limited compatibility with C++ application binary interface
- multi-paradigm (imperative, structured, object oriented, generic, functional programming purity, and even assembly)
- built-in error detection (contracts, unittests)

... and many more [features](http://dlang.org/overview.html).

{{/dmandesktop}}

### About the tour

Each section comes with a source code example that can be modified and used
to experiment with D's language features.
Click the run button (or `Ctrl-enter`) to compile and run it.

To navigate this tour, either use the "`<` previous" and "next `>`" links at the
bottom (or left and right arrow keys), or else go straight to particular sections
using the menus at the top.

### Đóng góp

Tài liệu dạo đầu này được tổ chức bởi [https://github.com/dlang-tour](https://github.com/dlang-tour)
và chúng tôi luôn hoan nghênh bạn đóng góp để nó tốt hơn.

## {SourceCode}

```d
import std.stdio;
import std.algorithm;
import std.range;

void main()
{
    // Nào bắt đầu!
    writeln("Chào thế giới!");

    // Ví dụ dành cho lập trình viên kinh nghiệm:
    // Tạo ra ba mảng số và sắp xếp chúng theo thứ tự tự nhiên
    // mà không cần yêu cầu thêm phần bộ nhớ nào
    int[] arr1 = [4, 9, 7];
    int[] arr2 = [5, 2, 1, 10];
    int[] arr3 = [6, 8, 3];
    sort(chain(arr1, arr2, arr3));
    writefln("%s\n%s\n%s\n", arr1, arr2, arr3);
    // Để hiểu hơn về ví dụ này, bạn hãy tham khảo phần
    // "thuật toán đoạn" (Range algorithms) ở phần "Gems"
}
```
