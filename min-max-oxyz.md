**Bài 1:** Trong không gian $Oxyz$, cho mặt phẳng $(P): 2x - y + z + 1 = 0$ và hai điểm $A(2; -1; 0)$, $B(3\sqrt{3}; 0; -1)$. Điểm $M(x; y; z)$ di động trên $(P)$, tìm giá trị nhỏ nhất của biểu thức $T = -MA + 7MB$. Tính giá trị $Q = 3a + 9b + 2025$ với $T_{min} = a\sqrt{b}$.

---

#### **Bước 1: Thiết lập hệ phương trình Lagrange**

Xét hàm Lagrange cho bài toán tối ưu có ràng buộc:

$$L = - \sqrt{(x-2)^2 + (y+1)^2 + z^2} + 7 \sqrt{(x-3\sqrt{3})^2 + y^2 + (z+1)^2} + \lambda(2x - y + z + 1)$$

Hệ phương trình đạo hàm riêng (điểm dừng):

$$
\begin{cases}
& -\frac{x - 2}{MA} + 7\frac{x - 3\sqrt{3}}{MB} + 2\lambda = 0 \\
& -\frac{y + 1}{MA} + 7\frac{y}{MB} - \lambda = 0 \\
& -\frac{z}{MA} + 7\frac{z + 1}{MB} + \lambda = 0 \\
& 2x - y + z + 1 = 0
\end{cases}
$$

Nhìn vào hệ đạo hàm Lagrange, đổi 3 phương trình đầu về dạng Vector sẽ là:

$$\nabla f = -\frac{\vec{PA}}{PA} + 7\frac{\vec{PB}}{PB} + \lambda \vec{n} = \vec{0}$$

Suy ra P, A, B thuộc cùng 1 mặt phẳng.
#### **Bước 2: Triệt tiêu tham số $\lambda$ để tìm quan hệ tuyến tính**
Cộng phương trình (2) và (3) theo vế để khử $\lambda$:

$$\left( -\frac{y+1}{MA} + 7\frac{y}{MB} \right) + \left( -\frac{z}{MA} + 7\frac{z+1}{MB} \right) = 0$$

$$\iff -\frac{y+z+1}{MA} + \frac{7(y+z+1)}{MB} = 0 \iff (y+z+1) \left( \frac{7}{MB} - \frac{1}{MA} \right) = 0$$

**Trường hợp 1**: **$\frac{7}{MB} - \frac{1}{MA} = 0$**.

$\rightarrow MB = 7MA$

$\rightarrow$ $\frac{\vec{MA}}{MA} - 7\frac{\vec{MB}}{7MA} = \lambda \vec{n}$

$\rightarrow \frac{\vec{MA} - \vec{MB}}{MA} = \lambda \vec{n}$

Vì $\vec{MA} - \vec{MB} = \vec{BA}$, phương trình trở thành: $\frac{\vec{BA}}{MA} = \lambda \vec{n}$

$\implies$Điều này có nghĩa là Vector **$\vec{BA}$** phải **cùng phương** với vector pháp tuyến $\vec{n}$ của mặt phẳng (tức là đường thẳng $AB$ phải vuông góc với mặt phẳng).

**Kiểm tra thực tế:** 
*   Vector $\vec{BA} = (2 - 3\sqrt{3}; -1; 1)$
*   Vector $\vec{n} = (2; -1; 1)$
Hai vector này **không cùng phương**. Ta loại trường hợp 1. 



**Trường hợp 2**: **$y + z + 1 = 0 \implies z = -1 - y$**.

Kết hợp với phương trình mặt phẳng $(P)$ mà đề đã cho:

$$
\begin{cases} 2x - y + z = -1 \\ 
y + z = -1 \end{cases}
\implies 
\begin{cases} 
z = t \\
y = -t - 1 \\
2x - (-t - 1) + t = -1 
\end{cases}
\implies 
\begin{cases}
x = -t - 1 \\
y = -t - 1 \\
z = t 
\end{cases}
$$

$\implies M(t; t; -1-t)$

