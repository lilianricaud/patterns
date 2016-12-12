# Extreme Manufacturing Explained

In 2008, Joe Justice responded to a challenge from the X-Prize competition to create a road-legal 100mpg automobile. Despite having little time, hardly any budget, competition from over 100 well-funded competitors from companies and universities around the world, and changing requirements from the awards committee, his company's WIKISPEED entry placed 10th in the Mainstream class. Joe not only created a great car, he also developed an Agile approach to creating physical products.

As a software developer, Joe was an "Agile native." He had only worked with methods like Scrum and Extreme Programming, so his engineering practices drew heavily on his software experience. Today, WIKISPEED is selling prototypes, and the WIKISPEED approach to manufacturing is turning heads worldwide at companies like Boeing and John Deere. "Our technology is more sophisticated than yours, but your culture is light-years ahead of ours!"

Joe calls his approach "Extreme Manufacturing." XM emphasizes the ability to create products quickly and integrate changes rapidly into existing products. XM is collection of principles and patterns to help you create and adapt products quickly.

I had the honor of co-teaching a CSM + Extreme Manufacturing course with Joe last week, and with his encouragement, this series of articles seeks to refine, document and publish those principles:
- Optimize for change
- Object-Oriented, Modular Architecture
- Test Driven Development (Red, Green, Refactor)
- Contract-First Design
- Iterate the Design
- Agile Hardware Design Patterns
- Continuous Integration Development
- Continuous Deployment Development
- Scaling Patterns
- Partner Patterns

These principles and patterns do not represent the final wisdom on Agile manufacturing, but rather a work-in-progress, on the discovery of better ways to manufacture things.

## XM Principle 1: Optimize for change

What happens if an engineer comes up with a way to build a safer car door? Can that new door be deployed right away? No. A stamping machine and a custom made die produce that door. Together they cost over 10 million US dollars and they must first be amortized before the new door can be economically produced. Given the high costs, it can take 10 years or more before that better door can enter production. You can see the impact of the need to amortize huge investments in the slow, incremental changes in automobiles from year to year, even from decade to decade!

WIKISPEED can change their design every seven days. They employ tools like value stream mapping not merely to reduce the variance of products produced or to optimize the flow through the production line, but first and foremost to reduce the cost of change. It does not cost them more to use a new design than to use an existing design. So if they have a safer way to build the door today, they start using it next week.

Welcoming and responding to change represent core Agile values and principles (see the Agile Manifesto and the Principles behind the Agile Manifesto). So by adopting this principle, you take a huge step towards becoming an Agile organization.



## XM Principle 2: Object-Oriented, Modular Architecture

In the software industry until the 1980's, programs were developed on a procedural model. This led to extremely complex, unmaintainable solutions. A change to one part of the program usually required changes throughout the program.

This 'tight-coupling' is still pervasive in automotive designs. A change to the suspension requires a change to the chassis, which requires a change to something else, with eventually impacts the designing of the entire car. 

Today software developers use "information hiding" and object-oriented design patterns to create loosely coupled, highly modular solutions. So you can change for instance the login process without having to modify other parts of your system.

At the X-Prize competition, many of the competitors dropped out. Why? As it became clear that there would be many entrants, the organizers planned to hold a race on city streets to determine the overall winner. This was changed to a coast-to-coast rally, and finally they settled on a race over a very demanding, closed course racetrack. Each acceptance scenario posted very different demands on the suspension. These changes posed huge challenges for teams that could not embrace change rapidly.

The WIKISPEED car is designed as 8 modules, with simple interfaces between the modules. Due to its modular architecture, WIKISPEED was able to switch suspension systems with a minimum of fuss. WIKISPEED has also discovered it can apply related patterns, like inheritance and code reuse, to its advantage. 

Embracing change is a core agile value. The ability to adapt rapidly meant WIKISPEED did better in the X-Prize competition than the nearly 100 entrants who dropped out without producing a car.

How do achieve an object-oriented, modular architecture? The next two principles will help you:

Test-Driven Development (Red, Green, Refactor)
Contract-First Design

## XM Principle 3: Test-Driven Development

...also known as "red, green, refactor"

Before Joe started building a car, he created a model for predicting fuel economy. He identified over 100 well known, freely available parameters, like weight, drag coefficients, engine power, tire size, etc. Based on these parameters he could predict the EPA fuel economy of the car within a few percent. 

Armed with this model, he was able to calculate the characteristics the WIKISPEED entrant must have in order to achieve not only 100 miles per gallon, but also to achieve performance characteristics worthy of a high-end sports car.

Team WIKISPEED wanted to achieve five-star crashworthiness according to the specifications of the NHTSA and IIHS. These specify impacts under multiple conditions to evaluate the crashworthiness of the cars. These tests are quite expensive, US$10'000 per test, plus the costs of the vehicle itself, transport and disposal of the test vehicle and the travel costs for the people involved. How can they update their designs every week, when each change requires retesting?

Step one was to use Finite Element Analysis to simulate the crashes. When they believed their car would pass the test, they ran an actual test. Of course they did not pass the test, but that was not the purpose. They wanted real crash data so they could better model crashes in their simulations. They updated their simulations based on the actual crash data. After a few iterations, their simulations became so good, that the authorities now accept the results of their simulations in lieu of actual tests. Since they can now do (almost) fully automated tests, they can simulate crash tests every week.

