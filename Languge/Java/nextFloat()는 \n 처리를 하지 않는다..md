# nextFloat()는 \n 처리를 하지 않는다.
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