#### **Bước 3: Tối ưu hàm một biến bằng Casio**
Thay tọa độ $M$ vào biểu thức khoảng cách:
*   $MA = \sqrt{(t-2)^2 + (t+1)^2 + (-1-t)^2} = \sqrt{3t^2 + 6}$
*   $MB = \sqrt{(t-3\sqrt{3})^2 + t^2 + (-1-t+1)^2} = \sqrt{3t^2 - 6\sqrt{3}t + 27}$

Hàm mục tiêu: $T(t) = 7\sqrt{3t^2 - 6\sqrt{3}t + 27} - \sqrt{3t^2 + 6}$
Sử dụng tính năng **`SHIFT SOLVE`** cho phương trình $T'(t) = 0$:
Máy tính nhả nghiệm: $t = \frac{7\sqrt{3}}{6}$.

#### **Bước 4: Tính giá trị cực tiểu và kết luận**
Tại $t = \frac{7\sqrt{3}}{6}$, ta tính được:
*   $MA^2 = 3 \cdot \left(\frac{49}{12}\right) + 6 = \frac{73}{4} \implies MA = \frac{\sqrt{73}}{2}$
*   $MB^2 = 3 \cdot \left(\frac{49}{12}\right) - 6\sqrt{3} \cdot \left(\frac{7\sqrt{3}}{6}\right) + 27 = \frac{73}{4} \implies MB = \frac{\sqrt{73}}{2}$

Giá trị nhỏ nhất:
$$T_{min} = 7 \cdot \frac{\sqrt{73}}{2} - 1 \cdot \frac{\sqrt{73}}{2} = 6 \cdot \frac{\sqrt{73}}{2} = \mathbf{3\sqrt{73}}$$
$\implies a = 3, b = 73$.

Giá trị biểu thức $Q$:
$$Q = 3(3) + 9(73) + 2025 = 9 + 657 + 2025 = \mathbf{2691}$$

**Đáp số: 2691.**

---

**Bài 2**: Trong không gian Oxyz, cho ba điểm $A(1;2;3); B(1;2;0)$ và $M(-1;3;4)$. Gọi $d$ là đường thẳng qua B, vuông góc với AB đồng thời cách M một khoảng nhỏ nhất. Một vector chỉ phương của d có dạng $\vec{u}(2;a;b)$. Tính $a+b$.

---

#### Bước 1: Tìm ràng buộc Đại số (Constraints)
Đường thẳng $d$ đi qua $B(1,2,0)$. Khoảng cách từ $M(-1,3,4)$ đến $d$ là nhỏ nhất.

Gọi $H(x, y, z)$ là hình chiếu vuông góc của $M$ lên đường thẳng $d$.
Lúc này, khoảng cách cần tìm chính là đoạn $MH$. Đường thẳng $d$ chính là đường thẳng đi qua $B$ và $H$.


**Ràng buộc 1:** $d \perp AB \implies \vec{BH} \perp \vec{AB} \implies \vec{BH} \cdot \vec{AB} = 0$.
*   $\vec{BH} = (x-1, y-2, z)$
*   $\vec{AB} = (0, 0, -3)$

Tích vô hướng: $(x-1)\cdot 0 + (y-2)\cdot 0 + z\cdot(-3) = 0 \implies \mathbf{-3z = 0 \implies z = 0}$.

> Tuyệt vời! Đại số tự động khai tử biến z. Từ đây ta biết Vector chỉ phương $$\vec{u}$$ có cao độ $b = 0$. Điểm $H$ giờ chỉ còn là $$H(x,y,0)$$.

**Ràng buộc 2:** $H$ là hình chiếu của $M$ lên $d \implies MH \perp BH \implies \vec{MH} \cdot \vec{BH} = 0$.
*   $\vec{MH} = (x - (-1), y - 3, 0 - 4) = (x+1, y-3, -4)$
*   $\vec{BH} = (x-1, y-2, 0)$

Tích vô hướng: $(x+1)(x-1) + (y-3)(y-2) + (-4)(0) = 0$
$\implies x^2 - 1 + y^2 - 5y + 6 = 0$
$\implies \mathbf{x^2 + y^2 - 5y + 5 = 0} \quad (*)$

