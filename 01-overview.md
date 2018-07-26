# Types of Tests

1. Unit
1. Integration
1. End-to-end (E2E)

## Unit Tests

1. Testing a small unit of code (e.g. a function or method)
1. Aware of implementation details
1. Written and executed by developers
1. No GUI
1. No network/DB/etc. use

## Integration Tests

1. Look at how units of code interact (e.g. a public API)
1. Not aware of implementation details/internal logic
1. Might be written by QA or test engineers, have a GUI, use the network, etc.

## End-to-end tests

1. Tests the actual application as it would be used by people
1. More likely to be used by QA
1. Require a fair bit of technical skill to write
1. Typically the slowest and most expensive

+++

# Test Pyramid

Normal model:

![Network](https://automationpanda.files.wordpress.com/2017/10/the-testing-pyramid.png?w=620)

+++

But it is contentious!

![](https://www.dropbox.com/s/tsjxri6u3ndhkhn/testing-rauchg.png?raw=1)
(author of socket.io)

+++

# Why unit tests might not be the right focus

1. Diminishing returns at your write more tests
1. Unit tests can be fragile because they often end up testing implementation details
1. Bugs that occur between multiple units of code are typically harder to find, test, and reason about
![](https://cdn-images-1.medium.com/max/1600/0*eCs8GoVZVksoQtQx.gif)
1. If your app doesn't work, your users don't care if you have 10k unit tests

If integration/E2E testing could be sufficiently fast and easy, then maybe you should focus there. That's the goal behind Cypress