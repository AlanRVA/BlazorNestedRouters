# Blazor Nested Routers

<br/>

Nested routers allow you to define child routes within a parent route, so that a child component can route independently of its parent and without altering the browser URL.

This provides a higher degree of code reusability, better organized code structure, and more efficient rendering in some cases.

Blazor has no native support for nested routers like React, Vue, Svelte, and other front-end web frameworks, so I created a proof of concept for adding this functionality.

## Example Project

The example project is based off the default Blazor Web App project template and reuses the existing pages to show how they can be made to work as in-page nested routers or in a modal dialog control.

## Usage

Simply run the project and click on either the *Nested Dialog* or *Nested In-Page* side menu links to see each example.

## Components

NestedRouter\*NestedContainer.razor*: This is a parent container for the nested router, allowing you to wrap the router with navigation and logic to control the route of the nested router. This component can be added to a page for in-page/in-line use, or added to something like a modal dialog control.

NestedRouter\*NestedRouter.razor*: This is the nested router and handles the rendering of child components/pages when any navigation occurs inside the nested router. This keeps routing state local to the nested router and doesn't affect the top level router (or change the browser's URL).

NestedRouter\*NotFoundComponent*: Optional component to be shown if the nested router is asked to navigate to a component/page it can't find.

## Notes

This has been tested with .net 8 and 9 with Blazor Server only.