> Đây chính là phương trình Ràng buộc $g(x,y) = 0$ cho hệ Lagrange).

---

#### Bước 2: Lập hệ Đạo hàm (Lagrange Style)
Mục tiêu: **Tìm Min của $MH^2$** (do $MH^2$ đạt GTNN thì $MH$ cũng có GTNN, nên đưa về bình phương cho dễ tính)

$$f(x,y) = MH^2 = (x+1)^2 + (y-3)^2 + 16$$

Với điều kiện ràng buộc $(*)$: $x^2 + y^2 - 5y + 5 = 0$.

Viết hệ 2 phương trình đạo hàm (Đạo hàm $f$ cộng $\lambda \times$ Đạo hàm $g$):

$$\begin{cases} 
L'_x = 2(x+1) + \lambda(2x) = 0 & (1) \\
L'_y = 2(y-3) + \lambda(2y - 5) = 0 & (2) 
\end{cases}$$

---

#### Bước 3: Ép $\lambda$ triệt tiêu
Rút $\lambda$ từ cả hai phương trình rồi cho chúng bằng nhau:
*   Từ (1) $\implies \lambda = -\frac{x+1}{x}$
*   Từ (2) $\implies \lambda = -\frac{y-3}{y-2.5}$ *(Chia 2 cả tử và mẫu cho gọn)*

Ép chúng bằng nhau (Nhân chéo):

$$\frac{x+1}{x} = \frac{y-3}{y-2.5}$$

$$(x+1)(y-2.5) = x(y-3)$$

$$xy - 2.5x + y - 2.5 = xy - 3x$$

$$0.5x + y - 2.5 = 0$$

Nhân đôi 2 vế cho đẹp:

$$\mathbf{x + 2y - 5 = 0 \implies x = 5 - 2y}$$

---

#### Bước 4: Lấy các kết quả cần thiết

Thay $x = 5-2y$ vào Ràng buộc $(*)$ ban đầu:

$$(5-2y)^2 + y^2 - 5y + 5 = 0$$

$$25 - 20y + 4y^2 + y^2 - 5y + 5 = 0$$

$$5y^2 - 25y + 30 = 0$$

Rút gọn cho 5:

$$y^2 - 5y + 6 = 0$$

Bấm máy tính, ra 2 nghiệm cực đẹp:

**Nghiệm 1: $y = 3 \implies x = 5 - 2(3) = -1$.** Ta có điểm $H_1(-1, 3, 0)$.

**Nghiệm 2: $y = 2 \implies x = 5 - 2(2) = 1$.** Ta có điểm $H_2(1, 2, 0)$.

> Đại số luôn tìm ra TẤT CẢ cực trị. Một cái sẽ là Min, một cái sẽ là Max. Thử tính khoảng cách $MH^2$ cho 2 điểm này):
*   Với $H_1(-1, 3, 0): MH_1^2 = (-1+1)^2 + (3-3)^2 + (0-4)^2 = 16$. **(Đây là MIN)**
*   Với $H_2(1, 2, 0): MH_2^2 = (1+1)^2 + (2-3)^2 + (0-4)^2 = 4 + 1 + 16 = 21$. (Đây là Max).

Vì đề hỏi khoảng cách nhỏ nhất, ta chốt điểm **$H(-1, 3, 0)$**.

---

#### Tính tổng $a+b$

Đường thẳng $d$ đi qua $B(1,2,0)$ và $H(-1,3,0)$.
Vector chỉ phương $\vec{u}$ cùng phương với $\vec{BH} = (-1-1, 3-2, 0-0) = (-2, 1, 0)$.

Để khớp với form đề bài cho là $(2, a, b)$, ta nhân vector này với $-1$:
$$\vec{u} = \mathbf{(2, -1, 0)}$$

Suy ra $a = -1, b = 0$.

Tính $a+b = -1 + 0 = \mathbf{-1}$.


---

