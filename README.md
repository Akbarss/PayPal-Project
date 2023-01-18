# react-paypal-js

> React components for the [PayPal JS SDK](https://developer.paypal.com/docs/business/javascript-sdk/javascript-sdk-reference/)

<div class="badges">
    <a href="https://github.com/paypal/react-paypal-js/actions?query=workflow%3Avalidate"><img src="https://img.shields.io/github/actions/workflow/status/paypal/react-paypal-js/validate.yml?branch=main&logo=github&style=flat-square" alt="build status"></a>
    <a href="https://codecov.io/github/paypal/react-paypal-js/"><img src="https://img.shields.io/codecov/c/github/paypal/react-paypal-js.svg?style=flat-square" alt="coverage"></a>
    <a href="https://www.npmjs.com/package/@paypal/react-paypal-js"><img src="https://img.shields.io/npm/v/@paypal/react-paypal-js.svg?style=flat-square" alt="npm version"></a>
    <a href="https://bundlephobia.com/result?p=@paypal/react-paypal-js"><img src="https://img.shields.io/bundlephobia/minzip/@paypal/react-paypal-js.svg?style=flat-square" alt="bundle size"></a>
    <a href="https://www.npmtrends.com/@paypal/react-paypal-js"><img src="https://img.shields.io/npm/dm/@paypal/react-paypal-js.svg?style=flat-square" alt="npm downloads"></a>
    <a href="https://github.com/paypal/react-paypal-js/blob/main/LICENSE"><img src="https://img.shields.io/npm/l/@paypal/react-paypal-js.svg?style=flat-square" alt="apache license"></a>
    <a href="https://paypal.github.io/react-paypal-js/"><img src="https://raw.githubusercontent.com/storybooks/brand/master/badge/badge-storybook.svg" alt="storybook"></a>
</div>

## Why use react-paypal-js?

### The Problem

Developers integrating with PayPal are expected to add the JS SDK `<script>` to a website and then render components like the PayPal Buttons after the script loads. This architecture works great for simple websites but can be challenging when building single page apps.

React developers think in terms of components and not about loading external scripts from an index.html file. It's easy to end up with a React PayPal integration that's sub-optimal and hurts the buyer's user experience. For example, abstracting away all the implementation details of the PayPal Buttons into a single React component is an anti-pattern because it tightly couples script loading with rendering. It's also problematic when you need to render multiple different PayPal components that share the same global script parameters.

### The Solution

`react-paypal-js` provides a solution to developers to abstract away complexities around loading the JS SDK. It enforces best practices by default so buyers get the best possible user experience.

**Features**

-   Enforce async loading the JS SDK upfront so when it's time to render the buttons to your buyer, they render immediately.
-   Abstract away the complexity around loading the JS SDK with the global [PayPalScriptProvider](https://paypal.github.io/react-paypal-js/?path=/docs/example-paypalscriptprovider--default) component.
-   Support dispatching actions to reload the JS SDK and re-render components when global parameters like `currency` change.
-   Easy to use components for all the different Braintree/PayPal product offerings:
    -   [PayPalButtons](https://paypal.github.io/react-paypal-js/?path=/docs/example-paypalbuttons--default)
    -   [PayPalMarks](https://paypal.github.io/react-paypal-js/?path=/docs/example-paypalmarks--default)
    -   [PayPalMessages](https://paypal.github.io/react-paypal-js/?path=/docs/example-paypalmessages--default)
    -   [PayPalHostedFields](https://paypal.github.io/react-paypal-js/?path=/docs/paypal-paypalhostedfields--default)
    -   [BraintreePayPalButtons](https://paypal.github.io/react-paypal-js/?path=/docs/braintree-braintreepaypalbuttons--default)

## Installation

To get started, install react-paypal-js with npm.

```sh
npm install @paypal/react-paypal-js
```
