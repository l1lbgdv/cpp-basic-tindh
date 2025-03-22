# Hướng Dẫn Cơ Bản Về Các Cú Pháp Trong C++ (Dành Cho Lập Trình Thi Đấu)

## 1. Cấu trúc chương trình C++ cơ bản

   - **`#include <bits/stdc++.h>`**: Thư viện bao gồm hầu hết các thư viện tiêu chuẩn của C++, giúp giảm thời gian nhập liệu trong lập trình thi đấu.
   - **`using namespace std;`**: Sử dụng không gian tên chuẩn (`std`), giúp truy cập trực tiếp các hàm và đối tượng trong `std` mà không cần phải viết `std::` trước mỗi lần sử dụng.
   - **`int main()`**: Hàm chính của chương trình, nơi bắt đầu thực hiện chương trình.
   - **`return 0;`**: Kết thúc hàm `main`, trả về giá trị 0 cho hệ điều hành, biểu thị chương trình chạy thành công.

   ```cpp
   #include <bits/stdc++.h>
   using namespace std;

   int main() {
       cout << "Hello, World!" << endl;
       return 0;
   }
   ```

## 2. Biến và kiểu dữ liệu

   - **Kiểu dữ liệu cơ bản**: Các kiểu dữ liệu thường gặp bao gồm `int` (số nguyên), `float` (số thực đơn), `double` (số thực kép), `char` (ký tự), và `bool` (giá trị logic).
   - **Khai báo biến**: Sử dụng cú pháp `type variable_name = value;` để khai báo biến và gán giá trị ban đầu.

   ```cpp
int a = 10;         // Số nguyên
float b = 5.5;      // Số thực đơn
double c = 3.14159; // Số thực kép
char d = 'A';       // Ký tự
bool e = true;      // Giá trị logic
   ```

## 3. Toán tử

   - **Toán tử số học**: Bao gồm `+` (cộng), `-` (trừ), `*` (nhân), `/` (chia), `%` (phép chia lấy dư).
   - **Toán tử so sánh**: Dùng để so sánh hai giá trị, bao gồm `==` (bằng), `!=` (không bằng), `<` (nhỏ hơn), `>` (lớn hơn), `<=` (nhỏ hơn hoặc bằng), `>=` (lớn hơn hoặc bằng).
   - **Toán tử logic**: Dùng để thực hiện các phép toán logic, bao gồm `&&` (và), `||` (hoặc), `!` (phủ định).
   - **Toán tử gán**: Dùng để gán giá trị cho biến, bao gồm `=` (gán), `+=` (cộng và gán), `-=` (trừ và gán), `*=` (nhân và gán), `/=` (chia và gán).

   ```cpp
int x = 10;
int y = 5;
int z = x + y; // z = 15
   ```

## 4. Cấu trúc điều kiện

   - **Câu lệnh `if`, `else if`, `else`**: Kiểm tra điều kiện và thực hiện các khối lệnh tương ứng. Dùng để quyết định chương trình sẽ làm gì dựa trên các điều kiện cụ thể.

   ```cpp
int num = 10;
if (num > 0) {
    cout << "Positive number";
} else if (num < 0) {
    cout << "Negative number";
} else {
    cout << "Zero";
}
   ```

   - **Câu lệnh `switch`**: Thay thế cho nhiều câu lệnh `if...else if...` khi có nhiều trường hợp cần kiểm tra, thường dùng khi cần so sánh một biến với nhiều giá trị khác nhau.

   ```cpp
int day = 3;
switch (day) {
    case 1: cout << "Monday"; break;
    case 2: cout << "Tuesday"; break;
    case 3: cout << "Wednesday"; break;
    default: cout << "Invalid day"; break;
}
   ```

## 5. Vòng lặp

   - **Vòng lặp `for`**: Lặp với số lần xác định, rất hữu ích khi biết trước số lần lặp.

   ```cpp
for (int i = 0; i < 10; i++) {
    cout << i << " ";
}
   ```

   - **Vòng lặp `while`**: Lặp đến khi điều kiện sai, dùng trong trường hợp số lần lặp chưa xác định.

   ```cpp
int i = 0;
while (i < 10) {
    cout << i << " ";
    i++;
}
   ```

   - **Vòng lặp `do...while`**: Tương tự như `while`, nhưng vòng lặp sẽ thực hiện ít nhất một lần trước khi kiểm tra điều kiện.

   ```cpp
int i = 0;
do {
    cout << i << " ";
    i++;
} while (i < 10);
   ```

