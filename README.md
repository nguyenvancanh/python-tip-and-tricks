## Python, today code better than yesterday

Trên con đường trở thành DevOpps thì việc học python là không thể thiếu đối với mỗi lập trình viên. Cũng là một developer, cũng đang trên con đường trở thành một DevOpps, hơn nữa cũng là người mời bắt đầu nghiên cứu tìm tòi về python, trong quá trình nghiên cứu và tìm tòi quả thật là không tránh khỏi những bỡ ngỡ cũng như là đi vào những hướng làm sai. Những lúc như vậy, kinh nghiệm của những người đi trước, chia sẻ của cộng đồng python là vô cùng quan trọng. Là người đã mắc sai lầm, đã tìm hiểu kiến thức của các bậc tiền bối đi trước, dưới đây tôi xin liệt kê lại một số tip and tricks khi bạn mới học code python hay mắc phải. Hy vọng bài viết này sẽ giúp ích được cho các bạn ít nhiều.

**1. F-String**

Không chỉ trong python, mà bất kỳ ngôn ngữ lập trình nào cũng vậy. Việc thao tác với chuỗi là không thể thiếu. Với **F-string** chúng ta có thể đơn giản và thuận tiện đưa các biểu thức vào trong chuỗi string để format, trước hết hãy khai báo 2 biến tên và tuổi như sau:

```
name = "CanhNV"
age = 28
```

Từ python 3.6, để đưa 2 biến trên vào một string, chúng ta chỉ cần đặt một ký tự f đằng trước chuỗi cần in, và để 2 biến bên trên vào trong dấu ngoặc nhọn. Giải thích thì có vẻ là hơi dài dòng và khó hiểu. Hãy xem ví dụ sau nhé:

```python
name = "CanhNV"
age = 28

output = f"Hello! Myname is {name} and I am {age} year old!"

print(output)
```

Kết quả khi chạy đoạn lệnh trên là:

```
Hello! Myname is Canh NV and I am 28 year old!
```

F-string là cách định dạng các chuỗi mới một cách vô cùng hiệu quả, giúp việc xử lý với chuỗi nhanh hơn, ngắn gọn hơn, và ít lỗi hơn.

**2. Help function**

Python cung cấp cho bạn một function để trực tiếp xem document của một function bạn định dùng, function đó là **help**. Cách dùng vô cùng đơn giản, truyền tên function, module, class, keyword vào bên trong hàm help và chạy

```
Python 3.8.2 (default, Feb 26 2020, 02:56:10)
 help(print)
Help on built-in function print in module builtins:

print(...)
    print(value, ..., sep=' ', end='\n', file=sys.stdout, flush
=False)
    
    Prints the values to a stream, or to sys.stdout by default.
    Optional keyword arguments:
    file:  a file-like object (stream); defaults to the current
 sys.stdout.
    sep:   string inserted between values, default a space.
    end:   string appended after the last value, default a newl
ine.
    flush: whether to forcibly flush the stream.
```

Vô cùng tiện lợi đúng k nào, khi bạn không biết một function cách dùng thế nào thì bạn có thể dễ dàng đọc document của function đó. 

**3. Find the size of any object**

Python cung cấp module default là syn, trong đó có một function giúp chúng ta việc lấy ra size cuả một object đó là getsizeof, tham số đầu vào là một object và kết quả trả về size của object đó dạng byte. Type của object được truyền vào có thể ở bấy kỳ kiểu nào. 

```
import sys

x = [1,2,3,4,5]

print(sys.getsizeof(x))
```

Hoặc một ví dụ khác như sau:

```
import sys

x = "abcvdfdfdf"

print(sys.getsizeof(x))
```

**4. Chuỗi các biểu thức so sánh**

Thông thường, để thực hiện câu lệnh với nhiều hơn 2 điều kiện, thì chúng ta thường cần phải xử dụng thêm toán tử and hoặc or, 

```
if a < b and b < c:
```

Nhưng trong python, việc này đơn giản hơn rất nhiều

```
if a < b < c:
```

Ví dụ như sau:

```
x = 5

if 2 < x < 6:

print ("Pass") 
```

Kết quả trả về là Pass

** 5. Danh sách với biểu thức

