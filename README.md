# strength

Link: https://docs.google.com/presentation/d/1DFFFEJuC18ChHPYVwxVwXADpVpI9UT6BrYqTUS4rVzc/edit#slide=id.p
Project: https://github.com/orgs/bigbearsio/projects/2

## Rule
- Use only 3 micro instances provided. Do anythings with it. Use nothing else.
- We'll hit your service with incremental load.
### The Winner
- The one who can withstand the most traffic, Until any client
  - returns error.
  - Reset connection.
  - Times out within X ms.
- Has to have correct behaviors
  - No two client can have the same ticket.
  - Every round has to sell out before next round is open.
  - No client has ticket in the round if the current round is still not full.
  - If the client received response that ticket is sold, that should show up in getAllTickets()
  - If the server had not responded with success on a ticket, it should not show up in getAllTickets()
  
## Constraints / Technical
* Use Fixed hostname so DNS is not a limiting factor (ref: [#5](https://github.com/bigbearsio/strength/issues/5))
* Servers will all be in same cloud network

## Contributors

Bear Strength Enforcers
* [@tspn](http://github.com/tspn)
* [@supaket](https://github.com/supaket)
* [@makasak](https://github.com/mahasak)
* [@dtinth](https://github.com/dtinth)
* [@varokas](https://github.com/varokas)

Reference Implementation
* [@phantomnat](https://github.com/phantomnat)
