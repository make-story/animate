# 에디터 (Editor)

> 실행예제
http://makeapi.net/test/animate.html  
  
-----
  
api.animate.frame({})
- requestAnimationFrame 애니메이션 리스트 실행

````javascript
// 단일 실행
api.animate.frame({
	'element': '.h2', 
	'style': {
		'left': '100px', 
		'top': '100px', 
		'width': '100px', 
		'height': '100px'
	}, 
	'duration': 3
});

// 여러개 실행
api.animate.frame([
{
	'element': api.dom('#h2'), 
	'style': {
		'left': '100px', 
		'top': '100px'
	}, 
	'duration': 3, 
	'complete': function() {  }
}, 
{
	'element': api.dom('#h2'), 
	'style': {
		'left': '200px', 
		'top': '200px'
	}, 
	'duration': 3, 
	'complete': function() {  }
}
]);
````

api.animate.transition({})
- 트랜지션 리스트 실행

````javascript
// 단일 실행
api.animate.transition({
	'element': api.dom('#view'), 
	'style': {
		'left': '100px', 
		'top': '100px'
	}, 
	'duration': 3
});

// 여러개 실행
api.animate.transition([
{
	'element': api.dom('#view'), 
	'style': {
		'left': '100px', 
		'top': '100px'
	}, 
	'duration': 3, 
	'complete': function() { }
},
{
	'element': api.dom('#view'), 
	'style': {
		'left': '200px', 
		'top': '200px'
	}, 
	'duration': 3, 
	'complete': function() { }
} 
]);
````

api.animate.animation({})
- 애니메이션 리스트 실행 (class 값으로 제어)

```javascript
// 단일 실행
api.animate.animation({
	'element': api.dom('#view'), 
	'class': 'pt-page-moveToLeft', 
	'complete': function() { }
});

// 여러개 실행
api.animate.animation([
{
	'element': api.dom('#view'), 
	'class': 'pt-page-moveToRight'
}, 
{
	'element': api.dom('#list'), 
	'class': 'pt-page-moveToRight'}
]);
```
