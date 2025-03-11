# Prioritization with the house analogy

A while ago we bought an old house which we wanted to renovate. With the start of the renovation, we quickly realized that we had more of a refurbishment on our hands. Time passes by, things take a lot longer than expected and we needed to make plans to move in - even though the house was still more of a construction area.

During this time, I remembered an analogy that a former manager introduced to me. It helped me think about prioritization in both house renovations and product development: The House Analogy.

## The House analogy
With The House Analogy you prioritize things as if you are building - or renovating -  a house, but already living in it. The idea is simple: When living in a house under construction, some tasks are urgent while others can wait. This helps us decide what needs immediate attention versus what can be done later.

There are four categories that go from major to minor impact:

1. 🏚️ Structure
2. 🪨 Boulder
3. 🛠️ Tools/👕 Clothes/🧸 Toys/📚 Books
4. 💐 Decoration

It's important to note that priorities are not fixed. What seems like a minor issue today could become critical tomorrow.

### 🏚️ Structure (Blocking + Immediate Action)

We need to ensure the roof and walls are in place.

#### Criteria
* Defect completely blocks testing of the feature
* Defect causes failure of the functionality
* No workaround
* Major data corruption

#### Action
Got to do it now because otherwise there is no house

### 🪨 Boulder (Blocking)
A door is blocked and we cant go through.

#### Criteria
* Impacts major functionality
* Defect causes failure of part of the product’s functionality
* Workaround is not obvious and is difficult to complete
* Impacts defined KPIs or quality

#### Action
We have to do it, but we can finish other things first

### 🛠️📚 Tools/Clothes/Toys/Books (Future Action)
Some tools, clothes, toys or books laying around on the floor. We got to remove it, but we don’t have to do it now.

#### Criteria
* Impacts minor functionality or non-critical data
* Workaround is easy
* E.g. UI layout issues
* Spelling and grammatical errors

#### Action
We have to do it, but later.

### 💐 Decoration (Future Consideration)
It would be nice, if we would add some decorations, but we can do it later.

#### Criteria
* No impacts to functionality or data
* Does not require a workaround
* E.g. UI colors

#### Action
We talk about whether or not we want to do it later.


## Summary
Prioritization is often tricky, but The House Analogy provides a practical way to break things down. Whether you're fixing a house or improving a product, understanding what’s critical versus what can wait will help you make better decisions.


## Inspired by
* [Feedback Ladders: The Code Review System We Follow at Netlify](https://www.netlify.com/blog/2020/03/05/feedback-ladders-how-we-encode-code-reviews-at-netlify/)
* [Rocks, Pebbles, Sand, and Beer](https://shepleywood.com/news/rocks-pebbles-sand-and-beer)

## Credits to
[Daniela Valero](https://danielavalero.com/)
