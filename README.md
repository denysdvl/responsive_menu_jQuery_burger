### This is an  Responsive burger menu <h2>
        
_You **can** combine this with your web project_

*This is a mini-project in which I implemented my menu burger with a screen size of 768px*

when clicking on the burger menu adds the menu-open class to the div
```javascript
	 (function ($) {
  $(function () {
    $(".icon").on('click',function () {
      $(this).closest('.menu').toggleClass('menu-open');
    });
  });
})(jQuery);
```

it's an icon drawn with a css 

```html
  <div class="icon">
        <span></span>
        <span></span>
        <span></span>
        <span></span>
    </div>
```

I prescribed our icon before opening the menu .

```css
	.icon span{
    display: block;
    position: absolute;
    height: 9px;
    width: 100%;
    background: #333333;
    border-radius: 9px;
    left: 0;
    transform: rotate(0deg);
    transition: 0.25s ease-in-out;
}

.icon span:nth-child(1){
top:0px;

}
.icon span:nth-child(2),.icon span:nth-child(3){
    top: 13px;
}
.icon span:nth-child(4){
    top: 26px;
}
```

icon with added menu-open class to div
```css
.menu.menu-open .icon span:nth-child(1){
    top: 18px;
    width: 0%;
    left: 50%;
}
.menu.menu-open .icon span:nth-child(2){
  transform: rotate(45deg);
}
.menu.menu-open .icon span:nth-child(3){
    transform: rotate(-45deg);
}
.menu.menu-open .icon span:nth-child(4){
    top: 18px;
    width: 0%;
    left: 50%;
}
```


