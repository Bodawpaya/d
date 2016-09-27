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
	
	var Button = React.createClass({
	  render: function() {
	    return (
	      <a className="btn btn-default">I am a button! Click me!</a>
	    );
	  }
	});

	React.render(<Button />, document.getElementById('content'));

**render** method ကေန HTML[or]XML ကို **return** ျပန္ေပးရပါတယ္<br>
*Note: element တစ္ခုထက္ပိုလာရင္ wrap လုပ္ေပးၿပီးမွ return ျပန္ဖို႕လိုပါတယ္*

**ဒီလိုမလုပ္ပါနဲ႕** - 

	return (
	  <div>Test</div>
	  <div>Test 2</div>
	)

**ဒီလိုလုပ္ပါ** - 

	return (
	  <div>
	    <div>Test</div>
	    <div>Test 2</div>
	  </div>
	);







