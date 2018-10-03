# TechEd2018-CGE716: Everything That Went Wrong with My SAPUI5 App

This is the examplatory code repository for TechEd Code Review Session CGE716 that was shown on TechEd 2018.
It is based on the SAPUI5 demo app "shopping cart" and outlines typical issues when developing complex apps with SAPUI5.

## Outline

Join this session to discover the most frequently abused and misunderstood concepts associated with SAPUI5 app development. Do you know how to troubleshoot your SAPUI5 app? In this interactive session, discuss and share with us what you have learned from your app projects and find out how to get the most out of SAPUI5.

## Instructions

1. Clone this repository in SAP Web IDE or run `npm install` and `ui5 start` to show the project locally in case of any infrastructure issues.

3. Follow the steps described below to fix the codebase while explaining what went wrong. Allow for questions and show whatever seems useful in the code base.

## Run

### Intro

1. Explain the project structure and how it is set up, quickly show the UI5 demo apps and tutorials

2. Run the app and ... see that the screen stays blank. Something went wrong!

### Troubleshooting

1. Show Developer tools

2. Fix code issue (missing comma)

3. Fix bootstrap issue (wrong path)

4. Fix wrong title tag in home view (use uncaught exception break points)

4. Fix syntax error in XML view (missing namespace)

6. Fix error in welcome.controller (missing id)

### Performance

1. Show Network trace and # of requests (ok with library preloads but slow)

2. Explain latency and cloud bootstrap (switch to Cloud CDN - should be faster)

3. Show single layout files loaded in network trace (add sap.ui.layout to manifest)

3. Run Support Assistant / Diagnostics (explain findings)

4. Check Performance errors and analyze network trace (preload, async, ...)

5. Still slow (show app build with ui5 build)

### Layouting

1. Check welcome view "Limited offer panel" (only title is visble, content has height 0)

2. Fix it

3. Fix Custom CSS (local class instead of standard class)

4. Show HCB Theme (show Theming app to show CSS parameters sap-ui-theme=sap_hcb)

5. Show Home view and CustomListItem (bad performance and unnecessary nesting)

### Data Binding

1. Check console "title" error (Fix wrong property with Diagnostics)

2. Fix wrong binding in cart view (Type in aggregation)

3. Fix expression binding in Panel title (W instead of w)

4. Break expression - remove a } somewhere (explain that its hard to debug)

5. Show to not use combined expressions and strings (use formatter + i18n text instead)

### Lifecycle

1. Show wrong attachment to routing / binding event (onAfterRendering instead of onRouteMatched)

2. Show use of Private API (no .oData, no _ API, nothing that is not listed in API reference)

3. Explain that there are different lifecycles (DOM / Rendering / Routing / Data Binding)

4. Async (show old shopping cart with 1.28)
https://sapui5.hana.ondemand.com/1.28.10/test-resources/sap/m/demokit/cart/index.html?responderOn=true#

5.Explain why it is crucial to not use old sync APIs anymore (still works but bad practice)

4. Show Callbacks and Promises (Async behavior)

### Summary and Q&A
