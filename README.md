##### *CuteJavascript*: Tiny Guides that Pack a Punch ππ₯π₯ ###
- ###### by @SummerTinio β ######

# π *CuteJavascript*: the βthisβ keyword in 0.8 minutes π

## **In JS, we either use β¬ *primitives* or { β¬, β¬, β¬ } *objects***. 
- Other data types **are, or *inherit***, from either one of these. via ***prototypal*** inheritance, not *classical* inheritance.
- **Functions are also objects**, but with an invocable code property { π, β¬, β¬ }. 
- **Classes are also objects** { π¦, π₯, π§ }, and so are Arrays [ β¬, β¬, β¬ ].
- ##### Prototypal Inheritance: Class, Function
  - ![Prototypal Inheritance: Class, Function](https://i.imgur.com/97f6dbZ.jpeg)
- ##### Prototypal Inheritance: Array
  - ![Prototypal Inheritance: Array](https://i.imgur.com/Ec8fCbn.jpeg)

## **Inside objects, 'this' refers to the object itself**. 
- { β¬, β¬, β¬ console.log(this) } -> { β¬, β¬, β¬ }
- **Inside Class constructors**, '**this**' refers to an **instance of that class** 
- (i.e. from { π¦, π₯, π§ }-> the specific thing that it's constructing { π, π, π }).
- **The value of 'this' also changes** **depending on how deeply nested** you're using 'this' in an object. 

## **Inside a function**, **'this' === the object that owns that function**. 
- **It depends on the function's execution context**
- > Where th r u running me?? π€ - your function
- Are you running it from inside another Object? what data type is it? -- or, ...

## **If the function doesn't belong to any object** 
- i.e. If it sits directly on the *global* execution context, 
- then **'this' === the *window* object if you're in a browser**. 
  - ##### 'this' when inside a global function running in the browser/client-side (Chrome)
  - !['this' when inside a global function running in the browser/client-side (Chrome)](https://i.imgur.com/VaSK2j4.jpeg)

- Or if you're not running it in a browser, then βthisβ === whatever the global object is. 
- Inside a global function running in Node, 'this' === the 'global' object.
  - ##### 'this' when inside a global function running in Node (Debian WSL)
  - !['this' when inside a global function running in Node (Debian WSL)](https://i.imgur.com/O9rhIEv.jpeg)

- but if you want to, **you can manipulate what 'this' refers to**, by using **.bind(), .call(), or .apply()**:

## .bind( ), .call( ), or .apply( )
- **.bind( )**
  - βbindβ / β**force it to use**β
  - Inside a React ClassComponent's constructor, we can write: **this**.π = **this**.π.bind(**this**). 
    - and for that function, π, we've made sure that 'this' refers to an instance of that ClassComponent.
  - π.bind(this)
    - > "Whatever 'this' refers to at the lexical place you're sitting at. That's what you should use *from now on* ok? π‘ But I'm not invoking you yet. π" - you to your function
  - **for partial application of functions**
    - "partial" 'cause you haven't called _or applied_ it yet. 
    - i.e. giving your function args for it to use *in the future*
- **to actually bind args *and* invoke your function at the same time,**
  - .call( )
    - C == Commas
    - π.call(this, β€, Β?οΈ)
  - .apply( )
    - A == Array
    - π.apply(this, [β€, Β?οΈ])

## **How does method chaining relate to 'this'?**
- β¬οΈ.spherify().blueify().squigglify()
- β¬οΈ-> β«οΈ-> π΅-> π
- 'this' is whatever 'this' was, at the left of the dot.
- Chaining Object methods on methods on methods is possible since, after modifying βthis,β (β¬οΈ-> β«οΈ) each of those methods return βthis,β (β«οΈ) for the next method to consume. (β«οΈ-> π΅) .. return (π΅) .. then (π΅-> π) .. return (π) and so on. 
- It's like adding beads to a bracelet. Before you can add another bead, you gotta expose the thread inside it.


When you realize that all things in JS are just a β¬ primitive or an { β¬,β¬,β¬ } object, it's a lot easier to π§ remember what 'this' is.

βοΈ Thanks for reading! π±βπ
> π π β€ Β?οΈ π ππ 

## License & Copyright

All materials herein are Β© 2021 Summer Tinio.

This work is licensed under a [Creative Commons Attribution-NonCommercial-NoDerivs 4.0 Unported License.](https://creativecommons.org/licenses/by-nc-nd/4.0/)
