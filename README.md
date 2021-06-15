##### *CuteJavascript*: Tiny Guides that Pack a Punch 👊💥💥 ###
- ###### by @SummerTinio ✌ ######

# 🚀 *CuteJavascript*: the ‘this’ keyword in 0.8 minutes 🚀

## **In JS, we either use ⬛ *primitives* or { ⬛, ⬛, ⬛ } *objects***. 
- Other data types **are, or *inherit***, from either one of these. via ***prototypal*** inheritance, not *classical* inheritance.
- **Functions are also objects**, but with an invocable code property { 🆒, ⬛, ⬛ }. 
- **Classes are also objects** { 🟦, 🟥, 🟧 }, and so are Arrays [ ⬛, ⬛, ⬛ ].
- ##### Prototypal Inheritance: Class, Function
  - ![Prototypal Inheritance: Class, Function](https://i.imgur.com/97f6dbZ.jpeg)
- ##### Prototypal Inheritance: Array
  - ![Prototypal Inheritance: Array](https://i.imgur.com/Ec8fCbn.jpeg)

## **Inside objects, 'this' refers to the object itself**. 
- { ⬛, ⬛, ⬛ console.log(this) } -> { ⬛, ⬛, ⬛ }
- **Inside Class constructors**, '**this**' refers to an **instance of that class** 
- (i.e. from { 🟦, 🟥, 🟧 }-> the specific thing that it's constructing { 🆗, 🆘, 🆚 }).
- **The value of 'this' also changes** **depending on how deeply nested** you're using 'this' in an object. 

## **Inside a function**, **'this' === the object that owns that function**. 
- **It depends on the function's execution context**
- > Where th r u running me?? 😤 - your function
- Are you running it from inside another Object? what data type is it? -- or, ...

## **If the function doesn't belong to any object** 
- i.e. If it sits directly on the *global* execution context, 
- then **'this' === the *window* object if you're in a browser**. 
  - ##### 'this' when inside a global function running in the browser/client-side (Chrome)
  - !['this' when inside a global function running in the browser/client-side (Chrome)](https://i.imgur.com/VaSK2j4.jpeg)

- Or if you're not running it in a browser, then ‘this’ === whatever the global object is. 
- Inside a global function running in Node, 'this' === the 'global' object.
  - ##### 'this' when inside a global function running in Node (Debian WSL)
  - !['this' when inside a global function running in Node (Debian WSL)](https://i.imgur.com/O9rhIEv.jpeg)

- but if you want to, **you can manipulate what 'this' refers to**, by using **.bind(), .call(), or .apply()**:

## .bind( ), .call( ), or .apply( )
- **.bind( )**
  - “bind” / “**force it to use**”
  - Inside a React ClassComponent's constructor, we can write: **this**.🆒 = **this**.🆒.bind(**this**). 
    - and for that function, 🆒, we've made sure that 'this' refers to an instance of that ClassComponent.
  - 🆒.bind(this)
    - > "Whatever 'this' refers to at the lexical place you're sitting at. That's what you should use *from now on* ok? 😡 But I'm not invoking you yet. 😌" - you to your function
  - **for partial application of functions**
    - "partial" 'cause you haven't called _or applied_ it yet. 
    - i.e. giving your function args for it to use *in the future*
- **to actually bind args *and* invoke your function at the same time,**
  - .call( )
    - C == Commas
    - 🆒.call(this, ⓤ, ®️)
  - .apply( )
    - A == Array
    - 🆒.apply(this, [ⓤ, ®️])

## **How does method chaining relate to 'this'?**
- ⬛️.spherify().blueify().squigglify()
- ⬛️-> ⚫️-> 🔵-> 🌀
- Chaining Object methods on methods on methods is possible since, after modifying ‘this,’ (⬛️-> ⚫️) each of those methods return ‘this,’ (⚫️) for the next method to consume. (⚫️-> 🔵) .. return (🔵) .. then (🔵-> 🌀) .. return (🌀) and so on.

When you realize that all things in JS are just a ⬛ primitive or an { ⬛,⬛,⬛ } object, it's a lot easier to 🧠remember what 'this' is.

✌️ Thanks for reading! 🐱‍🚀
> 🌠🚀 ⓤ ®️ 🆒 🚀🌠

## License & Copyright

All materials herein are © 2021 Summer Tinio.

This work is licensed under a [Creative Commons Attribution-NonCommercial-NoDerivs 4.0 Unported License.](https://creativecommons.org/licenses/by-nc-nd/4.0/)
