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
