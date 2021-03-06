# 마크다운 사용법 

<br>

## The tooling
vscode 에서 [__Code Runner__](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one) 와 [__Markdown Preview Enhanced__](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced) 를 설치 

<br>
<br>

## Paragraphs and Text Decoration

### 이탤릭체 / 볼드체 / 취소선 사용하기
```
*텍스트*: 이탤릭체
cat is *cute*.  

**텍스트**: 볼드체
cat is real **cute**.  

***텍스트*** - 이탤릭&볼드체
cat is real ***cute***.  
```
cat is *cute*. <br>
cat is real **cute**. <br>
cat is real ***cute***.

<br>

```
 _텍스트_: 이탤릭체
cat is _cute_.

__텍스트__: 볼드체
cat is real __cute__. 

___텍스트___: 이탤릭&볼드체
cat is real ___cute___. 
```
cat is _cute_. <br>
cat is real __cute__. <br>
cat is real ___cute___. 

<br>

```
~~텍스트~~: 취소선
cat is ~~cute~~. 
```
cat is ~~cute~~.

<br>
<br>

## Headings in Markdown
### "#"을 이용해 heading을 나타낼 수 있다.
```
# heading 1

## heading 2

### heading 3

```
# heading 1

## heading 2

### heading 3

<br>

### =, -으로 heading을 나타낼 수 있다.
```
heading 1
========
heading 2
--------
```
heading 1
========
heading 2
-------
"#"을 이용하는 것을 추천한다.

<br>
<br>

## Links in Markdown

### 기본 링크 추가법
```
https://github.com/yami03 
<https://github.com/yami03> 로 표현
```
https://github.com/yami03 <br>
<https://github.com/yami03>

<br>

### 텍스트에 링크를 삽입할 경우
```
[My GitHub Account](https://github.com/yami03 "sla")
[텍스트](링크 "title")
```
[My GitHub Account](https://github.com/yami03 "sla")

<br>

### 링크 key value 값처럼 사용하기
```
[마크다운사용법][1] key value 값처럼 링크를 달 수 있다. 
[1]: https://guides.github.com/features/mastering-markdown/
[1]값은 원하는 텍스트를 넣을 수 있다. 
```
[마크다운사용법][1] key value 값처럼 링크를 달 수 있다. 

[1]: https://guides.github.com/features/mastering-markdown/

<br>
<br>

## Markdown Images

### 기본 이미지 추가법
```
![yami03](images/36615680.jpg "profile")
![alt](이미지 url "title")
!표는 이미지를 뜻한다.
```
![yami03](images/36615680.jpg "profile")

<br>

### 이미지 key value값처럼 사용하기
```
![yami03][profile]

[profile]: images/36615680.jpg
링크와 동일하게 key value로 쓸 수 있다.
```
![yami03][profile]

[profile]: images/36615680.jpg

<br>

### 링크도 같이 달 경우
```
[![yami03](https://avatars3.githubusercontent.com/u/36615680?s=460&v=4)](https://github.com/yami03)
[![alt](이미지링크)](이미지링크)
```
[![yami03](images/36615680.jpg)](https://github.com/yami03)

<br>

### 이미지태그 사용1
```
[<img src="images/36615680.jpg">](https://github.com/yami03)
[<img src="이미지링크">](링크)
```

<br>

### 이미지태그 사용2
```
<img src= "images/36615680.jpg" >
<style>
img{}
</ style>
```

<br>

### figure태그 figcaption태그 사용
```
<figure>
    <figcaption></figcaption>
</figure>  
```

<br>
<br>

## Lists — Ordered, Unorderd, Bullets and Nesting

### list - * 혹은 + 사용한다
```
* text1
* text2 
* text3 
```
* text1
* text2 
* text3

<br>

```
+ text1
+ text2 
+ text3
```
+ text1
+ text2 
+ text3

<br>

### 순서가 있는 리스트 
```
1. text1
2. text2
3. text3
```
1. text1
1. text2
1. text3
   
    숫자는 1을 쓰는걸 추천한다. 왜냐면 하나가 추가된다고 뒤에 숫자를 특별히 신경 쓸 필요가 없다.

<br>

### 들여쓰기
```
1. text1
    * 들여쓰기 가능
        + css 없이 가능
2. text
```
1. text1
    * 들여쓰기 가능
        + css 없이 가능
2. text

<br>
<br>

## Line Breaks, Horizontal Rules and BlockQuotes

### Line breaks
```
cat is cute<br>
cat really is.
```
cat is cute<br>
cat really is.

<br>

### Horizontal Rules
```
Something

---
텍스트와 붙여 쓰면 heading으로 인식
```

Something

---



<br>
<br>

## Block Quotes
```
Four stages of competence
>Unconscious incompetence
>
>Conscious incompetence
>
>Conscious competence
>
>Unconscious competence
```
Four stages of competence
>Unconscious incompetence
>
>Conscious incompetence
>
>Conscious competence
>
>Unconscious competence

<br>
<br>

## Code Blocks

### 들여쓰기로 코드블록 만들기
Here is my code:
```
    var x = 100;
    const cat1 = 'yami';
    코드를 들여쓰기 하면 자동으로 코드 블럭이 됩니다. 
```
    var x = 100;
    const cat1 = 'yami';

<br>

### 언어를 정의하고 써보자

    ```js(언어정의)
    var y = 50;
    const cat2 = gurumy;    
    ```

```js
var y = 50;
const cat2 = gurumy;
```

<br>

### 인라인에서도 사용하기
``` 
Hey did you try `var x = 100;`?
```
Hey did you try `var x = 100;`?

<br>

### 레드라인 / 블루라인
<pre>
```diff
var x = 100;
- var y = 200;
+ var y = 300;
```
</pre>

```diff
var x = 100;
- var y = 200;
+ var y = 300;
```

<br>
<br>

## Tables
```
|Cat's Name|Cat's Age|
|:---------|:--------|
|yami|8|
|gurumy|8|

이 부분은 text-align을 나타낸다. 
left 정렬
|:---------|
center 정렬
|:---------:|
right 정렬
|---------:|
```
|Cat's Name|Cat's Age|
|:---------|:--------|
|yami|8|
|gurumy|8|

<br>
<br>

## Github Treats
```
* [ ] Get MilK
* [x] Crack Eggs
* [ ] Cook Bacon
```
* [ ] Get MilK
* [x] Crack Eggs
* [ ] Cook Bacon

Github write 창에도 쓸 수 있다.