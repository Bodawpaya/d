# React

## Resources

- [OpenSoure Tutorials](https://github.com/vhf/free-programming-books/blob/master/javascript-frameworks-resources.md#react)


1. render

## React Component

	React Component မွာ view ပါမယ္ view ရဲ႕ logic ပါမယ္၊

## React JSX

JSX ဆိုတာ HTML/XML ကို JavaScript နဲ႕အလြယ္တကူေရးလို႕ရေအာင္
လုပ္ထားတဲ့ syntax တစ္ခုပဲ၊
Browser ထဲမွာ run ဖို႕ build tool ေတြကိုသံုးရမယ္
ေနာက္ပိုင္းမွာေရးထားပါတယ္
အခုေလာေလာဆယ္ေတာ့ မၾကည့္ပါနဲ႕ဦး
စိတ္ညစ္သြားမွာဆိုးလို႕

## React render()
	
Component တစ္ခုမွာ `render` method တစ္ခုပါပါတယ္
ဒီတိုင္းေလးစေရးပါမယ္ 

```js	
var Button = React.createClass({
  render: function() {
    return (
      <a className="btn btn-default">I am a button! Click me!</a>
    );
  }
});

ReactDOM.render(<Button />, document.getElementById('content'));
```

**render** method ကေန HTML[or]XML ကို **return** ျပန္ေပးရပါတယ္<br>
> Note: element တစ္ခုထက္ပိုလာရင္ wrap လုပ္ေပးၿပီးမွ return ျပန္ဖို႕လိုပါတယ္

**ဒီလိုမလုပ္ပါနဲ႕** - 

```js
return (
  <div>Test</div>
  <div>Test 2</div>
)
```

**ဒီလိုလုပ္ပါ** - 

```js
return (
  <div>
    <div>Test</div>
    <div>Test 2</div>
  </div>
);
```


## React Props

```jsx
var Parent = React.createClass({
   render: function() {
     return (
       <ul>
         <Child text="Hello" />
       </ul>
     )
   }
})

var Child = React.createClass({
  render: function() {
    return (
      <li>
        {this.props.text}
      </li>
    )
  }
})

ReactDOM.render(<Parent />, document.getElementById('content'))
```

Result >> 

```html
<div id="content">
	<ul data-reactid=".0">
		<li data-reactid=".0.0">Hello</li>
	</ul>
</div>
```

> Note: prop  ကို value မပါပဲ pass လုပ္ရင္ React က boolean prop အျဖစ္သတ္မွတ္ပါတယ္

```js
// Parent
return (
      <ChildComponent checked />
      )

// Child
componentDidMount() {
	console.log(this.props.checked)  
},
render() {
	return (
		<div />
	)
}

// Output
//=> true
```

- **{this.props.text}** ဆိုတာေလးက text ကို output ထုတ္ေပးပါတယ္၊
  "Hello" ဆိုတဲ့ string က Parent က်ေန child ကို pass ေပးလိုက္ပါတယ္
- **Child** Component ကသူ႕ရဲ႕ **props**(this.props) ကိုသူကိုယ္တိုင္ေျပာင္းလဲလို႕မရပါဘူး
 ေျပာင္းလဲခ်င္ရင္ Parent Component ကေနပဲျပန္ pass လုပ္ရပါမယ္<br>
 **[or]**<br>
 Parent ကေနပဲ pass လုပ္ၿပီးေျပာင္းလဲသင့္ပါတယ္။
 လြယ္ပါတယ္
 

## getDefaultProps()

အကယ္ေရြ႕ parent က pass လုပ္မထားရင္ default အျဖစ္ထားဖို႕ 
ေအာက္ကအတိုင္းေရးရပါမယ္

```js
var Parent = React.createClass({
   render: function() {
     return (
       <ul>
        <Child />
        <Child text="Override Text" />
       </ul>
     )
   }
})

var Child = React.createClass({
  getDefaultProps: function() {
    return {
      text: "Default Text"
    }
  },
  render: function() {
    return (
      <li>
        {this.props.text}
      </li>
    )
  }
})

ReactDOM.render(<Parent />, document.getElementById('content'))
```

Output Result >>

```html
<div id="content">
	<ul data-reactid=".0">
		<li data-reactid=".0.0">Default Text</li>
		<li data-reactid=".0.1">Override Text</li>
	</ul>
</div>
```

ပထမ တစ္ခုမွာ pass မလုပ္ဖူး။<br>
ဒုတိယတစ္ခုမွာ pass လုပ္တယ္ Override လုပ္လိုက္ပါတယ္၊<br>
လြယ္ပါတယ္။


## Props Validation(propTypes)

```js
var Parent = React.createClass({
   render: function() {
     return (
       <ul>
        <Child />
        <Child text="Override Text" />
         <Child text={false} />
       </ul>
     )
   }
})

var Child = React.createClass({
  propTypes: {
     text: React.PropTypes.string
  },
  getDefaultProps: function() {
    return {
      text: 'Default N/A'
    }
  },
  render: function() {
    return (
      <li>
        {this.props.text}
      </li>
    )
  }
})

ReactDOM.render(<Parent />, document.getElementById('content'))
```

props ကို validate လုပ္ခ်င္ရင္ propTypes မွာ သတ္မွတ္ေပးရပါတယ္။
validate လုပ္ထားရင္ react library ကို development version နဲ႕ခ်ိတ္ထားတယ္ဆိုရင္
console မွာ error ျပေပးပါတယ္
minify version နဲ႕ ခ်ိတ္ထားတယ္ ဆိုရင္ေတာ့ ျပမွာမဟုတ္ပါဘူး

အကယ္ေရြ႕ မျဖစ္မေနလိုအပ္တဲ့ require ျဖစ္တဲ့ props ဆိုရင္ေတာ့ ေနာက္မွာ isRequired
ဆိုတာေလ ထပ္ထည့္ေပးလိုက္ယံုပါပဲ

> Note: **props** တစ္ခုမွာ **isRequired** နဲ႕ validate လုပ္ထားတယ္ဆိုရင္ getDefaultProps မွာ<br>
> အဲဒီ prop ကို ျဖဳတ္ရပါမယ္၊<br>
> လိုအပ္တယ္ လို႕ ေၾကညာထားရင္ၿပီး default မွာလည္ပါေနရင္ ဘယ္အဓိပါယ္ရိွပါ့မလဲ 


[ဒီမွာ သြားၾကည့္ပါ ေသခ်ာေပါက္သြားၾကည့္ပါ](https://facebook.github.io/react/docs/reusable-components.html#prop-validation)

## children

မူလ Componentထဲမွာပါတဲ **Content/SubComponent** ေတြကို this.props.children
ကေန access လုပ္လို႕ရပါတယ္။

```js
var ParentComponent = React.createClass({
    render() {
        return (
            <ChildComponent>
              {this.props.children}
            </ChildComponent>
        );
    }
});

var ChildComponent = React.createClass({
    render() {
        return (
            <div>
              <h1>I am a header!</h1>
            </div>
        );
    }
});

ReactDOM.render(<ParentComponent />, document.getElementById('content'))
```

Output >>

``html
<div id="content">
    <div data-reactroot="">
        <h1>I am a header!</h1>
    </div>
</div>
```



