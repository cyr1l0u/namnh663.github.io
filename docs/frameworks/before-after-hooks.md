---
layout: default
title: Before And After Hooks
parent: Karate
grand_parent: Frameworks
nav_order: 8
---

# Before And After Hooks

## Before Hooks

* **Background Section:** Code placed here executes before every scenario.
  * Use `call` to call another feature and access its return value in the current scenario.
  * Use `callOnce` to call another feature only once before all scenarios (cached value used subsequently).
* **`karate-config.js`:** Use `callSingle` to run code before all features (entire test suite).

## After Hooks

* **`configure` Keyword:** Used to define after hooks.
  * `afterScenario`: Define a JavaScript function to execute after each scenario.
  * `afterFeature`: Define a JavaScript function to execute after the entire feature completes.
    * The function can call another feature using `karate.call`.

## Inline vs. External JavaScript Functions

* Inline functions can be written directly within the hook configuration.
* For complex functions, use embedded expressions to call a separate JavaScript file.

## Key Points

* Background section mimics `@Before` behavior from other testing frameworks.
* `callOnce` is similar to `@BeforeSuite`.
* After hooks provide flexibility for post-scenario or post-feature actions.