**Bài 3**: Trong không gian $(Oxy)$, có 2 trạm phát sóng trên không: trạm A đặt trên không tại vị trí $A(1;1;3)$, trạm B đặt trên không tại vị trí $B(10;13;6)$. Trên mặt đất người ta cần đặt 2 trạm thu tín hiệu M và N sao cho khoảng cách giữa 2 trạm thu là cố định: $MN = 5$ và tổng chiều dài dây nối từ trạm A đến M và từ trạm B đến N là ngắn nhất. Khi đó, tổng hoành độ 2 điểm M và N bằng?

CRE: https://www.tiktok.com/@toanlxo/video/7602578317568429329

### Bước 1: Setup hàm và viết nhanh hệ phương trình
*   **Dữ kiện:** $A(1, 1, 3)$ và $B(10, 13, 6)$. Mặt đất là $(Oxy)$ nên có $M(x_M, y_M, 0)$ và $N(x_N, y_N, 0)$.
*   **Điều kiện (Constraint):** $MN = 5$.
*   **Từ đó lập hàm cần tối ưu:**

    $L = AM + BN + \lambda \cdot (MN - 5)$.

    > Viết hẳn ra cho dễ tưởng tượng còn thực tế nên hạn chế viết hẳn, vì cần tốc độ:

    $L = \sqrt{(x_M - 1)^2 + (y_M - 1)^2 + (0 - 3)^2} + \sqrt{(x_N - 10)^2 + (y_N - 13)^2 + (0 - 6)^2} +  \lambda(\sqrt{(x_N - x_M)^2 + (y_N - y_M)^2} - 5)$



Lập hệ đạo hàm cho các biến $x_M, y_M, x_N, y_N$:

$$\begin{cases}
L'_{x_M} = \frac{x_M - 1}{AM} + \lambda \frac{x_M - x_N}{MN} = 0 & (1) \\
L'_{y_M} = \frac{y_M - 1}{AM} + \lambda \frac{y_M - y_N}{MN} = 0 & (2) \\
L'_{x_N} = \frac{x_N - 10}{BN} + \lambda \frac{x_N - x_M}{MN} = 0 & (3) \\
L'_{y_N} = \frac{y_N - 13}{BN} + \lambda \frac{y_N - y_M}{MN} = 0 & (4) \\
L'_{\lambda} = MN - 5 
\end{cases}$$

### Bước 2: Triệt tiêu $\lambda$ 
Nhìn vào các phần tử có mẫu số là $MN$ chứa $\lambda$. Thấy được $\frac{x_M - x_N}{MN}$ và $\frac{x_N - x_M}{MN}$ là hai giá trị **đối nhau**.

$\implies$ Lấy **(1) + (3)**:
$$\frac{x_M - 1}{AM} + \frac{x_N - 10}{BN} = 0 \iff \mathbf{\frac{x_M - 1}{AM} = \frac{10 - x_N}{BN}} \quad (*)$$

Tương tự, lấy **(2) + (4)**:

$$\frac{y_M - 1}{AM} + \frac{y_N - 13}{BN} = 0 \iff \mathbf{\frac{y_M - 1}{AM} = \frac{13 - y_N}{BN}} \quad (**)$$

### Bước 3: Tư duy Vector Đơn vị

Theo Pythagoras trong không gian 3D, bình phương chiều dài sợi dây bằng tổng bình phương 3 độ lệch:

$$d^2 = \Delta x^2 + \Delta y^2 + \Delta z^2$$

Chia tất cả cho $d^2$, ta được một hệ thức luôn bằng **1**:

$$ \frac{\Delta x^2}{d^2} + \frac{\Delta y^2}{d^2} + \frac{\Delta z^2}{d^2} = 1 $$


$$\implies \begin{cases}
\left(\frac{x_M - 1}{AM}\right)^2 + \left(\frac{y_M - 1}{AM}\right)^2 + \left(\frac{0 - 3}{AM}\right)^2 = 1 \\
\left(\frac{10 - x_N}{BN}\right)^2 + \left(\frac{13 - y_N}{BN}\right)^2 + \left(\frac{0 - 6}{BN}\right)^2 = 1
\end{cases}$$

Mà ta có $(*)$ và $(**)$ nên:

