---
layout: default
title: Welcome
---

<style>
ol {
  float: left;
}
.codescreenshot {
  height: 250px;
  width: auto;
  border: none;
  display: none;
}
</style>

{% include alpha.html %}

<p class="lead">
{{site.project_title}} is a new type of library for the web, built on top of Web Components,
and designed to leverage the evolving web platform on modern browsers.
</p>

## Quick start

1. Clone the project to your app's root older. See [Get the code](/getting-the-code.html).

        git clone git://github.com/toolkitchen/toolkit.git --recursive

2. **Fire up a web server** in your app's directory.
3. Include `toolkit.js` in your main page:

        <script src="toolkit/toolkit.js"></script>

4. Read the [Getting Started](/getting-started.html) guide.
5. Learn how to soup-up your web components using the [Toolkit kernel](/toolkit-kernel-explainer.html).
6. Play with the [toolkit-ui examples](https://github.com/toolkitchen/toolkit-ui) (*also must be run from a web server)*.
7. Join the [mailing list](/discuss.html)! Ask questions and give feedback.

<p style="float:left;margin-left:10px;">
  <img class="codescreenshot" src="http://instacod.es/file/72206" alt="Custom element markup" title="Custom element markup">
</p>

<h2 style="clear:both;">What is the {{site.project_title}}?</h2>

{{site.project_title}} is comprised of two efforts:

- A set of core platform features ([Shadow DOM](/platform/shadow-dom.html),
[Custom Elements](/platform/custom-elements.html), [MDV](/platform/mdv.html)).
Initially, these core features will be enabled with a set of polyfills. As browsers
begin to implement these new primitives, the polyfill platform layer becomes smaller and better over time.
- A next-generation web application framework built upon these core technologies called the **_Toolkit_**.

The architectural stack looks like this:

<figure id="architecture-diagram">
  <!-- <img src="/images/architecture-diagram.svg" alt="Architecture Diagram" titld="Architecture Diagram"> -->
  <iframe src="/images/architecture-diagram.svg?{{'now' | date: "%Y%m%d"}}" seamless></iframe>
  <figcaption>Architectural Diagram</figcaption>
</figure>

## Guiding principles

The overall aim of the toolkit is to manage the complexity of building web applications. Our principles are:

**Everything is a component** — Encapsulation is the key to creating scalable, maintainable applications. All Toolkit resources are components, even ones that are non-visual. To construct an app, a developer creates new components, or uses ones the Toolkit provides, and assembles them together. Focusing on individual, composable building blocks allows developers to "think locally" about their application, reducing complexity. With this divide-and-conquer approach, applications can simultaneously be simple and arbitrarily complicated.

**Extreme pragmatism** — Developers should write the **minimum** amount of code possible to create their application. Anything repetitive should be re-factored into a component, handled by the Toolkit itself, or added into the browser platform itself. The Toolkit provides simple syntax without reducing features, and avoids boilerplate wherever possible.

**Salt to taste** —  Use as much or as little of the framework as you wish. An application can choose to only load `toolkit/platform/platform.js` to take advantage of the polyfills, or add `toolkit/toolkit.js` to
provide extra batteries for web components. We call this a ["Toolkit component"](/toolkit-kernel-explainer.html).

