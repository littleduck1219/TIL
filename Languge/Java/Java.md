# nextFloat()는 \n 처리를 하지 않는다.
2023.05.28

![image](https://github.com/littleduck1219/TIL/assets/107936957/eda0e4d6-2dff-4b14-96c7-262c83a9fb09)
<p>
입력과는 다르게 출력이 한줄 씩 밀려나게되는 현상이 발생하였습니다.

그 이유는 nextFloat()메소드가 원인이였습니다. nextFloat() 메소드는 float 값을 읽지만 줄 바꿈 문자는 그대로 남겨둡니다. 그래서 그 다음에 호출되는 nextLine() 메소드는 이 줄 바꿈 문자를 읽고 바로 끝내버리게 됩니다. 이를 해결하기 위해서는 nextFloat() 호출 이후에 추가로 nextLine()를 한 번 더 호출해줘서 줄 바꿈 문자를 소비해야 합니다.
</p>

```java
public class W1home {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String title = sc.nextLine();
        float rate = sc.nextFloat();
        sc.nextLine();
        String recipe1 = sc.nextLine();
        String recipe2 = sc.nextLine();
        String recipe3 = sc.nextLine();
        String recipe4 = sc.nextLine();
        String recipe5 = sc.nextLine();

        double rate1 = (int)rate;
        System.out.println("[" + title + "]");
        System.out.println("별점 : " +  rate + "(" + rate1 * 100 / 5 + "%)");
        System.out.println("1." + recipe1);
        System.out.println("2." + recipe2);
        System.out.println("3." + recipe3);
        System.out.println("4." + recipe4);
        System.out.println("5." + recipe5);
    }
}
```
![image](https://github.com/littleduck1219/TIL/assets/107936957/c02d6c02-08ba-460f-934c-8346090b6aa9)


# Python을 배운 후 Java
2023.05.29

Java를 배우면서 Python과 너무 달라 찾아보았습니다.

1. 타입 시스템: Java는 정적 타입 언어로, 변수를 선언할 때 그 변수의 타입을 명시해야 합니다. 반면 Python은 동적 타입 언어로, 변수의 타입을 선언하지 않아도 됩니다. Java에서는 변수의 타입이 한번 정해지면 변경할 수 없으므로, 타입에 대한 이해와 그에 따른 코드 작성이 중요합니다.

2. 객체 지향 프로그래밍: Java는 객체 지향 프로그래밍(Object-Oriented Programming, OOP)에 초점을 맞춘 언어입니다. 모든 것이 클래스와 객체로 표현되며, 상속, 캡슐화, 다형성 등의 개념이 중요하게 다뤄집니다. Python도 객체 지향 언어지만, 절차 지향적인 프로그래밍도 가능하므로 Python으로부터 Java를 배울 때는 OOP에 대한 이해를 깊게 하는 것이 중요합니다.

3. 구문: Java의 구문은 Python보다 복잡합니다. Java는 세미콜론(`;`)으로 문장을 종료하고, 중괄호(`{}`)로 코드 블록을 구분합니다. Python에서는 이런 것들이 없으므로, Java를 배울 때는 구문에 주의해야 합니다.

4. 표준 라이브러리와 프레임워크: Java는 풍부한 표준 라이브러리와 다양한 프레임워크(Spring, Hibernate 등)를 제공합니다. 이들을 이해하고 활용하는 것은 Java를 효과적으로 사용하는 데 중요합니다.

5. 메모리 관리: Java는 가비지 컬렉터를 통해 메모리 관리를 자동으로 수행합니다. Python도 가비지 컬렉션을 사용하지만, Java에서는 이에 대해 더 자세히 알아야 할 수 있습니다. 특히, 대규모 애플리케이션에서 성능을 최적화하려면 가비지 컬렉션의 동작 방식을 이해하는 것이 중요합니다.