## 6. Hàm

   - **Khai báo hàm**: Hàm là một khối mã lệnh thực hiện một nhiệm vụ cụ thể. Hàm có thể trả về giá trị (sử dụng cú pháp `type function_name(parameters)`) hoặc không trả về giá trị (sử dụng `void`).

   ```cpp
   int add(int a, int b) {
       return a + b;
   }

   int main() {
       int result = add(3, 4);
       cout << result; // Kết quả là 7
       return 0;
   }
   ```

## 7. Mảng

   - **Khai báo mảng**: Mảng là một danh sách các phần tử cùng kiểu dữ liệu, được truy cập thông qua chỉ số.

   ```cpp
int arr[5] = {1, 2, 3, 4, 5};
cout << arr[0]; // Truy cập phần tử đầu tiên
   ```

   - **Vòng lặp qua mảng**: Dùng vòng lặp `for` hoặc `while` để duyệt qua các phần tử của mảng.

   ```cpp
for (int i = 0; i < 5; i++) {
    cout << arr[i] << " ";
}
   ```

## 8. Chuỗi

   - **Khai báo chuỗi**: Sử dụng kiểu `string` từ thư viện `<string>`, chuỗi là một mảng ký tự kết thúc bởi ký tự null (`''`).

   ```cpp
string str = "Hello, C++!";
cout << str;
   ```

## 9. Con trỏ

   - **Khai báo và sử dụng con trỏ**: Con trỏ là biến lưu trữ địa chỉ của biến khác. Con trỏ được sử dụng nhiều trong việc quản lý bộ nhớ, tối ưu hóa và thao tác với mảng.

   ```cpp
   int var = 20;
   int *ptr = &var;

   cout << "Giá trị của var: " << var << endl;
   cout << "Địa chỉ của var: " << ptr << endl;
   cout << "Giá trị qua con trỏ: " << *ptr << endl;
   ```

## 10. Thao tác với file

   - **Sử dụng `freopen` để thao tác với file**: `freopen` là một cách tiện dụng để chuyển hướng input/output từ bàn phím/màn hình sang file và ngược lại, đặc biệt hữu ích trong lập trình thi đấu khi cần nhập/xuất dữ liệu từ file.

   ```cpp
   int main() {
       freopen("input.txt", "r", stdin);   // Đọc dữ liệu từ file input.txt
       freopen("output.txt", "w", stdout); // Ghi dữ liệu ra file output.txt

       int n;
       cin >> n;
       cout << "Số vừa nhập là: " << n << endl;

       fclose(stdin);
       fclose(stdout);
       return 0;
   }
   ```
## BONUS
Dưới đây là các công thức được viết theo dạng **mã giả (pseudocode)** để dễ hiểu và có thể triển khai thành code trong các ngôn ngữ lập trình khác nhau:  

---

## **1. Đếm số lượng ước số của \( N \)**  
**Công thức:**  
\[
D(N) = (e_1 + 1) \times (e_2 + 1) \times ... \times (e_T + 1)
\]
**Mã giả:**  
```
function count_divisors(factors):
    result = 1
    for each (p, e) in factors:
        result = result * (e + 1)
    return result
```
📌 **Ví dụ:** \( N = 60 = 2^2 \times 3^1 \times 5^1 \)  
\[
D(60) = (2+1) \times (1+1) \times (1+1) = 3 \times 2 \times 2 = 12
\]

---

## **2. Tổng tất cả các ước số của \( N \)**  
**Công thức:**  
\[
S(N) = \left(\frac{p_1^{e_1+1} - 1}{p_1 - 1}\right) \times ... \times \left(\frac{p_T^{e_T+1} - 1}{p_T - 1}\right)
\]
**Mã giả:**  
```
function sum_divisors(factors):
    result = 1
    for each (p, e) in factors:
        term = (p^(e+1) - 1) / (p - 1)
        result = result * term
    return result
```
📌 **Ví dụ:** \( N = 12 = 2^2 \times 3^1 \)  
\[
S(12) = \left(\frac{2^{3} - 1}{2-1} \right) \times \left(\frac{3^{2} - 1}{3-1} \right)
\]
\[
= \left(\frac{8 - 1}{1} \right) \times \left(\frac{9 - 1}{2} \right) = 7 \times 4 = 28
\]

