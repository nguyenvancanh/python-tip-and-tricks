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
