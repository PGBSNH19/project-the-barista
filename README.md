# Project 1 - The Barista
In this first project should you be working with what have been discussed regarding OOP in the theory for this lecture.

You should work in the group during the second half of the lecture.

On the start of the following lecture are your group going to present (a mini-presentation) the key points of you solution. And the rest of the class will give a points for the solution.

You need:

* One and only one, computer
* A stopwatch
* A yellow hat for the spy
* A green hat for the driver

Work with pair programming, one driver, 10 min per driver, driver wears a green hat, spy wears an yellow hat.

Everybody in the group is driver on turn. The last thing the drives does before leaving the keyboard to the next driver is to perform a commit and push of the code to GitHub. The comment should have the following comment "Driver @Github-username".

## Team

The team consist of 3 to 4 persons, with the following roles:

- **Driver**, the one sitting in front of the computer, and the only one using the keyboard and mouse, wears a green hat
- **Spy**, when signal is given should this person spy on another team
- **Timekeeper**, has a stopwatch and makes sure the team switch places as close to 10 min as possible and that the spy only spies the allowed time
- **Co-driver** (only for teams of four), everybody is in theory co-drivers and helps the driver. The term is taken from Rally where the co-driver keeps track on the track and the driver is responsible of steering the car.

The team rotate roles every 10 minutes, following this pattern:

* Spy becomes Driver
* Timekeeper becomes Spy
* Driver becomes Timekeeper, in case of four team members will the Driver become co-driver, and the co-driver become Timekeeper.

The timing is important as the team will retrieve penalty points for late or early rotation (measured on the git commit/push).

## Spying

When the signal is given should all spys go to a driver to learn about the solution by another team. Only the driver is allowed to talk with the spy and answer all the spy's questions. The total spy session from signal is given is **only** 45 seconds! And it's the mater of the timekeeper to cut of the spy.

A hint is to plan the spying: which team are we spying at? what are we looking for?

The result of the spying is a comment in the code like this:

```C#
// Spy: @GitHub-username, a short desciption of findings
```

## Mini-presentation of the project

On Thursday 5th of march 8:30, will each group do a mini presentation. You should long before the presentation have made decision in the group who is going to do the talking.

Be sharp you only have **5 min** including attaching your computer.

The rest of class will give a vote on paper, scale is 1-5, this vote is placed into the hat of the group.

### When voting

Remember to write the group you are voting on and your own group on the voting paper. Otherwise is the vote considered invalid.

Look for the following in the presentation:

- Code
- Tests
- Patterns
- Readiness
- Presentation

- Timing

## Points

This project is part of the overall evaluation of all students. This is done by collecting point. You and you team will get points for the following:

- Presentation, team-point
- A driver check-in, personal-point
- A vote, team-point
- A spy comment, personal-point
- Time off switching, gives negative points, team-point.

# Barista API
In this projects should you create an Fluent API for a [barista](https://en.wikipedia.org/wiki/Barista) to create espresso based drinks using code. To get into the Barista domain have a look at [The Ultimate Beginner's Guide to Espresso](https://prima-coffee.com/learn/section/espresso) they also have a [A Beginner's Guide to Espresso](https://www.youtube.com/watch?v=-kd-zX-JOVU) video serie (5 parts).

The API should be made for a barista-programmer, and he/she should be able to produce the following six cofee types using the API:
![Six coffee types](https://www.latteartguide.com/wp-content/uploads/2016/01/different-types-of-coffee-infograph.jpg)

The final method of the API should return a beverage-object of the correct type, depending on the methods which have been executed.

An example of how the API could look (this is pseudo-code!!):

```c#
IBeverage espresso = new EspressoMachine()
                            .AddWater(20)
                            .AddBeans(b => b.AmountInG = 5 && b.Sort = CoffeSorts.Robusta)
                        .ToBeverage();
// espresso is type of Espresso

IBeverage latte = new EspressoMachine()
                            .AddBeans(b => b.Sort = CoffeSorts.Robusta)
                            .GrindBeans()
                            .AddWater(20)
                            .AddMilk()
                        .ToBeverage();
// latte is type of Latte
```

## The solution 

The solution should cover the following:

- Encapsulation, Inheritance, Polymorphism, Abstraction
- A fluent api, which uses some lambda expressions
- Unit tests, is a must that the solution contains some unit tests

Extra

- The usage of attributes

