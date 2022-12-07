## 1. Introduction
Welcome to software engineering practices, part I  
In this lesson, you'll learn about the following software engineering practices and how they apply in data science.
* Writing clean and modular code
* Writing efficient code
* Code refactoring
* Adding meaningful documentation
* Using version control

In the lesson following this one (part 2), you'll also learn about the following software engineering practices:
* Testing
* Logging
* Code reviews
## 2. Clean and Modular Code
* Production code: Software running on production servers to handle live users and data of the intended audience. Note that this is different from production-quality code, which describes code that meets expectations for production in reliability, efficiency, and other aspects. Ideally, all code in production meets these expectations, but this is not always the case.
* Clean code: Code that is readable, simple, and concise. Clean production-quality code is crucial for collaboration and maintainability in software development.
* Modular code: Code that is logically broken up into functions and modules. Modular production-quality code that makes your code more organized, efficient, and reusable.
* Module: A file. Modules allow code to be reused by encapsulating them into files that can be imported into other files.
## 3. Refactoring code
* Refactoring: Restructuring your code to improve its internal structure without changing its external functionality. This gives you a chance to clean and modularize your program after you've got it working.
* Since it isn't easy to write your best code while you're still trying to just get it working, allocating time to do this is essential to producing high-quality code. Despite the initial time and effort required, this really pays off by speeding up your development time in the long run.
* You become a much stronger programmer when you're constantly looking to improve your code. The more you refactor, the easier it will be to structure and write good code the first time.
## 4. Writing clean code
### Use meaningful names.
* Be descriptive and imply type: For booleans, you can prefix with is_ or has_ to make it clear it is a condition. You can also use parts of speech to imply types, like using **verbs for functions and nouns for variables**.
* Be consistent but clearly differentiate: age_list and age is easier to differentiate than ages and age.
* Avoid abbreviations and single letters: You can determine when to make these exceptions based on the audience for your code. If you work with other data scientists, certain variables may be common knowledge. While if you work with full stack engineers, it might be necessary to provide more descriptive names in these cases as well. (Exceptions include counters and common math variables.)
* Long names aren't the same as descriptive names: You should be descriptive, but only with relevant information. For example, good function names describe what they do well without including details about implementation or highly specific uses.
Try testing how effective your names are by asking a fellow programmer to guess the purpose of a function or variable based on its name, without looking at your code. Coming up with meaningful names often requires effort to get right.

### Writing clean code: Nice whitespace
Use whitespace properly.

* Organize your code with consistent indentation: the standard is to use four spaces for each indent. You can make this a default in your text editor.
* Separate sections with blank lines to keep your code well organized and readable.
* Try to limit your lines to around 79 characters, which is the guideline given in the PEP 8 style guide. In many good text editors, there is a setting to display a subtle line that indicates where the 79 character limit is.
## 5. Writing modular code
* Tip: DRY (Don't Repeat Yourself)  
Don't repeat yourself! Modularization allows you to reuse parts of your code. Generalize and consolidate repeated code in functions or loops.

* Tip: Abstract out logic to improve readability  
Abstracting out code into a function not only makes it less repetitive, but also improves readability with descriptive function names. Although your code can become more readable when you abstract out logic into functions, it is possible to over-engineer this and have way too many modules, so use your judgement.

* Tip: Minimize the number of entities (functions, classes, modules, etc.)  
There are trade-offs to having function calls instead of inline logic. If you have broken up your code into an unnecessary amount of functions and modules, you'll have to jump around everywhere if you want to view the implementation details for something that may be too small to be worth it. Creating more modules doesn't necessarily result in effective modularization.

* Tip: Functions should do one thing  
Each function you write should be focused on doing one thing. If a function is doing multiple things, it becomes more difficult to generalize and reuse. Generally, if there's an "and" in your function name, consider refactoring.

* Tip: Arbitrary variable names can be more effective in certain functions  
Arbitrary variable names in general functions can actually make the code more readable.

* Tip: Try to use fewer than three arguments per function  
Try to use no more than three arguments when possible. This is not a hard rule and there are times when it is more appropriate to use many parameters. But in many cases, it's more effective to use fewer arguments. Remember we are modularizing to simplify our code and make it more efficient. If your function has a lot of parameters, you may want to rethink how you are splitting this up.
## 6. Efficient code
Knowing how to write code that runs efficiently is another essential skill in software development. Optimizing code to be more efficient can mean making it:
* Execute faster
* Take up less space in memory/storage

The project on which you're working determines which of these is more important to optimize for your company or product. When you're performing lots of different transformations on large amounts of data, this can make orders of magnitudes of difference in performance.

* Tip 1: Use vector operations over loops when possible, numpy and numpy method are faster than list and loop
* Tip 2: Know your data structures and which methods are faster, set o(1) is much faster than list o(n)
## 7. Documentation
* Documentation: Additional text or illustrated information that comes with or is embedded in the code of software.
* Documentation is helpful for clarifying complex parts of code, making your code easier to navigate, and quickly conveying how and why different components of your program are used.
* Several types of documentation can be added at different levels of your program:
  * Inline comments - line level
  * Docstrings - module and function level
  * Project documentation - project level
