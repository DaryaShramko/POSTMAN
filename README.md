
## Postman HW_1


*Создать запросы в Postman*:

 
***Protocol: http,
IP: 162.55.220.72,
Port: 5005***


``` python 
EP_1
Method: GET
EndPoint: /get_method
request url params: 
 name: str
 age: int

response: 
[
    “Str”,
    “Str”
]

```

- Заходим в приложение Postman >
- нажимаем Collection > new > ИМЯ КОЛЛЕКЦИИ: EP_1
- в меню нажимаем на коллекцию EP_1 > collection is empty > add 
- переходим в правую рабочую зону и выбираем метод **GET**
- в строке URL добавляем `http://162.55.220.72:5005/get_method` 
- в области **Query Params** вводим:
     1. KEY = name, VALUE = dasha; 
    2. KEY = age, VALUE = 25 
- после ввода последних данных, в строке URL появляется следующее: `http://162.55.220.72:5005/get_method?name=dasha&age=int` 
- нажимаем Save > Send > Body (результат) 
``` python
 [
    "dasha",
    "25"
]
```
===================================================

``` python
EP_2
Method: POST
EndPoint: /user_info_3
request form data: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': age,
          'salary': salary,
          'family': {'children': [['Alex', 24], ['Kate', 12]],
                     'u_salary_1_5_year': salary * 4}}
```

- добавляем новую коллекцию под именем EP_2 
- collection is empty > add request
- переходим в правую рабочую зону и выбираем метод **POST**
- Body > form-data > в строке URL добавляем ` http://162.55.220.72:5005/user_info_3`
 
-  вводим переменные:
   1. KEY = name, VALUE = dasha; 
   2. KEY = age, VALUE = 25; 
   3. KEY = salary, VALUE = 500
-  нажимаем Save > нажимаем Send 
- Body:
```python  
{
    "age": "25",
    "family": {
        "children": [
            [
                "Alex",
                24
            ],
            [
                "Kate",
                12
            ]
        ],
        "u_salary_1_5_year": 2000
    },
    "name": "dasha",
    "salary": 500
}
```
====================================================


``` python 
EP_3
Method: GET
EndPoint: /object_info_1
request url params: 
 name: str
 age: int
 weight: int

response: 
{'name': name,
          'age': age,
          'daily_food': weight * 0.012,
          'daily_sleep': weight * 2.5}
 
```

- нажимаем Collection > new > ИМЯ КОЛЛЕКЦИИ: EP_3
- в меню нажимаем на коллекцию EP_3 > collection is empty > add request
- переходим в правую рабочую зону и выбираем метод **GET**> в строке URL добавляем `http://162.55.220.72:5005/object_info_1` 
-  в области **Query Params** вводим:
-   1. KEY = name, VALUE = dasha; 
-   2. KEY = age, VALUE = 25; 
-   3. KEY = weight, VALUE = 60 
- после ввода последних данных, в строке URL появляется следующее: `http://162.55.220.72:5005/object_info_1?name=dasha&age=25&weight=60` 
-  нажимаем Save > нажимаем Send 
- Body:

``` python
{
    "age": 25,
    "daily_food": 0.72,
    "daily_sleep": 150.0,
    "name": "dasha"
}
```

====================================================

``` python 
EP_4
Method: GET
EndPoint: /object_info_2
request url params: 
 name: str
 age: int
 salary: int

response: 
{'start_qa_salary': salary,
          'qa_salary_after_6_months': salary * 2,
          'qa_salary_after_12_months': salary * 2.7,
          'qa_salary_after_1.5_year': salary * 3.3,
          'qa_salary_after_3.5_years': salary * 3.8,
          'person': {'u_name': [user_name, salary, age],
                     'u_age': age,
                     'u_salary_5_years': salary * 4.2}
          }
```


- нажимаем Collection > new > ИМЯ КОЛЛЕКЦИИ: EP_4
-  в меню нажимаем на коллекцию EP_4 > collection is empty > add request 
-  переходим в правую рабочую зону и выбираем метод **GET**
-   в строке URL добавляем `http://162.55.220.72:5005/object_info_2`
-   в области **Query Params** вводим:
-    1. KEY = name, VALUE = dasha; 
-    2. KEY = salary, VALUE = 500 
-   после ввода последних данных, в строке URL появляется следующее: `http://162.55.220.72:5005/object_info_2?name=dasha&age=25&salary=500`  
-  нажимаем Save > нажимаем Send 
- Body:

``` python 

{
    "person": {
        "u_age": 25,
        "u_name": [
            "dasha",
            500,
            25
        ],
        "u_salary_5_years": 2100.0
    },
    "qa_salary_after_1.5_year": 1650.0,
    "qa_salary_after_12_months": 1350.0,
    "qa_salary_after_3.5_years": 1900.0,
    "qa_salary_after_6_months": 1000,
    "start_qa_salary": 500
}
```
====================================================

