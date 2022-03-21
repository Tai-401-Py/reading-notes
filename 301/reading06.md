
# Reading  06

---

## [node.js](https://www.sitepoint.com/an-introduction-to-node-js/)

    What is node.js?

node.js is a runtime, that uses Google's V8 JavaScript enigne. It is Event-Based and has Asyncronous Input/Output

    In your own words, what is Chrome’s V8 JavaScript Engine?

It's an open source JS and WebAssembly engine that was built using C++, this engine has a bunch of features that have been added to it for ease of use and extra functionality.

    What does it mean that node is a JavaScript runtime?

It means that this can execute JavaScript code

    What is npm?

Node Package Manager, this handles the retrieval of all packages for install, boasting a library of over 1 million packages.

    What version of node are you running on your machine?

v16.13.2

    What version of npm are you running on your machine?

8.3.2

    What command would you type to install a library/package called ‘jshint’?

npm install -g jshint -> This would be a global install of this package

    What is node used for?

Node is the runtime environment that allows the execution of the node packages. It runs the JS on a server, it is also single threaded and event drivien which can prevent server slowdowns and even potential crashes. It does have its downsides in that  things like blocking input/output call should be avoided, and CPU intensive things should be handed off.

---

# [Paired Programming](https://canvas.instructure.com/courses/4345588/discussion_topics/14096892)

    What are the 6 reasons for pair programming?

1. Greater Efficiency

- By having two people working at the same time on the same code base, it's easier to catch mistakes as they are happening.  

2. Engaged Collaboration

- Programmers tend to be more focused on the code when body doubling, they also tend to ask for help from TAs and instructors less which can build self confidence.

3. Learning from Fellow Students

- Everyone has different learning tactics and styles and ways that they think about things. working with someone else can expose you to methods ou may have otherwise not thought of.

4. Social Skills

- Pair programming improves social skills and ability to communicate regarding a code base. By forcing you to communicate with another programmer it becomes more easily to convey what you are trying to communicate precisely when it comes to reading and analyzing code.

5.Job interview readiness

- Paired programming is a very common job interview process, by doing it in practice, it becomes easier to do when you really need the skill.

6. Work environment readiness

- Many companies will utilize paired programming for onboarding, and by already knowing paired programming it beomes one lless hurdle yto overcome while training.

    In your experience, which of these reasons have you found most beneficial?

In my experience I have founf that my ability to communicate which code I am talking about has increased greatly.

    How does pair programming work?

There is one driver, and one navigator. The driver is the only one who is directly interacting with the code. It is up to the navigator to tell them what to write and where to write it.
