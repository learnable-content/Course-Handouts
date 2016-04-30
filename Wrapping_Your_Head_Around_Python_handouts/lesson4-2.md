![](headings/4.2.png)

# Raise an Exception

Now we're going to see how to **raise an exception**. So, we're going to start with our `try` again:

```py
try:
    raise Exception('testing exception')
except:
    print('exception raised')
```

Inside we say `raise` to manually raise an error with a message.

# SystemError Exception

Now raise a particular type of exception, rather than a general exception:

```py
try:
    raise SystemError('testing exception')
except SystemError as e:
    print('system error raised')
except Exception as e:
    print('general exception raised')
```

# Raise Our Own Exceptions

What's more, you can create custom exceptions:

```py
class MyException(RuntimeError):
   def __init__(self, arg):
      self.args = arg,
```

# Testing

Test it out:

```py
try:
   raise MyException('custom exception')
except NameError as e:
   print('name exception raised')
except MyException as e:
   print(e.args)
except Exception as e:
    print('general exception raised')
```