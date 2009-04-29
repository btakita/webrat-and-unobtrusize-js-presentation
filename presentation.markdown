# Webrat & Unintrusive JS #

# Rails Testing #

* Model
* Helper
* View
* Controller
* Selenium

# Attributes of Selenium & Controller Tests #

* Selenium

  * User flows
  * Almost complete integration (Html content, Javascript behavior, Browser differences)
  * Often removed from your controller architecture
  * Difficult to TDD
  * Difficult to tell if you have full coverage
  * Slow (often times not comprehensive)
  * Integration test combinatorial explosion

* Controller Tests

  * Single action
  * Only the rendered html (in test::unit by default and if integrate_views is on in rspec)
  * Easy to TDD
  * Comprehensive
  * Boiler-plate tests mixed with more interesting tests
  * Fast
  * Difficult to tell where the SUT fits into the rest of the app
  * Unit test isolation

# Common Usages of Selenium & Controller Tests #

* Selenium

  * Organized by use cases
  * Happy path testing (skipping edge cases)
  * Making sure js client/server interaction works
  * Mainly regression testing (tests are created after the feature is implemented)

* Controller Tests

  * Organized by action (method)
  * Full edge case coverage
  * View rendering is on to catch errors in view logic
  * Basic validation that the correct view is being presented

# Attributes of Webrat Tests #

* User flows (also useful to test single actions)
* Integration testing of the Rails stack (javascript & browser behavior needs to be simulated)
* Easy to TDD
* Can be comprehensive if organized by url path
* Integration test combinatorial explosion
* Can be slow depending on how the tests are organized
* Natural way to test forms and views

# How we are using Webrat Tests #

* Organized by url start point & use case
* A mix of Full edge case coverage and happy path testing
* TDD

# What Webrat tests enable #

* Top-down TDD
  * User flows
* Less Selenium tests
  * Most use cases covered
* More focused Controller Tests
  * integrate_views not needed as often
  * Less boiler-plate tests (more focus on interesting logic)
