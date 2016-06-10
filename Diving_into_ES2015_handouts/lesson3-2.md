The Basics

Let's explore Block Scope Variables, shall we?Block scoped variables are simply variables that are local to the blockin which they were defined.Let's explore this a bit with a few code samples.If we were just to use 'var' to declare a variable in this following snippet,everything would work just fine.But let's say we use 'let' to declare that variable instead.This is a subtle difference but an important one.
Nested Scopes

This really helps to keep variable scope to their local block, andavoids confusion for other developers and yourself.Now, scoping also works in situations where the blocks are nested.In this example, the return function has access to the 'bar' variablebecause it was declared in the outer scope.The function that is returned from the 'foo' function has access to all variablesdeclared in the scope of the 'foo' function.Now on the other hand,as you can see, this is notallowed because 'j'was declared inside ofa different scope.Now taking this one step further, we can do something like this.You know, this isn't verygood programming practice butit clearly demonstrateshow nested scoping works.The 'j' variable is available in all child scopes.
Scoping with Switch Statements

Scoping also applies to switch statements.Adding curly braces to your case statements will encapsulate them in theirown scope.This will throw an error because you are attempting todefine the 'label' constant twice inside of the same scope.However, if we were to rewrite that like this.This is perfectly acceptable because we have created an isolated scope foreach case statement.
Wrapping Up

Anything inside curly braces is considered to be inside of a block andyou can create a block all by itself.This is inside of an isolated block scope.'foo' is undefined in this scope, here.Now, constants behave in exactly the same way as let when it comes to scoping.Is for this reason that it is preferred to use constant 'let'over 'var' as often as possible.Easy.Blocked scope variables are a simple concept, and usingthe right type of variable declarations Is crucial to writing good clean code.Let's move on, and discuss block scope functions.