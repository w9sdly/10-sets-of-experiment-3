# 10-sets-of-experiment-3
10 sets of Experiment 3

import java.io.Serializable;

/**
 * 员工实体类：存储企业员工基础信息
 * 实现Serializable接口，支持对象序列化存储
 */
public class Employee implements Serializable {
    private static final long serialVersionUID = 1L;

    private String empId;      // 员工编号（唯一）
    private String name;       // 姓名
    private String gender;     // 性别
    private int age;           // 年龄
    private String department; // 部门
    private String position;   // 职位
    private double salary;     // 薪资
    private String hireDate;   // 入职日期
    private String phone;      // 联系电话

    public Employee() {}

    public Employee(String empId, String name, String gender, int age, String department,
                    String position, double salary, String hireDate, String phone) {
        this.empId = empId;
        this.name = name;
        this.gender = gender;
        this.age = age;
        this.department = department;
        this.position = position;
        this.salary = salary;
        this.hireDate = hireDate;
        this.phone = phone;
    }

    // Getter & Setter
    public String getEmpId() { return empId; }
    public void setEmpId(String empId) { this.empId = empId; }
    public String getName() { return name; }
    public void setName(String name) { this.name = name; }
    public String getGender() { return gender; }
    public void setGender(String gender) { this.gender = gender; }
    public int getAge() { return age; }
    public void setAge(int age) { this.age = age; }
    public String getDepartment() { return department; }
    public void setDepartment(String department) { this.department = department; }
    public String getPosition() { return position; }
    public void setPosition(String position) { this.position = position; }
    public double getSalary() { return salary; }
    public void setSalary(double salary) { this.salary = salary; }
    public String getHireDate() { return hireDate; }
    public void setHireDate(String hireDate) { this.hireDate = hireDate; }
    public String getPhone() { return phone; }
    public void setPhone(String phone) { this.phone = phone; }

    @Override
    public String toString() {
        return "员工编号：" + empId +
               " | 姓名：" + name +
               " | 性别：" + gender +
               " | 年龄：" + age +
               " | 部门：" + department +
               " | 职位：" + position +
               " | 薪资：" + String.format("%.2f", salary) +
               " | 入职日期：" + hireDate +
               " | 电话：" + phone;
    }
}
