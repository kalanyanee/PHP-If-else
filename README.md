---
description: กาลัญญาณี อมรเวชกุล 630710125
---

# If-else-elseif: If-else

ในหัวข้อนี้ มีหัวข้อหลักๆ 2 หัวข้อนะคะ

* If-else
* If-elseif-else

เรามากันที่หัวข้อ if-else กันนะคะ&#x20;

## If-else

&#x20;    If….else คือ การทำงานไม่ว่าเงื่อนไขจะเป็นจริงหรือเท็จ if ทำงานเมื่อเงื่อนไขเป็นจริง และ else จะถูกทำงานเงื่อนไขเป็นเท็จ

### Syntax:

```php
  if( เงื่อนไข ){
       // คำสั่งที่ให้ทำงาน เมื่อเงื่อนไขถูกต้อง
    }else {
       // ถ้าในเงื่อนไข if ไม่ถูกต้อง จะทำคำสั่งใน else
    }
```

### **Flowchart:**

<figure><img src=".gitbook/assets/image (6).png" alt="" width="446"><figcaption><p> </p></figcaption></figure>

#### อธิบาย f**lowchart ของการทำงานของ if-else**

#### ขั้นแรก ตรวจสอบว่าเงื่อนไขเป็น True หรือ False

* ถ้าเป็น True ทำงานต่อไปที่ If code&#x20;
* หากเป็น False ทำงานต่อไปที่ else code

ทำงานใน If code หรือ else code เสร็จแล้ว จะทำงานต่อไปที่ After If&#x20;

เมื่อทำงานที่ After If เสร็จแล้วก็เป็นการจบการทำงานใน Flowchart if-else

### ตัวอย่างโค้ด

```php
<?php
$score = 65;
if ($score >= 50) {
    echo "You passed the exam!";
} else {
    echo "You failed the exam!";
}
?>
```

<details>

<summary>Output:</summary>

You passed the exam!

</details>

#### <mark style="color:blue;">อธิบายโค้ด</mark>

กำหนดตัวแปร $score = 65

เช็คเงื่อนไขใน if

$score ถ้ามีค่ามากกว่าหรือเท่ากับ 50 หรือไม่

&#x20;    ถ้า $score มีค่ามากกว่าหรือเท่ากับ 50 แสดงว่าเงื่อนไขเป็นจริง

&#x20;         แสดงข้อความว่า You passed the exam!

&#x20;    ถ้า $score มีค่าน้อยกว่า 50 แสดงว่าเงื่อนไขเป็นเท็จ&#x20;

&#x20;         ทำงานที่ else แล้ว แสดงข้อความว่า You failed the exam!

ในตัวอย่างนี้ $score = 65 แปลว่าเงื่อนไขเป็นจริง แสดงOutput : You passed the exam!

## คำสั่ง if-else แบบย่อ

* #### ใช้ สัญลักษณ์ <mark style="background-color:red;">? :</mark> &#x20;

### Syntax if-else แบบย่อ:

```php
$ตัวแปร = (เงื่อนไข) ? (คำสั่ง1) : (คำสั่ง2); 
```

* คำสั่ง 1 : คำสั่งที่จะถูกดำเนินการหากเงื่อนไขเป็นจริง
* คำสั่ง2 : คำสั่งที่จะถูกดำเนินการหากเงื่อนไขเป็นเท็จ

### ตัวอย่าง if-else แบบย่อ:

```php
<?php
$y = 100;
$x = ($y>=80) ? “ผ่าน” : “ไม่ผ่าน”;
echo $x; 
?>
```

<details>

<summary>Output:</summary>

ผ่าน

</details>

#### <mark style="color:blue;">อธิบายโค้ด</mark>

กำหนดตัวแปร $y = 100

ตรวจสอบเงื่อนไข $y มีค่ามากกว่าหรือเท่ากับ 80 หรือไม่

ถ้า $y มีค่ามากกว่าหรือเท่ากับ 80 เงื่อนไขเป็นจริง ให้ค่า ผ่าน

ถ้า  $y มีค่าน้อยกว่า 80 เงื่อไขเป็นเท็จ ให้ค่า ไม่ผ่าน กับตัวแปร x

