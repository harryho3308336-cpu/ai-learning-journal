# 第三課：Python 基礎

**日期**：2026-06-09  
**狀態**：🔄 進行中

---

## 1. 變數（Variable）

存儲數據的容器，就像 Excel 的儲存格。

```python
name = "Harry"
age = 21
gpa = 3.4
is_student = True

print(name)   # Harry
print(age)    # 21
```

---

## 2. 列表（List）

存多個值，像 Excel 的一列。

```python
courses = ["FX", "固定收益", "衍生品", "合規"]
print(courses[0])   # FX（從 0 開始數）
print(courses[-1])  # 合規（最後一個）

courses.append("Python")  # 加入新項目
print(len(courses))       # 5（共幾個）
```

---

## 3. 字典（Dictionary）

鍵值對，像 Excel 的一行記錄。

```python
bond = {
    "name": "中國國債 10Y",
    "yield": 2.85,
    "currency": "CNY",
    "rating": "AAA"
}

print(bond["yield"])    # 2.85
print(bond["name"])     # 中國國債 10Y
```

---

## 4. 函數（Function）

把重複的操作包裝起來，一次定義，多次使用。

```python
def calculate_yield_spread(bond_yield, risk_free):
    spread = bond_yield - risk_free
    return spread

result = calculate_yield_spread(2.85, 1.50)
print(result)  # 1.35
```

---

## 5. 迴圈（Loop）

自動重複操作，不用手動一個個處理。

```python
yields = [2.85, 3.10, 4.55, 2.10]

for y in yields:
    if y > 3.0:
        print(f"高收益率：{y}%")
    else:
        print(f"普通收益率：{y}%")
```

---

## 綜合練習：債券組合分析

```python
portfolio = [
    {"name": "中國國債 10Y", "yield": 2.85, "weight": 0.30},
    {"name": "美國國債 10Y", "yield": 4.55, "weight": 0.40},
    {"name": "香港政府債 5Y", "yield": 3.20, "weight": 0.30},
]

total_yield = 0
for bond in portfolio:
    weighted = bond["yield"] * bond["weight"]
    total_yield += weighted
    print(f"{bond['name']}：{bond['yield']}% × {int(bond['weight']*100)}% = {weighted:.2f}%")

print(f"組合加權平均收益率：{total_yield:.2f}%")
```

輸出結果：
```
中國國債 10Y：2.85% × 30% = 0.85%
美國國債 10Y：4.55% × 40% = 1.82%
香港政府債 5Y：3.20% × 30% = 0.96%
組合加權平均收益率：3.63%
```

---

## 金融類比

| Python 概念 | 金融類比 |
|------------|---------|
| 變數 | Excel 儲存格 |
| 列表 | Excel 一列數據 |
| 字典 | Excel 一行記錄（欄位有名稱）|
| 函數 | Excel 公式（定義一次，重複使用）|
| 迴圈 | Excel 批量套用公式 |
