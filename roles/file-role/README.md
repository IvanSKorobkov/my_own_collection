# File_Content Role

Роль для тестирования модуля file_content.

По умолчанию роль записывает строку **test_content** в файл **test_file** на хосте.
Вы можете изменить имя файла и его содержимое с помощью переменных.
Если содержимое опущено, роль попытается прочитать содержимое файла из существующего файла на хосте.

# Variables

- **test_file** [str] - Путь к файлу. Необязательный.
- **test_content** [str] - Содержимое файла. Необязательный.

# Examples

```yaml
---
- hosts: all
  roles:
    - file_content
      path: 'test'
      content: 'write some bytes'
...