ในตัวอย่างนี้  $y มีค่าเป็น 100 มากกว่า 80 แสดงว่าเงื่อนไขเป็นจริง ให้ค่า ผ่าน กับตัวแปล x

แสดงตัวแปร x  ออกมา Output: ผ่าน

### ตัวอย่างเพิ่มเติม:

เป็นเดียวกับตัวอย่างif-else แบบปกติ มาทำให้เป็นแบบย่อ

```php
<?php
$score = 65;
echo ($score >=50) ? "You passed the exam!" : "You failed the exam!";
?>
```

### เปรียบเทียบโค้ดภาษา PHP,Java,C,Python,JavaScipt

{% tabs %}
{% tab title="PHP" %}
```php
<?php
$number = 7;
if ($number % 2 == 0) {
    echo "$number is an even number.";
} else {
    echo "$number is an odd number.";
}
?>
```
{% endtab %}

{% tab title="Java" %}
```java
public class Main {
    public static void main(String[] args) {
        int number = 7;
        if (number % 2 == 0) {
            System.out.println(number + " is an even number.");
        } else {
            System.out.println(number + " is an odd number.");
        }
    }
}
```
{% endtab %}

{% tab title="C" %}
```c
#include <stdio.h>
int main() {
    int number = 7;
    if (number % 2 == 0) {
        printf("%d is an even number.\n", number);
    } else {
        printf("%d is an odd number.\n", number);
    }
}
```
{% endtab %}

{% tab title="Python" %}
```python
number = 7
if number % 2 == 0:
    print(f"{number} is an even number.")
else:
    print(f"{number} is an odd number.")
```
{% endtab %}

{% tab title="JavaScipt" %}
```javascript
let number = 7;

if (number % 2 === 0) {
    console.log(`${number} is an even number.`);
} else {
    console.log(`${number} is an odd number.`);
}
```
{% endtab %}
{% endtabs %}

<details>

<summary>Output:</summary>

7 is an odd number.

</details>

จบหัวข้อif-elseแล้วค่ะ

***

มาทำความเข้าใจกันต่อที่หัวข้อถัดไป if-elseif-else นะคะ

## If-elseif-else

elseif คือ ดำเนินการเงื่อนไขมากกว่า2 เงื่อนไข การนำelseif มาแทรกระหว่าง if กับ else ทำงานคล้ายคลึงกับ else คือเงื่อนไข if เป็นเท็จ จะทำงานที่ elseif มีข้อแตกต่างจาก else ตรงที่ elseif ต้องมีเงื่อนไขที่เป็นจริงเท่านั้น

### Syntax:

```php
if(เงื่อนไข 1 ){
   //คำสั่งจะให้ทำงาน เมื่อเงื่อนไข1 เป็นจริง
} else if(เงื่อนไข 2){  
   //คำสั่งจะดำเนินการหากเงื่อนไข 1 เป็นเท็จและเงื่อนไขนี้เป็นจริง
} …… 
}else{
   //คำสั่งจะดำเนินการหากเงื่อนไขที่กำหนดทั้งหมดเป็นเท็จ
}
```

### Flowchart:

<figure><img src=".gitbook/assets/image (1).png" alt="" width="563"><figcaption></figcaption></figure>

#### อธิบาย f**lowchart ของการทำงานของ if-elseif-else**

#### ตรวจสอบเงื่อนไขแรก(Condition-1) : เป็น True หรือ False&#x20;

* ถ้าเป็น True ทำงานต่อไปที่ Statement-1 แล้วจบการทำงาน
* ถ้าเป็น False ทำงานเงื่อนไขถัดไป

ตรวจสอบเงื่อนไขถัดไป(Condition-2): เงื่อนไขแรกเป็น False ทำการตรวจสอบที่ เงื่อนไขที่สอง (Condition-2) เป็น True หรือ False

* ถ้าเป็น True ทำงานต่อไปที่ Statement-2 แล้วจบการทำงาน
* ถ้าเป็น False ทำงานเงื่อนไขถัดไป

ตรวจสอบเงื่อนไขถัดไป(Condition-n): เงื่อนไข2เป็น False ทำการตรวจสอบเงื่อนไขตามลำดับไปเรื่อยๆ จนกว่าจะพบเงื่อนไขที่เป็นจริง หรือจนถึงเงื่อนไขสุดท้าย