$$\implies \begin{cases}
\left(\frac{x_M - 1}{AM}\right)^2 + \left(\frac{y_M - 1}{AM}\right)^2 + \left(\frac{0 - 3}{AM}\right)^2 = 1 \\
\left(\frac{x_M - 1}{AM}\right)^2 + \left(\frac{y_M - 1}{AM}\right)^2 + \left(\frac{0 - 6}{BN}\right)^2 = 1
\end{cases}$$

$$\implies \left(-\frac{3}{AM}\right)^2 = \left(-\frac{6}{BN}\right)^2$$

$$\implies \mathbf{BN = 2AM}$$


### Bước 4: Chuyển về hệ phương trình bậc nhất
Thay $BN = 2AM$ ngược lại vào phương trình $(*)$ và $(**)$:

$$\frac{x_M - 1}{AM} = \frac{10 - x_N}{2AM} \implies \mathbf{2x_M + x_N = 12}$$

$$\mathbf{\frac{y_M - 1}{AM} = \frac{13 - y_N}{BN}} \implies 2y_M + y_N = 15$$

### Bước 5: Tìm M
Từ $x_N = 12 - 2x_M$ và $y_N = 15 - 2y_M$, thế vào điều kiện $MN = 5$ ta được:

$$(12 - 3x_M)^2 + (15 - 3y_M)^2 = 25 \iff \mathbf{(x_M - 4)^2 + (y_M - 5)^2 = \frac{25}{9}}$$



**Tham số hóa Lượng giác (Casio)**:

Từ phương trình đường tròn: $(x - 4)^2 + (y - 5)^2 = \left(\frac{5}{3}\right)^2$.
Mọi điểm nằm trên đường tròn này luôn có dạng:

$$\begin{cases} 
x = 4 + \frac{5}{3} \cos t \\
y = 5 + \frac{5}{3} \sin t 
\end{cases}$$

Thay thẳng cục này vào hàm cần đạt Min:

$$AM + BN = AM+2AM = 3AM$$

> Đoạn này không cần $\lambda \cdot (MN - 5)$ nữa vì khi thay x và y bên trên vào ta đang xét trên ràng buộc để $MN=5$ rồi

$$3AM = \sqrt{(x - 1)^2 + (y - 1)^2 + 9}$$

$$3\sqrt{\left(3 + \frac{5}{3}\cos t\right)^2 + \left(4 + \frac{5}{3}\sin t\right)^2 + 9}$$

Chạy Casio TABLE tìm Min: Với khoảng từ 0 $\rightarrow$ 2 $\cdot\pi$, STEP là 2 $\cdot\pi$ / 29

<table border="1">
  <tr>
    <th>x</th>
    <th>y</th>
  </tr>
  <tr>
    <td>...</td>
    <td>...</td>
  </tr>
  <tr>
    <td>3.6832</td>
    <td>13.856</td>
  </tr>
  <tr>
    <td>3.8999</td>
    <td>13.532</td>
  </tr>
  <tr>
    <td>4.1165</td>
    <td>13.459</td>
  </tr>
  <tr>
    <td>...</td>
    <td>...</td>
  </tr>
</table>

Thấy được trên TABLE $x = 4.1165$ có vẻ cho $y$ nhỏ nhất. Ta nhập lại biểu thức $3AM$ vào chế độ tính toán bình thường để `SHIFT SOLVE` tìm nghiệm chuẩn:

$$\frac{d}{dx} \left(3\sqrt{\left(3 + \frac{5}{3}\cos t\right)^2 + \left(4 + \frac{5}{3}\sin t\right)^2 + 9}\right)$$

Tìm được Min = $\sqrt{181}$ tại $t = 4.0688..$ . Thay $t$ vào để tìm $M$:


$$\begin{cases}
x_M = 4 + \frac{5}{3} \cos t \\
y_M = 5 + \frac{5}{3} \sin t
\end{cases}$$

Ta được $M = (3; \frac{11}{3};0)$

Dựa vào điều kiện cũ ở **Bước 4** ta suy ra được $N(6;\frac{23}{3};0)$

**Vậy**, tổng hoành độ điểm $M$ và $N$ bằng: $x_m + x_N = 3 + 6 = 9$
