# Javascript Koans 오답노트

[javascript koans](<https://github.com/mrdavidlaing/javascript-koans>) 의 테스트 내용을 정리하였습니다. 

**답이 있기 때문에 풀고자 하시는 분들에게는 하단내용을 읽지마시고 뒤로가기를 해주시길 바랍니다.** 



## AboutObjects.js

### Array.prototype.join()

문제

```js
  it("should know properties that are functions act like methods", function () {
    var megalomaniac = {
      mastermind : "Brain",
      henchman: "Pinky",
      battleCry: function (noOfBrains) {
        return "They are " + this.henchman + " and the" +
          Array(noOfBrains + 1).join(" " + this.mastermind);
      }
    };

    var battleCry = megalomaniac.battleCry(4);
    expect(FILL_ME_IN).toMatch(battleCry);
  });
```



풀이

```js
var battleCry = megalomaniac.battleCry(4);
    expect(FILL_ME_IN).toMatch(battleCry);
megalomaniac.battleCr을 호츌했을 때 

return "They are " + this.henchman + " and the" +
          Array(noOfBrains + 1).join(" " + this.mastermind);

매개변수 4를 넣었다면 
return "They are Pinky and the" + Array(4+1).join(" "+"Brain");
가 됩니다.

Array(5).join(" brain");을 집중해보면 
console.log(Array(5)) //(5) [empty × 5] 가 뜹니다. length는 5

[empty × 5].join(" brain"); 에서 
.join의 역할은 join() 메서드는 배열의 모든 요소를 연결해 하나의 문자열로 만듭니다.(MDN출처) 

join까지 풀어써보자면 
empty+" brain"+empty+" brain"+empty+" brain"+empty+" brain"+empty 가 됩니다.
" brain  brain  brain  brain"이 됩니다.

Array(5) 를 넣어서 " brain"이 총 5번 반복될거 같지만 .join은 앞쪽인덱스와 뒷쪽 인덱스 사이에 들어가기 때문에 총 `4번`이 들어갑니다.

return 값은 
"They are Pinky and the brain  brain  brain  brain"
됩니다.
```



###  in 연산자

문제

```js
describe("'in' keyword", function () {
    var megalomaniac;
    beforeEach(function () {
      megalomaniac = {
        mastermind: "The Monarch",
        henchwoman: "Dr Girlfriend",
        theBomb: true
      };
    });

    it("should have the bomb", function () {

      var hasBomb = "theBomb" in megalomaniac;

      expect(hasBomb).toBe(FILL_ME_IN);
    });

    it("should not have the detonator however", function () {

      var hasDetonator = "theDetonator" in megalomaniac;

      expect(hasDetonator).toBe(FILL_ME_IN);
    });
  });
```



풀이

```js
in 연산자는 명시된 속성이 명시된 객체에 존재하면 true를 반환합니다. (출처: MDN)

문법 
속성 in 객체명
속성: 속성의 이름이나 배열의 인덱스를 뜻하는 문자열 또는 수 값입니다
객체명: 객체의 이름입니다.

var hasBomb = "theBomb" in megalomaniac;
megalomaniac 객체에 "theBomb" 속성이 포함되어 있는지를 뜻합니다.
theBomb: true 이 속성의 이름으로 포함되어 있기 때문에 `true`를 반환합니다.


```

