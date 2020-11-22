# Interview Cheatsheet

## :pencil: Index

## Normal Bir HTML Rendering Akışı

1. HTML parse edilerek DOM ağacı oluşturulur,
2. JS ile DOM API gelen değişiklikler DOM Ağacını günceller
3. StyleSheet CSS tarafından parse edilir. StyleSheet kuralları oluşturulur
4. DOM Tree ve Style Rules birleştirilerek Render Tree oluşturulur.
5. Layout yani tarayıcının özellikleri (Dekstop, Mobile, Çözünürlük vb..) göre ekrana boyama işlemi gerçekleştirilir.