When designing new components, 

Create the test it is expected to pass. That can be very high level, like emissions tests or crash standards, or it might be more component level. If it is possible to automate the test (or create an automated proxy for the test), do so, as this reduces the cost of repeating the test after future design changes.
Create the simplest design possible that enables the test to pass.
Iterate on the design, improving it until it is more valuable to work on another portion of the product.

In software, this process is known as "Red-Green-Refactor." To implement something, first create a test, which by definition fails immediately ("goes red"). Then implement functionality to make it pass (go green). Then improve the design for better maintainability, efficiency, etc. This is called refactoring.

## XM Principle 4: Contract-First Design

The initial design decision of the WIKISPEED car was that it should consist of eight modules – body, chassis, motor, suspension, interior, etc. Before Team WIKISPEED even started to design individual components, they designed the interfaces between those modules.

Joe did not know what suspension would be used on his car, but he was able identify the external parameters and boundary conditions of the suspension. After researching the subject, he found that that if the suspension mounting could withstand 8 gees, it would more than meet all the necessary requirements, even for Formula One racing applications. So the team identified a suitably sized block of aluminum that could carry that load. Any suspension that could be attached to that block could be used on the WIKISPEED car without modification to the rest of the car. 

So when designing a solution, 
Design the interfaces based on outside parameters, e.g. load factors, or communication and power requirements.
Only architect the connections up front, not the individual components.
Leave room to grow, i.e. over engineer these interfaces, because changing these fundamental contracts may be expensive.
P.S. Be sure to check out the Wrapper pattern to ensure independence between your design and the design of any component suppliers.

## XM Principle 5: Iterate the Design

One frequently asked question for hardware or embedded projects considering Scrum is, "How can we get stuff done every sprint? It takes longer to develop a piece of hardware than could ever fit in a two-week sprint!" Hardware development needs to take a slightly different view on iterations and iterating than software development.

When the WIKISPEED engineers were first working on the interior, they realized that the lack of an emergency brake was slowing down their progress. The brake handle sits between the seats, close to the gearshift and to the attach points for the seats and seat belts. Because no one knew what the emergency brake handle looked like, they were unwilling to commit to design decisions on these nearby components. 

The solution was "version 0.01" of the emergency brake: a cardboard box that said, “the brake handle will fit in this box.” That was enough functionality that the team could move forward on nearby components, even though nobody had any illusions that this cardboard box would actually hold the car in place!

When working with hardware, you will iterate on your designs:
- Create the test that your design should pass.
- Create the simplest design possible that enables the test to pass.
- Improve the design to be simpler or more elegant.
- Repeat this process ("Iterate on the design") until improving this component is no longer the highest value work you can do.

In the case of v0.01 of the emergency brake, the acceptance test was "Can the engineers design the surrounding components with confidence?" The cardboard box satisfied this test. Other components were judged to be of higher value, so they stayed with the cardboard box until the other components were finished enough.

When developing software with Agile, each iteration should produce potentially deliverable functionality. That may not be possible when working with hardware, so you may need to iterate on a particular item many times before the design is satisfactory. In the case of the WIKISPEED X-Prize entrant, those subsequent iterations included, "An emergency brake to hold the car in place," and "An emergency brake which produces no resistance when the car is in motion."

You may also need to iterate on your acceptance tests, especially as you strive to automate them. Before WIKISPEED performed a real crash test, they had done many Finite Element simulations. These are cheap and repeatable, because all they need is computer time. Then they had a real crash test performed. That crash produced results that were different from their simulation, so they iterated. They used the real crash data to improve their simulation. Eventually their simulations became close enough to reality that they no longer needed the expensive physical tests. 

## XM Principle 6: Agile Hardware Design Patterns


A pattern is an old idea. A pattern is simple way to represent implicit knowledge about well-known solutions to well-known problems. Patterns were pioneered in architecture by Christopher Alexander to facilitate the understanding of good solutions to common challenges in building houses and other structures. Software developers picked up on the idea to communicate solutions to typical challenges in computer systems. WIKISPEED has identified a number of patterns to help design good hardware. For example:

### Wrapper – Use a wrapper to adapt a third party part to your contract. If you use the supplier's interface as your contractual interface, any change in either product or supplier will probably cause you to redesign the interface, a potentially expensive undertaking.


### Facade – Use a façade, a connector of connectors with a simple interface, whenever multiple wires (like data & power) need to go to the same place.

### Singleton – Every component needs power, data and ground. The first thing every engineer wants to create when designing a new component is the power, data and ground bus. The singleton pattern says for each basis component, there is just one in use. So if you need a power-data-ground bus - use ours!

Sometimes the patterns have a cost. The wrapper pattern added 8 kg to the weight of a WIKISPEED car, for example by adding an extra slab of aluminum between the chassis and the suspension.

Was the design pattern worth the extra weight? Yes, because that pattern allowed Team WIKISPEED to a) reduce several hundred pounds from the weight of the car by steady optimization, and b) react easily and cheaply to the changing suspension requirements. Had they not been able to do that, they would not have been able to participate in the final selection round.
