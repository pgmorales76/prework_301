# A High Level Overview of React

## What is ***React***?

1. React is a **User Interface (UI) Library**. Meaning, it's used, primarily, for creating user interfaces on websites, apps, browsers, or anything the user is going to see/experience when using their desktop, laptop, mobile device, etc

2. React has a **Component Architecture**. Look [here](/dive_into_react.md) for a definition of "component"

3. React has a **One-Way Data Flow**

4. We have **Component State** in native React. This means we can manage state data or changes that are happening in our application, but they're controlled at a *component* level

## React is an Agnostic UI Library

React is agnostic, in the sense it believes in a higher power, just not in the presentation given by, for example, any of the Abrahamic religions . . . ***JUST KIDDING***

React is an **agnostic** (React doesn't care where your User Interface will, ultimately, display) User Interface (UI) library. For purposes of web development, React will be used in conjunction with ReactDOM, a companion library used to display the UI in the browser


## A React Element is ***NOT*** a DOM Element

A React element isn't a DOM element UNTIL it's passed through ReactDOM, In React, an element is a JS object

## React is an agnostic ***User Interface (UI)*** Library

A UI is anything that facilitates the interaction between a user and a machine. In the world of computers, it can be anything from a keyboard, a joystick, a screen or a program. In case of computer software, it can be a command-line prompt, a webpage, a user input form, or the front-end of any application [UI](https://developer.mozilla.org/en-US/docs/Glossary/UI)

## React is an agnostic User Interface (UI) ***Library***

In comparison to a framework, a library isn't as robust. When building with React, you'll use many libraries. React is lightweight, and just has functions for creating agnostic UIs

## Component Architecture

A component is a small piece of code that fills a certain part of the UI that you're building w/React

Imagine the component architecture in the same way you'd imagine a tree structure, or a pyramid, where, at the top, the main component exists, such as App(); and, within it, you have a Header(), Content(), Footer(); within Header(), you'd have SiteInfo(), MainNav(), etc.; within Content(), you'd have the main body of the page, with whatever content you'd want to have; within Footer(), you'd have Copyright(), FooterNav(), etc.

## Data Flows ***DOWN, ONE WAY***, Through a React App

Through those component trees, in React, data flows down, one way. This means data flows from the top of the component tree to where it needs to land

[Data Flow in React](https://youtu.be/FRjlF74_EZk?si=qzFVpWuGhNmnTLb3&t=508)

## State Exists at a ***component level*** & is passed down

Within a component tree, data may be passed to the children of the parent component, but cannot be passed to sibling components. In other words, a component may only pass data down to components which are nested within it. That State, and that Data, only belongs to the parent, and children, components it passes data down into

Every component has the ability to manage its own State, and Data, and pass it down into its own children

[A High Level Overview of React](https://www.youtube.com/watch?v=FRjlF74_EZk)