ถ้าตรวจสอบทุกเงื่อนไข พบว่าไม่มีเงื่อนไขไหนเป็นจริงเลย: จะทำงานไปยังคำสั่ง Next Statement

### ตัวอย่างโค้ด

```php
<?php  
    $calories = 600;
    if ($calories > 800) {    
        echo "This is a high-calorie.";    
    }elseif($calories >= 500) {    
        echo "This is a medium-calorie.";    
    }($calories >= 200) {    
        echo "This is a low-calorie.";    
    }else{
        echo "This is a very low-calorie.";     
    }
?>
```

<details>

<summary>Output:</summary>

This is a medium-calorie.

</details>

#### <mark style="color:blue;">อธิบายโค้ด</mark>

กำหนดตัวแปร $calories = 600&#x20;

ตรวจสอบเงื่อนไขif $calories มีค่ามากกว่า 800 หรือไม่

&#x20;    ถ้า $calories มีค่ามากกว่า 800 เงื่อนไขเป็นจริง แสดงข้อความ This is a high-calorie.

&#x20;    ถ้า $calories น้อยกว่า 800 เงื่อนไขเป็นเท็จ ตรวจสอบเงื่อนไขที่ elseif&#x20;

ตรวจสอบเงื่อนไข elseif เช็คว่า  $calories มากกว่าหรือเท่ากับ 500 หรือไม่&#x20;

&#x20;    ถ้า $calories มีค่ามากกว่าเท่ากับ 500 แสดงข้อความ This is a medium-calorie.

เนื่องจาก $calories ในตัวอย่างคือ 600 เข้าเงื่อนไข elseif นี้ Output: This is a medium-calorie.&#x20;

แล้วก็หยุดการทำงาน ไม่เข้าเงื่อนไขต่อไป เพราะเจอเงื่อนไขที่เป็นจริงแล้ว

### เปรียบเทียบภาษา PHP,Java,C,Python,JavaScipt

{% tabs %}
{% tab title="PHP" %}
```php

<?php  
    $score = 75;
    if ($score >= 80) {    
        $grade = "A";    
    }    
    else if ($score >= 70 && $score < 80) {    
        $grade = "B";    
    }    
    else if ($score >= 60 && $score < 70) {    
        $grade = "C";   
    }    
    else if ($score >= 50 && $score < 60) {    
        $grade = "D";   
    }  
    else {    
        $grade = "F";    
    }    
    echo "คะแนนที่ได้คือ {$score}<br>";
    echo "เกรดที่ได้คือ {$grade}";  
?>
```
{% endtab %}

{% tab title="Java" %}
```java
public class GradeCalculator {
    public static void main(String[] args) {
        int score = 75;
        String grade;

        if (score >= 80) {
            grade = "A";
        } else if (score >= 70) {
            grade = "B";
        } else if (score >= 60) {
            grade = "C";
        } else if (score >= 50) {
            grade = "D";
        } else {
            grade = "F";
        }

        System.out.println("คะแนนที่ได้คือ " + score \n "เกรดที่ได้คือ " + grade);
        System.out.println("เกรดที่ได้คือ " + grade);
    }
}
```
{% endtab %}

{% tab title="C" %}
```c
#include <stdio.h>
int main() {
    int score = 75;
    char *grade;
    if (score >= 80) {
        grade = "A";
    } else if (score >= 70) {
        grade = "B";
    } else if (score >= 60) {
        grade = "C";
    } else if (score >= 50) {
        grade = "D";
    } else {
        grade = "F";
    }
    printf("คะแนนที่ได้คือ %d\n", score);
    printf("เกรดที่ได้คือ %s\n", grade);
}
```
{% endtab %}

{% tab title="Python" %}
```python
score = 75
if score >= 80:
    grade = "A"
elif score >= 70:
    grade = "B"
elif score >= 60:
    grade = "C"
elif score >= 50:
    grade = "D"
else:
    grade = "F"

print(f"คะแนนที่ได้คือ {score}")
print(f"เกรดที่ได้คือ {grade}")
```
{% endtab %}