---

## **3. Đếm số lượng ước số chính phương của \( N \)**  
**Công thức:**  
\[
D_{\text{square}}(N) = (\lfloor \frac{e_1}{2} \rfloor + 1) \times (\lfloor \frac{e_2}{2} \rfloor + 1) \times ... \times (\lfloor \frac{e_T}{2} \rfloor + 1)
\]
**Mã giả:**  
```
function count_square_divisors(factors):
    result = 1
    for each (p, e) in factors:
        term = (floor(e / 2) + 1)
        result = result * term
    return result
```
📌 **Ví dụ:** \( N = 60 = 2^2 \times 3^1 \times 5^1 \)  
\[
D_{\text{square}}(60) = (2/2 + 1) \times (1/2 + 1) \times (1/2 + 1) = 2 \times 1 \times 1 = 2
\]

---

## **4. Đếm số lượng ước số lẻ của \( N \)**  
**Công thức:**  
\[
D_{\text{odd}}(N) = (e_2 + 1) \times (e_3 + 1) \times ... \times (e_T + 1)
\]
(bỏ qua thừa số nguyên tố \( 2 \) nếu có).  
**Mã giả:**  
```
function count_odd_divisors(factors):
    result = 1
    for each (p, e) in factors:
        if p != 2:
            result = result * (e + 1)
    return result
```
📌 **Ví dụ:** \( N = 60 = 2^2 \times 3^1 \times 5^1 \)  
\[
D_{\text{odd}}(60) = (1+1) \times (1+1) = 2 \times 2 = 4
\]
(Các ước lẻ là \( 1, 3, 5, 15 \)).

---

## **5. Đếm số lượng ước số là bội số của một số \( k \)**  
**Công thức:**  
- Nếu \( k = p_1^{a_1} \times p_2^{a_2} \times ... \times p_M^{a_M} \), ta xét các thừa số có trong \( N \).
- Với mỗi \( p_i \) xuất hiện cả trong \( k \) và \( N \), ta chỉ có thể chọn số mũ \( \geq a_i \).
\[
D_{\text{multiple}}(N, k) = (e_1 - a_1 + 1) \times (e_2 - a_2 + 1) \times ...
\]
**Mã giả:**  
```
function count_multiples(factors, k_factors):
    result = 1
    for each (p, e) in factors:
        if p exists in k_factors:
            result = result * (e - k_factors[p] + 1)
        else:
            result = result * (e + 1)
    return result
```
📌 **Ví dụ:** \( N = 60 = 2^2 \times 3^1 \times 5^1 \), \( k = 6 = 2^1 \times 3^1 \)  
\[
D_{\text{multiple}}(60, 6) = (2 - 1 + 1) \times (1 - 1 + 1) \times (1+1) = 2 \times 1 \times 2 = 4
\]
(Các bội số của 6 trong các ước của 60 là \( 6, 12, 30, 60 \)).

---

## **Tổng kết**  
Các công thức trên đều dựa trên tư duy **đếm số cách chọn số mũ hợp lệ**. Chúng đều có dạng nhân các số hạng từ \( e_i + 1 \) nhưng có thêm các điều kiện phụ thuộc vào yêu cầu bài toán.  

Mỗi bài toán số học về ước số đều có thể được giải quyết bằng cách **phân tích kỹ cách lựa chọn số mũ của thừa số nguyên tố** rồi áp dụng **quy tắc nhân trong tổ hợp** để đếm số lượng khả năng hợp lệ. 🚀
## Lời kết

Việc nắm vững các cú pháp cơ bản và cách áp dụng chúng vào giải quyết bài toán là nền tảng quan trọng trong lập trình thi đấu. Để thành công, bạn cần luyện tập thường xuyên và tìm hiểu sâu hơn về các thư viện tiêu chuẩn, các thuật toán cơ bản và các kỹ thuật tối ưu hóa.
