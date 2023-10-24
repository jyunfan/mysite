---
date: 2023-10-25
readtime: 10
categories:
    - Elixir
---

學習一個新語言總是有趣的，這次我想分享一下我學習 Elixir 的心得。

推薦一個學習資源 [ThinkingElixir](https://thinkingelixir.com/available-courses/pattern-matching/)

先來比較一下 python 跟 Elixir 的資料結構，特別注意 Elixir 是 functional programming language，所以資料結構都是 immutable 的，
而且沒有 object method，不管是 List 或是 Map 存取都是用 function。

# Tuple
Python 的 Tuple 跟 Elixir 的 Tuple 很像，但是 Elixir 的 Tuple 是 immutable 的。

    # Python
    data = (1, 2, "GO") # Python
    data[0] # 1
    data[2] # "GO"

    # Elixir
    data = {1, 2, "GO"}
    elem(data, 0) # 1
    elem(data, 2) # "GO"
    put_elem(t, 2, "foo") # 修改第二個值會傳回一個新的 tuple {1, 2, "foo"}



# Map

Python: Dictionary

    data = { "name" : "gary" , "age": 99 }

Elixir: Map

產生 Map

    data = %{ name: "gary", age: 99, city: "Tokyo" }

注意這裡的 name 是一個 atom (:name)

讀取 Map

    data[:name]

寫入 Map

    Map.put(data, :name, "bob")

更新 Map

    %{data | age: 31, city: "Taipei"}

# List