{% tab title="JavaScipt" %}
```javascript
let score = 75;
let grade;

if (score >= 80) {
    grade = "A";
} else if (score >= 70 && score < 80) {
    grade = "B";
} else if (score >= 60 && score < 70) {
    grade = "C";
} else if (score >= 50 && score < 60) {
    grade = "D";
} else {
    grade = "F";
}

console.log("คะแนนที่ได้คือ " + score);
console.log("เกรดที่ได้คือ " + grade);
```
{% endtab %}
{% endtabs %}

<details>

<summary>Output :</summary>

คะแนนที่ได้คือ 75

เกรดที่ได้คือ B

</details>

### ความแตกต่างภาษา PHP,Java,C,Python,JavaScipt

**ความเหมือน**: if-else และ if-elseif-else ทุกภาษาใช้โครงสร้างพื้นฐานเดียวกัน

**ความแตกต่าง :**

1. ประกาศตัวแปรและการใช้วงเล็บ{}เหมือนกัน แตกต่างออกไปภาษาPython ใช้ ย่อหน้า(indentation) แทน
2. แสดงผลลัพธ์แต่ละภาษามีรูปแบบที่แตกต่างกัน

* **PHP**: ใช้ <mark style="background-color:yellow;">echo</mark>&#x20;
* **Java**: ใช้  <mark style="background-color:yellow;">System.out.println</mark>&#x20;
* **C**: ใช้  <mark style="background-color:yellow;">printf</mark>&#x20;
* **Python**: ใช้ <mark style="background-color:yellow;">print</mark>
* **JavaScript**: ใช้ <mark style="background-color:yellow;">console.log</mark>

3. Python มีลักษณะที่อ่านง่าย สบายตา

### ตรางการเปรียบเทียบเพิ่มเติมภาษา PHP,Java,C,Python,JavaScipt

<figure><img src=".gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

**จุดเด่นของ PHP:**

1. การใช้ if-else และ if-elseif-else ไม่แตกต่างจากภาษา Java,C มาก ทำให้ผู้ที่กำลังศึกษาเข้าใจง่าย
2. ใช้สร้างเว็บแอปพลิเคชัน ทำงานบนServer
3. มีการใช้ if-else แบบย่อ ช่วยให้โค้ดกระชับมากขึ้น

จบการอธิบายส่วนของ if-else กับ if-elseif-else ของ PHP ขอบคุณค่ะ

***

### Slide:

{% file src=".gitbook/assets/Control Flows  If-else.pdf" %}

## Video:

{% embed url="https://www.youtube.com/watch?v=YIQ9Yx4VKfY" %}

### Reference:

PHP:

* GeeksforGeeks. ( 2024). _Difference Between try-catch and if-else Statements in PHP_. Retrieved from GeeksforGeeks: [https://www.geeksforgeeks.org/difference-between-try-catch-and-if-else-statements-in-php/?ref=header\_outind](https://www.geeksforgeeks.org/difference-between-try-catch-and-if-else-statements-in-php/?ref=header\_outind)
* &#x20;GeeksforGeeks. (2024). _PHP Ternary Operator_. Retrieved from GeeksforGeeks: [https://www.geeksforgeeks.org/php-ternary-operator/  ](https://www.geeksforgeeks.org/php-ternary-operator/)
* Group, P. D. ( 2024). _elseif_. Retrieved from PHP.net: [https://www.php.net/manual/en/control-structures.elseif.php](https://www.php.net/manual/en/control-structures.elseif.php)
* Javatpoint. (2024). _PHP if-else Statement_. Retrieved from Javatpoint: [https://www.javatpoint.com/php-if-else](https://www.javatpoint.com/php-if-else)
* TutorialsPoint. (2024). _PHP if...else Statement_. Retrieved from TutorialsPoint: [https://www.tutorialspoint.com/php/php\_if\_else\_statement.htm](https://www.tutorialspoint.com/php/php\_if\_else\_statement.htm)
* W3Schools. (2024). _JavaScript if else and else if_. Retrieved from W3Schools: [https://www.w3schools.com/js/js\_if\_else.asp](https://www.w3schools.com/js/js\_if\_else.asp)
* W3Schools. (2024, October 11). _PHP If...Else...Elseif Statements_. Retrieved from W3Schools: [https://www.w3schools.com/php/php\_if\_nested.asp](https://www.w3schools.com/php/php\_if\_nested.asp)
