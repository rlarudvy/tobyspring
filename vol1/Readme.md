# 팩토리 메서드
부모 클래스에서 객체들을 생성할 수 있는 인터페이스를 제공하지만, 자식 클래스들이 생성될 객체들의 유형을 변경할 수 있도록 하는 생성 패턴


> 예시
> 
![](https://refactoring.guru/images/patterns/diagrams/factory-method/solution1.png)

자식 클래스에서 팩토리 메서드를 오버라이딩하고 그 메서드에 의해 생성되는 제품들의 클래스를 변경


![](https://refactoring.guru/images/patterns/diagrams/factory-method/solution2-ko.png)

Ship과 Truck 클래스 모두 Transport 인터페이스를 구현하고, deliver() 메서드를 선언하지만 각 클래스에 다르게 구현

ex) 육로,해상

![](https://refactoring.guru/images/patterns/diagrams/factory-method/solution3-ko.png)

Road­Logistics​(도로 물류) 클래스에 포함된 팩토리 메서드는 Truck 객체들을 반환하는 반면 Sea­Logistics​(해운 물류) 클래스에 포함된 팩토리 메서드는 선박 객체들을 반환

- 팩토리 메서드를 사용하는 코드를 클라이언트 코드라고 부른다. 
- 클라이언트 코드는 다양한 자식 클래스들에서 실제로 반환되는 여러 제품 간의 차이에 대해 알지 못한다. 
- 클라이언트 코드는 모든 제품을 추상 Transport​(운송체계)​로 간주 한다. 
- 클라이언트는 모든 Transport 객체들이 deliver​(배달) 메서드를 가져야 한다는 사실을 알고 있지만, 이 메서드가 정확히 어떻게 작동하는지는 클라이언트에게 중요하지 않다.



## 전체 구조

![](https://refactoring.guru/images/patterns/diagrams/factory-method/structure.png)
