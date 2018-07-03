# jQuery to JavaScript Dictionary

## Selectors

### Accessing selectors

```js
$('*');                // wildcard (all)
$('#demo');            // id
$('.demo');            // class
$('p');                // tag
$('[type="text"]');    // attribute
$('h1:first-of-type'); // pseudo
$('p, div');           // multiple
$('.footer h1');       // descendent
```

```js
document.querySelector('#demo');
document.querySelector('.footer h1');
```

```js
document.querySelectorAll('*');
document.querySelectorAll('.demo');
document.querySelectorAll('p');
document.querySelectorAll('type="text"');
document.querySelectorAll('h1:first-of-type');
document.querySelectorAll('.footer h1');
```


### Accessing an id

```js
$('#example');
```

```js
document.getElementById('example');
```

### Accessing classes

```js
$('.example');
```

```js
const elements = document.getElementsByClassName('example');

for (let i = 0; i < element.length; i++) {
    elements[i];
}
```

### Accessing tags

```js
$('div');
```

```js
const elements = document.getElementsByTagName('div');

for (let i = 0; i < elements.length; i++) {
    elements[i];
}
```

# Find

```js
elements.querySelectorAll(selector);
```

## Classes

### Adding a class

```js
$('element').addClass('selected');
```

```js
element.classList.add('selected');
```

### Removing a class

```js
$('element').removeClass('selected');
```

```js
element.classList.remove('selected');
```

### Toggling a class

```js
$('element').toggleClass('selected');
```

```js
element.classList.toggle('selected');
```

### Getting a class

```js
$('element').hasClass('selected');
```

```js
element.classList.contains('selected');
```

## Styles

### Modifying CSS

```js
$('element').css('color', 'blue');
```

```js
element.style.color = 'blue';
```

## Attributes

### Geting attributes

```js
$('element').attr('href', 'index.html');
```

```js
element.getAttribute('href');
element.href;
```

### Setting attributes

```js
$('element').attr('href', 'index.html');
```

```js
element.setAttribute('href', 'index.html');
element.href = 'index.html';
```

## Traversing

### Parents

```js
$('element').parent();
```

```js
element.parentNode;
```

### Siblings

```js
$('element').siblings();
```

```js
// todo
```

### Children

```js
$('element').siblings();
```

```js
element.previousSibling;
element.nextSibling;
```

### Previous and Next

```js
$('element').prev();
$('element').next();
```

```js
element.previousSibling;
element.previousElementSibling;
element.nextSibling;
element.nextElementSibling;
```

```js
function getNextSiblings(el) {
    let siblings = [];
    while (el = el.nextSibling) { 
    	siblings.push(el); 
    }
    return siblings;
}
    
    let elements = getNextSiblings(el);
    
    elements.forEach(el => { 
    	// do something
    }); 
```

## Append HTML string

```js
$('element').append('<p>A paragraph</p>');
```

```js
element.innerHTML = '<p>A paragraph</p>';
```

## Append elements

```js
var body = document.body;
var p = document.createElement('p');
p.textContent = 'A paragraph';

body.appendChild(p);
```


## Event listeners

```js
$('element').on('click', function() { ... });
$('element').click(function() { ... });
```

```js
element.addEventListener('click', function() { ... });
```

## Modifying Text

```js
$('element').text('New text');
```

```js
element.textContent = 'New text';
```

## Looping

```js
var arr = ['tiger', 'cat', 'lion'];

$.each(arr, function(key, val) {
	$('ul').append('<li>' + key + ': ' + val + '</li>');
});
```

```js
const arr = ['tiger', 'cat', 'lion'];
const ul = document.querySelector('ul');
let li;

arr.forEach(function(value, index) {
	li = document.createElement('li');
	li.textContent = index + ': ' + value;
	ul.appendChild(li);
});
```

## Forms

```js
$('element').val();
```

```js
element.value;
```

## Effects

### Fade in/out

```js
$('element').fadeIn();
$('element').fadeOut();
```

```css
.element {
  visibility: visible;
  opacity: 1;
  transition: opacity .3s ease-in-out;
}

.fadein {
  visibility: hidden;
  opacity: 0;
  transition: visibility .3s, opacity .3s ease-in-out;
}
```

```js
element.classList.toggle('fadein');
```


"# jQuery-to-JavaScript" 
