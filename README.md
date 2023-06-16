# K1
ob one
class Book:
    """
    表示一本图书的类，包含书名和借阅状态属性。
    """

    def __init__(self, title):
        self.title = title
        self.borrowed = False

    def borrow(self):
        """
        借阅图书。
        """
        if self.borrowed:
            print(f"{self.title} 已被借出，请选择其他图书。")
        else:
            self.borrowed = True
            print(f"成功借阅 {self.title}。")

    def return_book(self):
        """
        归还图书。
        """
        if self.borrowed:
            self.borrowed = False
            print(f"成功归还 {self.title}。")
        else:
            print(f"{self.title} 未被借出。")


# 创建图书对象
book1 = Book("Python入门教程")
book2 = Book("数据结构与算法")

# 借阅图书
book1.borrow()
book2.borrow()

# 再次尝试借阅已被借出的图书
book1.borrow()

# 归还图书
book1.return_book()
book2.return_book()
