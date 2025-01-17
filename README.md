#Hướng dẫn sử dụng file settings.sty
#Các bước bắt buộc (nhiều thứ ở đây được custom nên nếu sử dụng phải nhớ add file)
1. Thêm dòng lệnh \usepackage{settings} ở file chính
2. Sử dụng documentclass[scrartcl][12pt] (hoặc 11pt) thay vì article.
3. Mọi setting nếu muốn chỉnh sửa thì phải vào file settings.sty để làm tối giản file chính.
#Các tùy chọn hiệu quả
1. Từ giờ với mọi set bài toán hoặc bài viết nhiều đoạn, ta nên đưa các thành phần vào cấu trúc itemize, cụ thể như sau: 
*Nếu là một set bài toán thì có thể làm theo mẫu sau:
\begin{itemize}[label=, itemsep=0.5em, leftmargin=0em]
    \item \begin{bt} 
        ...Nội dung bài toán..
    \end{bt}
    \item \begin{bt} 
        ...Nội dung bài toán..
    \end{bt}
    ...
\end{itemize}
*Tương tự với bài viết, nếu muốn đầu đoạn có dấu gạch đầu dòng thì thay label=-
3. Sử dụng cấu trúc sau cho từng bài toán(có khung đẹp)
    \begin{bt} 
        ...Nội dung bài toán...
    \end{bt}
*Nếu có lời giải thì thêm vào
    \begin{sol}
        ...Nội dung lời giải
    \end{sol}
4. Nếu muốn thêm bài toán mà không có khung thì thay {bt} thành {btvn}

5. Sử dụng vocab để tạo kiểu chữ in đậm (đẹp). Ví dụ như bài toán. 

6. Nếu muốn dùng font mặc định của latex thì tìm dòng \renewcommand\familydefault{\sfdefault} và thêm dấu % ở đầu

7.  Với mọi biểu thức toán học dài thì ta nên để vào dấu \[và \] (để đưa ra giữa cho đẹp).
8.  Nếu muốn viết biểu thức ra nhiều bước có dấu = nằm ngay nhau chẵn hạn thì ta dùng
\[
    \begin{aligned} 
        Mệnh đề 1 &= Mệnh đề 2\\
        Mệnh đề 3 &= Mệnh đề 4\\
        ...
    \end{aligned} 
\]
Với dấu & là vị trí năm ngay nhau khi xuống hàng. 
9. Mỗi phần thì dùng section và subsection (dùng như file mẫu).
10. Muốn thêm mục lục thì thêm dòng \tableofcontent ở file chính. 
11. Muốn phát biểu định lý hay bổ đề nào đó thì sử dụng
\begin{theo}[Tên Định lý]
    ...Nội dung định lý...
\end{theo}
hoặc 

12. Các ký hiệu toán học sẽ được viết gọn hơn như sau:	
	Tổng sigma -> \dsum
	Tích Pi -> \dprod
	Giới hạn -> \blim
	Giới hạn (có n ->oo) -> \dlim
	Dấu suy ra -> \ra
	Dấu tương dương -> \lra
	Dấu gạch trên -> \ov
Ngoài ra còn có 
	Với mọi x,y thuộc R -> \xyr
	Với mọi x thuộc R -> \xr
	Với mọi y thuộc R -> \yr
	Với mọi x,y thuộc R^+ -> \xyro
	...
Đọc thêm trong file settings. 
13. Vẽ hình nên xuất file pdf để file nhìn đẹp và nhẹ hơn (tui bị ocd nên mỗi lần nhìn hình phải phóng to thấy nó bị gãy rất khó chịu).
