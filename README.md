##### 🚀 *CuteJavascript*: Concise JS guides, without the fluff. 🚀 ###
- ###### by @SummerTinio ######

# 🚀 *CuteJavascript*: the ‘this’ keyword in 258 words 🚀

## **In JS, we either use ⬛ *primitives* or { ⬛, ⬛, ⬛ } *objects***. 
- Other data types **are, or *inherit***, from either one of these. via ***prototypal*** inheritance, not *classical* inheritance.
- **Functions are also objects**, but with an invocable code property { 🆒, ⬛, ⬛ }. **Classes are also objects** { 🟦, 🟥, 🟧 }, and so are Arrays [ ⬛, ⬛, ⬛ ].
- ##### Prototypal Inheritance: Class, Function
  - ![Prototypal Inheritance: Class, Function](https://i.imgur.com/97f6dbZ.jpeg)
- ##### Prototypal Inheritance: Array
  - ![Prototypal Inheritance: Array](https://i.imgur.com/Ec8fCbn.jpeg)

## **Inside objects, 'this' refers to the object itself**. 
- { ⬛, ⬛, ⬛ console.log(this) } ▶ { ⬛, ⬛, ⬛ }
- **Inside Class constructors**, '**this**' refers to an **instance of that class** (i.e. the thing that it's constructing { 🆗, 🆘, 🆚 }).

## The value of 'this' also changes.
- **Depending on how deeply nested** you're using 'this' in an object. 
- but if you want to, **you can manipulate what 'this' refers to**, by using **.bind(), .call(), or .apply()**:

## .bind( ), .call( ), or .apply( )
- **.bind( )**
  - “bind” / “**force it to use**”
    - e.g. **this**.🆒 = **this**.🆒.bind(**this**) .. good 'ole Class Components ..
  - 🆒.bind(this) 
    - > "Whatever 'this' refers to at the lexical place you're sitting at. 😡That's what you should use *from now on* ok? 😌But I'm not invoking you yet." - you to your function
  - **for partial application of functions**
    - i.e. giving your function args for it to use *in the future*

- **to actually bind args *and* invoke your function,**
  - .call( )
    - C == Commas
    - 🆒.call(this, ⓤ, ®️)

  - .apply( )
    - A == Array
    - 🆒.apply(this, [ⓤ, ®️])

## **Inside a function**, **'this' === the object that owns that function**. 
- ### i.e. **It depends on the function's execution context**
- > Where th r u running me?? 😤 - your function

## **If the function doesn't belong to any object** 
- ### i.e. if it sits directly on the *global* execution context, 
- then **'this' === the *window* object if you're in a browser**. 
  - ##### 'this' when Running in the browser/client-side (Chrome)
  - !['this' when Running in the browser/client-side (Chrome)](https://i.imgur.com/VaSK2j4.jpeg)

- Or if you're not running it in a browser, then ‘this’ === whatever the global object is. 
- Inside a global function running in Node, 'this' === the 'global' object.
  - ##### 'this' when Running in Node (Debian WSL)
  - !['this' when Running in Node (Debian WSL)](https://i.imgur.com/O9rhIEv.jpeg)

When you realize that all things in JS are just a ⬛ primitive or an { ⬛,⬛,⬛ } object, it's a lot easier to 🧠remember what 'this' is.

✌️ Thanks for reading! 🐱‍🚀
> 🚀 ⓤ, ®️ 🆒 🚀
