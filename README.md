def get_employee_details():
    name = input("Enter Employee Name: ")
    emp_id = input("Enter Employee ID: ")
    department = input("Enter Department: ")
    basic_salary = float(input("Enter Basic Salary: "))
    return name, emp_id, department, basic_salary
def calculate_salary(basic_salary):
    hra = basic_salary * 0.20    
    da = basic_salary * 0.10     
    pf = basic_salary * 0.12     
    gross_salary = basic_salary + hra + da
    net_salary = gross_salary - pf
    return hra, da, pf, gross_salary, net_salary
def print_salary_slip(name, emp_id, department, basic, hra, da, pf, gross, net):
    print("\n============== EMPLOYEE SALARY SLIP ==============")
    print("Employee Name   :", name)
    print("Employee ID     :", emp_id)
    print("Department      :", department)
    print("-----------------------------------------------")
    print("Basic Salary    : Rs.", basic)
    print("HRA (20%)       : Rs.", hra)
    print("DA (10%)        : Rs.", da)
    print("PF Deduction    : Rs.", pf)
    print("-----------------------------------------------")
    print("Gross Salary    : Rs.", gross)
    print("Net Salary      : Rs.", net)
    print("================================================")
name,emp_id,department,basic=get_employee_details()
hra,da,pf,gross,net=calculate_salary(basic)
print_salary_slip(name,emp_id,department,basic,hra,da,pf,gross,net)

OUTPUT:
Enter Employee Name: priya
Enter Employee ID: 101
Enter Department: software engineer
Enter Basic Salary: 60000

============== EMPLOYEE SALARY SLIP ==============
Employee Name   : priya
Employee ID     : 101
Department      : software engineer
-----------------------------------------------
Basic Salary    : Rs. 60000.0
HRA (20%)       : Rs. 12000.0
DA (10%)        : Rs. 6000.0
PF Deduction    : Rs. 7200.0
-----------------------------------------------
Gross Salary    : Rs. 78000.0
Net Salary      : Rs. 70800.0
================================================
