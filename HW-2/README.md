Jmeter_2 HW

1) http://162.55.220.72:5005/user_info
req. (RAW JSON)
POST
age: int
salary: int
name: str
auth_token


resp.
{'start_qa_salary':salary,
 'qa_salary_after_6_months': salary * 2,
 'qa_salary_after_12_months': salary * 2.9,
 'person': {'u_name':[user_name, salary, age],
                                'u_age':age,
                                'u_salary_1.5_year': salary * 4}
                                }

��������:
1) ������� �� Respose �������� �� ���� 'qa_salary_after_6_months' � �������� � ���� salary ������� http://162.55.220.72:5005/new_data
===================

2) http://162.55.220.72:5005/new_data
req.
POST
age: int
salary: int
name: str
auth_token

Resp.
{'name':name,
  'age': int(age),
  'salary': [salary, str(salary*2), str(salary*3)]}

��������:
1) ������� �� Respose �������� �� ���� 'name' � �������� � ���� name ������� http://162.55.220.72:5005/new_data

===================

3) http://162.55.220.72:5005/test_pet_info
req.
POST
age: int
weight: int
name: str
auth_token


===================

3) http://162.55.220.72:5005/get_test_user
req.
POST
age: int
salary: int
name: str
auth_token

Resp.
{'name': name,
 'age':age,
 'salary': salary,
 'family':{'children':[['Alex', 24],['Kate', 12]],
 'u_salary_1.5_year': salary * 4}
  }

�����:
������� ***
0) ������� ��� �������� Response Assertion.
1) ������� Assertion �� ��������� ������ ��� 200
2) ������� Assertion �� ��������� 'salary': salary