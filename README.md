Airport Challenge
=================

```
        ______
        _\____\___
=  = ==(____MA____)
          \_____\___________________,-~~~~~~~`-.._
          /     o o o o o o o o o o o o o o o o  |\_
          `~-.__       __..----..__                  )
                `---~~\___________/------------`````
                =  ===(_________)

```

Task
-----

We have a request from a client to write the software to control the flow of planes at an airport. The planes can land and take off provided that the weather is sunny. Occasionally it may be stormy, in which case no planes can land or take off.  Here are the user stories that we worked out in collaboration with the client:


```
------------------------------------------------
As an air traffic controller
So I can get passengers to a destination
I want to instruct a plane to land at an airport
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Create Airport class
Create Plane class
Create Method for landing a Plane at Airport
(Test - lands a plane)
------------------------------------------------
################################################
------------------------------------------------
As an air traffic controller
So I can get passengers on the way to their destination
I want to instruct a plane to take off from an airport and confirm that it is no longer in the airport
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Create a take off method that confirms the plane has left the airport
Remove plane from airport with confirmation message
(Test - takes off a plane)
------------------------------------------------
################################################
------------------------------------------------
As an air traffic controller
To ensure safety
I want to prevent takeoff when weather is stormy
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Create a method that defines the weather which will mostly output sunny.
Create a test to ensure that planes can take off when sunny.
Create another test that will force the weather condition to be stormy thus
raising an error message. 
------------------------------------------------
################################################
------------------------------------------------
As an air traffic controller
To ensure safety
I want to prevent landing when weather is stormy
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Create a stub that ensures the weather for this test will be stormy.
Pass a test that will raise an error if weather is stormy so plane cannot land.
Ensure when weather sunny, planes can still land fine.
------------------------------------------------
################################################
------------------------------------------------
As an air traffic controller
To ensure safety
I want to prevent landing when the airport is full
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Define constant with DEFAULT_CAPACITY of airport to 10 planes
Create a method that raises an error when airport full
Create test to check if airport full against default capacity
------------------------------------------------
################################################
------------------------------------------------
As the system designer
So that the software can be used for many different airports
I would like a default airport capacity that can be overridden as appropriate
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Define constant with default capacity which is then changeable when calling new object on class
Create test to test this
------------------------------------------------

```

Your task is to test drive the creation of a set of classes/modules to satisfy all the above user stories. You will need to use a random number generator to set the weather (it is normally sunny but on rare occasions it may be stormy). In your tests, you'll need to use a stub to override random weather to ensure consistent test behaviour.

Your code should defend against [edge cases](http://programmers.stackexchange.com/questions/125587/what-are-the-difference-between-an-edge-case-a-corner-case-a-base-case-and-a-b) such as inconsistent states of the system ensuring that planes can only take off from airports they are in; planes that are already flying cannot take off and/or be in an airport; planes that are landed cannot land again and must be in an airport, etc.

For overriding random weather behaviour, please read the documentation to learn how to use test doubles: https://www.relishapp.com/rspec/rspec-mocks/docs . There’s an example of using a test double to test a die that’s relevant to testing random weather in the test.

Please create separate files for every class, module and test suite.

In code review we'll be hoping to see:

* All tests passing
* High [Test coverage](https://github.com/makersacademy/course/blob/master/pills/test_coverage.md) (>95% is good)
* The code is elegant: every class has a clear responsibility, methods are short etc.

Reviewers will potentially be using this [code review rubric](docs/review.md).  Referring to this rubric in advance will make the challenge somewhat easier.  You should be the judge of how much challenge you want this weekend.

**BONUS**

* Write an RSpec **feature** test that lands and takes off a number of planes

Note that is a practice 'tech test' of the kinds that employers use to screen developer applicants.  More detailed submission requirements/guidelines are in [CONTRIBUTING.md](CONTRIBUTING.md)

Finally, don’t overcomplicate things. This task isn’t as hard as it may seem at first.

* **Submit a pull request early.**  There are various checks that happen automatically when you send a pull request.  **Fix these issues if you can**.  Green is good.

* Finally, please submit a pull request before Monday at 9am with your solution or partial solution.  However much or little amount of code you wrote please please please submit a pull request before Monday at 9am.
