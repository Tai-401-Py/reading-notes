# Pythonisms

## Dunders

Dunder or doubleunder are unique methods, they let you emulate behaviours of built in types.

Object initialization `__init__`

Object representation: 
`__repr__`: The “official” string representation of an object. This is how you would make an object of the class. The goal of `__repr__ `is to be unambiguous.

`__str__`: The “informal” or nicely printable string representation of an object. This is for the enduser

Iteration: `__len__`, `__getitem__`, `__reversed__`

Callable Python Objects: `__call__`
You can make an object callable like a regular function by adding the `__call__` dunder method.


## [Iterators](https://dbader.org/blog/python-iterators)

Bare bones iterator protocol

```py
    class Repeater:
        def __init__(self, value):
            self.value = value

        def __iter__(self):
            return RepeaterIterator(self)

    class RepeaterIterator:
    def __init__(self, source):
        self.source = source

    def __next__(self):
        return self.source.value   
```


the `__iter__` dundermethod is really a helperclass. 

RepeaterIterator looks like a straightforward Python class, but you might want to take note of the following two things:

In the `__init__` RepeaterIterator holds on to the “source” object that’s being iterated over.

In RepeaterIterator.__next__, we reach back into the “source” and return it

This causes an infinite loop. 

Here is something a bit healthierr
```py
    class BoundedRepeater:
    def __init__(self, value, max_repeats):
        self.value = value
        self.max_repeats = max_repeats
        self.count = 0

    def __iter__(self):
        return self

    def __next__(self):
        if self.count >= self.max_repeats:
            raise StopIteration
        self.count += 1
        return self.value
```

This will go until the max number of repeats have been reached. 


## [Generators](https://dbader.org/blog/python-generators)

Generators hit a little differently, calling a generator function doesn’t even run the function. It merely creates and returns a generator object. the code only really runs if you call next on it. 

`yield` - this keyword suspends a function yet holds onto state. 


# [NEXT.jx Famework](https://nextjs.org/learn/basics/create-nextjs-app)

## Why NEXT

Next si a framework that aims to have the best in-class dev experience. IOt includes many features that make developing your application much easier. 

- Intuitive page-based routing
- Pre-rendring and static generation, side server rendering, are all supported on a per-page basis
- Code splitting for faster load times
- Cklient side routing
- Native CSS and Sass, as well as support for any CSS lib. 
-API routes to build endpoints with serverless functions

## Pages

Pages are associated iwith a route based on thier filename. Folders nested in the pages folder will create new /routes

The link component mimics the `<a>` tag. You will first need to import it via `import Link from 'next/link'`

Syntactically links look like this...
```HTML
    <h1 className="title">
      Read{' '}
      <Link href="/posts/first-post">
        <a>this page!</a>
      </Link>
    </h1>
```

Using just a '/' in the Link href will return to home route. 

## Assets 

NEXT can serve static assets liek images under the top level public directory. This is also where your robots.txt will go. 

Different from normal web handling, NEXT fetches images on demand to reduce load times significantly. 

```js
    import Image from 'next/image';

    const YourComponent = () => (
      <Image
        src="/images/profile.jpg" // Route of the image file
        height={144} // Desired size with correct aspect ratio
        width={144} // Desired size with correct aspect ratio
        alt="Your Name"
      />
    );
```

## Metadata 

Metadata is handled with `<Head>` 

```js
    import Head from 'next/head';
    import Script from 'next/script';


    <Head>
      <title>Create Next App</title>
      <link rel="icon" href="/favicon.ico" />
      <Script
        src="https://connect.facebook.net/en_US/sdk.js"
        strategy="lazyOnload"
        onLoad={() =>
          console.log(`script loaded correctly, window.FB has been populated`)
        }
      />
```

script takes in some arguments.

`strategy` controls when the third-party script should load. A value of `lazyOnload` tells Next.js to load this particular script lazily during browser idle time

`onLoad` is to run any JS code after load, in this case rendering a console log of sucess. 

## React Context

React context is handy because it prevents the need for drilling of props from one parent to sucessive children when one component doesn't use it. 

There are four steps to using React context:

1. Create context using the createContext method.
2. Take your created context and wrap the context provider around your component tree.
3. Put any value you like on your context provider using the value prop.
4. Read that value within any component by using the context consumer.

You can create context by using syntax as such 
```js
    import React from 'react';

    export const UserContext = React.createContext();

    export default function App() {
      return (
        <UserContext.Provider value="Reed">
          <User />
        </UserContext.Provider>
      )
    }

    function User() {
      const value = React.useContext(UserContext);  
        
      return <h1>{value}</h1>;
    }

# You can also pass multiple context as a variable. 

    export default function App({ user }) {
      const { username, avatarSrc } = user;

      const avatar = <img src={avatarSrc} alt={username} />;

      return (
        <main>
          <Navbar avatar={avatar} />
        </main>
      );
    }
```
