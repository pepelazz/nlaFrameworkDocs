## GetFldRef
*поле-ссылка на другой документ*

> Соглашение. Поле, которое является ссылкой на другую таблицу, называется по следующему шаблону: `<имя таблицы>_id`. Например, если ссылка на таблицу `department`, то поле `department_id`.
  Исключение ссылка на таблицу `user`. Потому что поле `user_id` автоматически добавляется ко всем параметрам на стороне сервера - это `id` пользователя, который вызвал данный метод. Соответственно если в документе будет поле `user_id`, то оно будет записываться в базу некорректно. Как вариант можно называть `user_table_id`

##### isShowLink

Для отображения аватарки со ссылкой, нужно добавить параметр **`isShowLink`**

Пример:
```go
    t.GetFldRef("object_id", "объект", "object", [][]int{{1,2}}, "col-4", "isShowLink")
```
<img src="flds/is_show_link.png" style="max-width: 500px">