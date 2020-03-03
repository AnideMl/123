# Вторая лабораторная работа по разработке ПО.

## File-Reader git

Задачи данного проекта:
  - Чтение;
  - Запись;
  - Получение метаданных;
  - Шифрование;
  - Дешифрование;
  - Подсчет слов палиндромов
	текстового файла

## Delimiter
  - Tab (``\t``)
  - Comma (``,``)

## Basic Example 

```
string Path = @"C:\sample.txt";
var table = Path.FileToTable(heading: true, delimiter: '\t');

// All your processing here

table.TableToFile(@"C:\output.txt");
```

## Pagination Example 

```
int Offset = 0;
int Limit = 100000
string Path = @"C:\sample.txt";
var table = Path.FileToTable(heading: true, delimiter: '\t', offset : Offset, limit: Limit);

// Do all your processing here and with limit and offset and save to drive in append mode
// The append mode will write the output in same file for each processed batch.

table.TableToFile(@"C:\output.txt");
```
