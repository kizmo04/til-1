# 객체 생성 패턴 3가지

* 리터럴(literal) 방식
* 함수 방식
* 프로토 타입

## 리터럴(literal) 방식

```js
var 인스턴스 = {
    프로퍼티1: 초깃값,
    프로퍼티2: 초깃값,
    
    메서드1: function(){
        
    },
    메서드2: function(){
        
    }
}
```

리터럴 방식에는 생성자가 존재하지 않는다.
객체를 정의함과 동시에 자동으로 인스턴스가 만들어진다.
인스턴스를 하나 이상 만들 수 없는 단점을 가진다. 
붕어빵 들이 있어도 두 개 이상 붕어빵을 만들 수 없다.. :fish:

> 재사용하기 위한 용도보다는 여러 개의 데이터를 묶어 값을 보관하거나 함수의 매개변수 값으로 전달할 때 주로 사용한다.

## 함수 방식

```js
function 클래스이름(){
    this.프로퍼티1 = 초깃값;
    this.프로퍼티2 = 초깃값;
    
    this.메서드 = function(){
        
    },
    this.메서드 = function(){
        
    }
}

var 인스턴스 = new 클래스 이름();
```

프로퍼티와 메서드는 반드시 자기 자신을 나타내는 this에 정의해야 한다.
생성자를 이용해 인스턴스를 만든다.

> 치명적인 단점이 있는데 인스턴스마다 내부의 모든 메서드가 독립적으로 만들어진다.

인스턴스가 여러개이고 그 메서드마다 독립적으로 만들어진다면 많은 코스트를 지불해야한다. 

## 프로토타입 방식

```js
function 클래스이름(){
    this.프로퍼티1 = 초깃값;
    this.프로퍼티2 = 초깃값;
}
클래스이름.prototype.메서드 = function(){};
클래스이름.prototype.메서드 = function(){};

var 인스턴스 = new 클래스 이름();
```

인스턴스끼리 메서드를 공유하는 구조다 
인스턴스가 생성되기 전에 이미 prototype에 메서드가 만들어져 있다. 