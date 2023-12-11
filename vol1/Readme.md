# 팩토리 메서드
부모 클래스에서 객체들을 생성할 수 있는 인터페이스를 제공하지만, 자식 클래스들이 생성될 객체들의 유형을 변경할 수 있도록 하는 생성 패턴


> 예시
> 
![](https://refactoring.guru/images/patterns/diagrams/factory-method/solution1.png)

자식 클래스에서 팩토리 메서드를 오버라이딩하고 그 메서드에 의해 생성되는 제품들의 클래스를 변경


![](https://refactoring.guru/images/patterns/diagrams/factory-method/solution2-ko.png)

Ship과 Truck 클래스 모두 Transport 인터페이스를 구현하고, deliver() 메서드를 선언하지만 각 클래스에 다르게 구현

ex) 육로,해상
