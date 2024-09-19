# The thing with abbreviations - Programming Principles

Developers like to keep things short. We need to save time wherever possible, and that's why we also favor abbreviations. Abbreviations are common and useful in programming principles, but they are often not very descriptive. Here is an incomplete list of common programming principles abbreviations that you should have encountered at least once in your programming career:

## KISS (Keep it simple, stupid!)

KISS is the abbreviation of "Keep it simple, Stupid" or sometimes "Keep it simple and smart" or "Keep it simple and short". The principle encourages reducing the complexity of the code(-base) as much as possible. Simpler code is easier to read, maintain and test. While it may sound straightforward, simplifying code effectively takes hard work. Fortunately, many of the other programming principles, like DRY and YAGNI, support the KISS principle.


## DRY (Don’t repeat yourself)


DRY stands for "Don't repeat yourself", which, as the name suggests, aims to eliminate redundancy. However, does this mean you should never have the same code twice? Not necessarily. A good guideline is the Rule of Three: if you're writing the same code for the third time, it's probably time to de-couple, refactor or abstract the problem. Consider future maintenance — do you really want to update multiple code sections when something changes?

By the way, did you know that there is also the opposite of DRY: WET - Write Everything Twice?


## YAGNI (You Aren’t Gonna Need it)

YAGNI means "You Aren't Gonna Need it", which in any case does not apply to this principle. When developing a feature, it can be tempting to add extra functionality for potential future use. You might anticipate future needs or create interfaces with additional functions, just in case. YAGNI advises focusing solely on what is needed right now. Plans often change, and what seems necessary today may be irrelevant tomorrow. Design for adaptability, but don't build more than what's required.


## SOLID
The SOLID principles are a set of five principles aimed at making software designs more understandable, flexible, and maintainable. They were developed by Robert C. Martin, Bertrand Meyer, and Barbara Liskov, with the acronym popularized by Michael Feathers. Each letter stands for a specific principle. Even though the principles talk about classes, they can also be applied to frontend development - especially for components. In frontend development, applying SOLID helps create more modular, scalable, and maintainable components.

### S - Single Responsibility Principle

"There should be only one reason for a class to change. In other words, every class should have only one responsibility."

If you have a component for a product overview `ProductOverview`, this component should not include getting the products from a backend. Better have a service or another component like `ProductFetcher` getting the data.


### O - Open Closed Principle

"Classes should be open for extensions but closed for modifications."

For instance a `BaseButton` button component defines basic styles and behaviour. When creating variations like `PrimaryButton` or a `SecondaryButton`, they extend the base component without changing it's core logic.


### L - Liskov Substitution Principle

"If a base class is a subtype of a super class, it should be possible to replace the super class with the base class without disrupting the behavior of the program."

In other words, this means the base class should be usable wherever you expect the super class.

Coming back to the button example, if you have a `IconButton` that extends a `Button` component. The `IconButton` could be used everywhere where the `Button` is implemented.



### I - Interface Segregation Principle

"Interfaces should be split such that clients only need to know about methods that are of interest to them. No client should be forced to depend on methods it doesn't use."

If you have a component that needs to have specific data like user information. Don't pass a `user` object with all possible data to the component, but just the values the component needs like `username` and `name`.


### D - Dependency Inversion Principle

"High-level modules should not depend on low-level modules; both should depend on abstractions."

API calls for example should be wrapped in services, so whenever the interface changes the component is not effected by that.


## TSR (The Scout Rule)
Though I call this TSR, "The Scout Rule", there isn’t any official abbreviation for it. In fact, it's referred to as 'The Boy Scout Rule' by Uncle Bob. Regardless of the name, I think it’s an excellent principle.

The rule comes from the Scouts' motto: “Always leave the campground cleaner than you found it”. Applied to coding, it means leaving the codebase better than it was. Whenever you touch the code, take a moment to improve it: re-format the file, remove unused dependencies or css styles or refactor a complicated function. Regularly tidying up will make your codebase more readable and maintainable over time.



## Further Readings
* Clean Code by Robert C. Martin
* https://martinfowler.com/bliki/Yagni.html
* https://gist.github.com/wojteklu/73c6914cc446146b8b533c0988cf8d29
* https://www.baeldung.com/solid-principles
* https://docs.getdbt.com/terms/dry
* https://www.baeldung.com/cs/kiss-software-design-principle
* https://medium.com/@hlfdev/kiss-dry-solid-yagni-a-simple-guide-to-some-principles-of-software-engineering-and-clean-code-05e60233c79f