``` python 
EP_5
Method: GET
EndPoint: /object_info_3
request url params: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': age,
          'salary': salary,
          'family': {'children': [['Alex', 24], ['Kate', 12]],
                     'pets': {'cat':{'name':'Sunny',
                                     'age': 3},
                              'dog':{'name':'Luky',
                                     'age': 4}},
                     'u_salary_1_5_year': salary * 4}
          }
```

- нажимаем Collection > new > ИМЯ КОЛЛЕКЦИИ: EP_5
-  в меню нажимаем на коллекцию EP_5 > collection is empty > add request
-  переходим в правую рабочую зону и выбираем метод **GET**
-  в строке URL добавляем `http://162.55.220.72:5005/object_info_3` 
-  в области Query Params вводим 
-  1. KEY = name, VALUE = dasha; 
-  2. KEY = age, VALUE = 25; 
-  3. KEY = salary, VALUE = 500; 
-  4. KEY = family, VALUE = {'children': [['Alex', 24], ['Kate', 12]],
                     'pets': {'cat':{'name':'Sunny',
                                     'age': 3},
                              'dog':{'name':'Luky',
                                     'age': 4}},
                     'u_salary_1_5_year': salary * 4}
- после ввода последних данных, в строке URL появляется следующее: ` http://162.55.220.72:5005/object_info_3?name=dasha&age=25&salary=500&family={'children': [['Alex', 24], ['Kate', 12]],
                     'pets': {'cat':{'name':'Sunny',
                                     'age': 3},
                              'dog':{'name':'Luky',
                                     'age': 4}},
                     'u_salary_1_5_year': salary * 4}` 

 - нажимаем Save > нажимаем Send 
- Body:
``` python
{
    "age": "25",
    "family": {
        "children": [
            [
                "Alex",
                24
            ],
            [
                "Kate",
                12
            ]
        ],
        "pets": {
            "cat": {
                "age": 3,
                "name": "Sunny"
            },
            "dog": {
                "age": 4,
                "name": "Luky"
            }
        },
        "u_salary_1_5_year": 2000
    },
    "name": "dasha",
    "salary": 500
}
```
====================================================

``` python
EP_6
Method: GET
EndPoint: /object_info_4
request url params: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': int(age),
          'salary': [salary, str(salary * 2), str(salary * 3)]}


```

- нажимаем Collection > new > ИМЯ КОЛЛЕКЦИИ: EP_6
- в меню нажимаем на коллекцию EP_6 > collection is empty > add request
-  переходим в правую рабочую зону и выбираем метод **GET**
-   в строке URL добавляем `http://162.55.220.72:5005/object_info_4` 
-    в области **Query Params** вводим:
      1. KEY = name, VALUE = dasha; 
     2.  KEY = age, VALUE = 25; 
     3.   KEY = salary, VALUE = 500
-  после ввода последних данных, в строке URL появляется следующее: ` http://162.55.220.72:5005/object_info_4?name=dasha&age=25&salary=500`
- нажимаем Save > нажимаем Send 
- Body:
``` python
{
    "age": 25,
    "name": "dasha",
    "salary": [
        500,
        "1000",
        "1500"
    ]
}
```
====================================================
``` python
EP_7
Method: POST
EndPoint: /user_info_2
request form data: 
 name: str
 age: int
 salary: int

response: 
{'start_qa_salary': salary,
          'qa_salary_after_6_months': salary * 2,
          'qa_salary_after_12_months': salary * 2.7,
          'qa_salary_after_1.5_year': salary * 3.3,
          'qa_salary_after_3.5_years': salary * 3.8,
          'person': {'u_name': [user_name, salary, age],
                     'u_age': age,
                     'u_salary_5_years': salary * 4.2}
          }
```

- добавляем новую коллекцию под именем EP_6 
-  collection is empty > add request
-  переходим в правую рабочую зону и выбираем метод **POST** 
-   Body > form-data> в строке URL добавляем `http://162.55.220.72:5005/user_info_2` 
-   вводим:
    1. KEY = name, VALUE = dasha; 
    2.  KEY = age, VALUE = 25; 
    3.  KEY = salary, VALUE = 500 
- нажимаем Save > нажимаем Send 
- Body:

``` python 
{
    "person": {
        "u_age": 25,
        "u_name": [
            "dasha",
            500,
            25
        ],
        "u_salary_5_years": 2100.0
    },
    "qa_salary_after_1.5_year": 1650.0,
    "qa_salary_after_12_months": 1350.0,
    "qa_salary_after_3.5_years": 1900.0,
    "qa_salary_after_6_months": 1000,
    "start_qa_salary": 500
}  
``` 