Danh sách biểu thức là một cách khác, và nó hay hơn nhiêu so với cách khai báo một danh sách theo cách thông thường. Thông thường, chúng ta khai báo một danh sách rỗng, rồi thêm từng phần tử vào cuối của danh sách, nhưng với danh sách biểu thức thì không cần phải thao tác như vậy, chúng ta hoàn toàn có thể định nghĩa được giá trị của danh sách ngay từ lúc khai báo nó ra, cách làm như sau:

```
new_list = [expression for item in iterable (if conditional)]
```

Đọc xong công thức có thể bạn vẫn chưa hiểu gì, vậy xem thêm ví dụ sau nhé:

```
squares = [x * x for x in range(10)] 

print(squares)
```

Ví dụ trên, chúng ta đang khai báo một danh sách bao gồm các số là bình phương của x, với x chạy từ 0 tới 10. Kết quả thu được là

```
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

Hay là một ví dụ khác, 

```
sentence = "My name is Canh, i was married and have a son. i love him so much!"

filterChar = [i for i in sentence if i in "aueoi"]

print(filterChar)
```

Kết quả thu được sẽ là

```
['a', 'e', 'i', 'a', 'i', 'a', 'a', 'i', 'e', 'a', 'a', 'e', 'a', 'o', 'i', 'o', 'e', 'i', 'o', 'u']
```

**6. Duplicate string**

Python cho phép các bạn làm phép tính nhân không chỉ với kiểu là int, mà còn với các chuỗi string

```
print("test" *4 )

// Result: testtesttesttest
```

**7. Khai báo nhiều biến trên một dòng**

Trong python, bạn có thể khai báo nhiều biến và gán giá trị cho chúng trên một dòng như sau

```
a,b,c = 10,20,30

print(a,b,c)

// Result: 10, 20, 30
```

Ngắn gọn hơn, bạn có thể viết thành

```
a,b,c = [10,20,30]

print(a,b,c)
```

**8. Đổi chỗ các phần tử**

Trong rất nhiều ngôn ngữ lập trình, nếu bạn muốn đổi chỗ 2 phần tử cho nhau, thì bạn cần phải khai báo thêm 1 biến tmp, thuật toán đơn giản để đổi chỗ x và y cho nhau như sau:

```
temp = x
x = y
y = temp
```

Trong python, việc này thu gọn lại chỉ bằng 1 dòng, bởi vì python cho phép gán mutiple giá trị cho mutiple biến chỉ bằng một câu lệnh

```
x = 5
y = 10

x, y = y, x

print(x, y)

//Result: 10, 5
```

**9. Create a Enum**

Enum là một class trong python để tạo các danh sách liệt kê, là một tập hợp các tên tượng trưng được gắn với các giá trị không đổi và duy nhất. Để tạo 1 Enum bạn thao tác như sau:

```
class Person:
A = 0
B = 1
C = 2

print(Person.A)

//Result: 0
```

Để truy cập vào member A, bạn chỉ cần gọi Person.A và kết quả trả về là 0. Ví dụ trên có thể viết được ngắn gọn hơn bởi việc dùng hàm range()

```
class Person:
A, B, C = range(3)

print(Person.A)

//Result: 0
```

** 10. Enumerate **

Thông thường khi làm việc với một danh sách, bạn thường muốn lấy ra cả index cũng như value của từng index đó. Hãy định nghĩa một danh sách dạng mảng

```
x = ['a', 'b', 'c']
```

Để lấy được index và value, thông thường chúng ta chỉ cần dùng lệnh for 

```
x = ['a', 'b', 'c']

for i in range(len(x)):
  print(i, x[i])
  
// Result:

0 a
1 b
2 c
```

Sử dụng enumerate:

Enumerate là một hàm tích hợp sẵn của python, cho phép chúng ta lặp qua một tệp với bộ đếm tự động. Về cơ bản nó ghép nối mọi phần tử trong danh sách của chúng ta với từng chỉ mục tương ứng. Hầu hết mọi người đều k biết về nó

```
x = ['a', 'b', 'c']

for i,v in enumerate(x):
  print(i, v)


```

Vô cùng đơn giản đúng k nào. Bài hôm nay mình viết tới đây, hẹn g
