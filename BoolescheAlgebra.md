## 1. Implikation (A → B) 的真值表 
| A | B | A → B (A Implies B) |
|----|----|---------------------|
| 真 (True) | 真 (True) | 真 (True) |
| 真 (True) | 假 (False) | 假 (False) |
| 假 (False) | 真 (True) | 真 (True) |
| 假 (False) | 假 (False) | 真 (True) | 
## 2. XOR (A ⊕ B) 的真值表 
| A | B | A ⊕ B (A XOR B) | 
|----|----|-------------------| 
| 真 (True) | 真 (True) | 假 (False) | 
| 真 (True) | 假 (False) | 真 (True) | 
| 假 (False) | 真 (True) | 真 (True) | 
| 假 (False) | 假 (False) | 假 (False) | 
## 3. NOR (A ↓ B) 的真值表 
| A | B | A ↓ B (A NOR B) | 
|----|----|------------------| 
| 真 (True) | 真 (True) | 假 (False) | 
| 真 (True) | 假 (False) | 假 (False) | 
| 假 (False) | 真 (True) | 假 (False) | 
| 假 (False) | 假 (False) | 真 (True) | 

# 真值表

## Implikation (A → B) 和 交换律 (B → A) 的真值表

| A  | B  | A → B (A Implies B) | B → A (B Implies A) |
|----|----|---------------------|---------------------|
| T  | T  | T                   | T                   |
| T  | F  | F                   | T                   |
| F  | T  | T                   | F                   |
| F  | F  | T                   | T                   |

### 解释
- **A 为真，B 为真**：
  - A → B 为真。
  - B → A 为真。
  
- **A 为真，B 为假**：
  - A → B 为假。
  - B → A 为真。
  
- **A 为假，B 为真**：
  - A → B 为真。
  - B → A 为假。
  
- **A 为假，B 为假**：
  - A → B 为真。
  - B → A 为真。

从真值表中可以看出，A → B 和 B → A 在某些情况下（例如 A 为真，B 为假时）其结果并不相同，因此条件运算（Implikation）不符合交换律。
