## Phương thức thêm/xóa phần tử

### 1. `append()` - Thêm phần tử vào cuối list
```python
fruits = ['apple', 'banana']
fruits.append('orange')  # ['apple', 'banana', 'orange']
```

### 2. `extend()` - Nối list với iterable khác
```python
fruits = ['apple', 'banana']
fruits.extend(['orange', 'grape'])  # ['apple', 'banana', 'orange', 'grape']
```

### 3. `insert()` - Chèn phần tử tại vị trí chỉ định
```python
fruits = ['apple', 'banana', 'orange']
fruits.insert(1, 'grape')  # ['apple', 'grape', 'banana', 'orange']
```

### 4. `remove()` - Xóa phần tử đầu tiên tìm thấy
```python
fruits = ['apple', 'banana', 'orange', 'banana']
fruits.remove('banana')  # ['apple', 'orange', 'banana']
```

### 5. `pop()` - Xóa và trả về phần tử tại vị trí
```python
fruits = ['apple', 'banana', 'orange']
last = fruits.pop()  # 'orange', list còn: ['apple', 'banana']
second = fruits.pop(1)  # 'banana', list còn: ['apple']
```

### 6. `clear()` - Xóa tất cả phần tử
```python
fruits = ['apple', 'banana', 'orange']
fruits.clear()  # []
```

## Phương thức tìm kiếm và sắp xếp

### 7. `index()` - Tìm vị trí phần tử đầu tiên
```python
fruits = ['apple', 'banana', 'orange', 'banana']
pos = fruits.index('banana')  # 1
pos = fruits.index('banana', 2)  # 3 (tìm từ vị trí 2)
```

### 8. `count()` - Đếm số lần xuất hiện
```python
numbers = [1, 2, 3, 2, 1, 2]
count = numbers.count(2)  # 3
```

### 9. `sort()` - Sắp xếp list
```python
numbers = [3, 1, 4, 1, 5]
numbers.sort()  # [1, 1, 3, 4, 5]

# Sắp xếp giảm dần
numbers.sort(reverse=True)  # [5, 4, 3, 1, 1]

# Sắp xếp với key function
words = ['apple', 'Banana', 'cherry']
words.sort(key=str.lower)  # ['apple', 'Banana', 'cherry']
```

### 10. `reverse()` - Đảo ngược list
```python
numbers = [1, 2, 3, 4]
numbers.reverse()  # [4, 3, 2, 1]
```

## Phương thức copy

### 11. `copy()` - Tạo bản sao nông (shallow copy)
```python
original = [1, 2, [3, 4]]
copied = original.copy()  # [1, 2, [3, 4]]
```

## Các hàm built-in áp dụng cho list

### 12. `len()` - Lấy độ dài list
```python
fruits = ['apple', 'banana', 'orange']
length = len(fruits)  # 3
```

### 13. `max()` - Tìm giá trị lớn nhất
```python
numbers = [5, 2, 8, 1, 9]
max_value = max(numbers)  # 9
```

### 14. `min()` - Tìm giá trị nhỏ nhất
```python
numbers = [5, 2, 8, 1, 9]
min_value = min(numbers)  # 1
```

### 15. `sum()` - Tính tổng
```python
numbers = [1, 2, 3, 4, 5]
total = sum(numbers)  # 15
```

### 16. `sorted()` - Trả về list đã sắp xếp (không thay đổi list gốc)
```python
numbers = [3, 1, 4, 1, 5]
sorted_numbers = sorted(numbers)  # [1, 1, 3, 4, 5]
# numbers vẫn là [3, 1, 4, 1, 5]
```

### 17. `reversed()` - Trả về iterator đảo ngược (không thay đổi list gốc)
```python
numbers = [1, 2, 3, 4]
reversed_numbers = list(reversed(numbers))  # [4, 3, 2, 1]
# numbers vẫn là [1, 2, 3, 4]
```

## Các phương thức và thao tác khác

### 18. Cộng list (concatenation)
```python
list1 = [1, 2, 3]
list2 = [4, 5, 6]
combined = list1 + list2  # [1, 2, 3, 4, 5, 6]
```

### 19. Nhân list (repetition)
```python
numbers = [1, 2, 3]
repeated = numbers * 3  # [1, 2, 3, 1, 2, 3, 1, 2, 3]
```

### 20. Kiểm tra tồn tại (in operator)
```python
fruits = ['apple', 'banana', 'orange']
has_apple = 'apple' in fruits  # True
has_grape = 'grape' in fruits  # False
```

### 21. Slice (cắt list)
```python
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
slice1 = numbers[2:6]  # [2, 3, 4, 5]
slice2 = numbers[:4]   # [0, 1, 2, 3]
slice3 = numbers[5:]   # [5, 6, 7, 8, 9]
slice4 = numbers[::2]  # [0, 2, 4, 6, 8] (bước nhảy 2)
slice5 = numbers[::-1] # [9, 8, 7, 6, 5, 4, 3, 2, 1, 0] (đảo ngược)
```

## List Comprehensions (Không phải method nhưng quan trọng)

### 22. List Comprehension
```python
# Tạo list bình phương
squares = [x**2 for x in range(10)]  # [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

# Với điều kiện
even_squares = [x**2 for x in range(10) if x % 2 == 0]  # [0, 4, 16, 36, 64]

# Nested comprehension
matrix = [[i*j for j in range(3)] for i in range(3)]
# [[0, 0, 0], [0, 1, 2], [0, 2, 4]]
```
