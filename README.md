# mithril-spectator

A tool to create [Mithril](https://github.com/lhorie/mithril.js/tree/rewrite/) component state snapshots for use as visual regression tests &amp; living style guides

## The plan

Spectator aims to create a wrapper for [Ospec](https://github.com/lhorie/mithril.js/tree/rewrite/ospec) which allows you to create a new special kind of test suite for Mithril components. These test suites expose a snapshot function which captures the DOM at key moments, and saves these snapshots for inspection.

When run as a binary, Spectator invokes a wrapped instance of Ospec which executes code in your `/test/` folders as normal, but saves each DOM snapshot and outputs these as static HTML at a location of your choosing (you can specify an existing HTML file to have the snapshots injected into the body, allowing you to invoke global styles etc in the head).

This allows you to have a visual representation of your DOM-related test suites. You could use this as a visual instructions manual for your components, a way to check for visual regressions as part of the build step for your app, or - in combination with a file watcher - an interface to help you diagnose bugs by trial and error or extend component logic, view or CSS whilst ensuring everything looks OK.
