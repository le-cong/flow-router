[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/flow-router/Lobby)
[![GitHub issues](https://img.shields.io/github/issues/VeliovGroup/flow-router.svg)](https://github.com/VeliovGroup/flow-router/issues)
[![GitHub forks](https://img.shields.io/github/forks/VeliovGroup/flow-router.svg)](https://github.com/VeliovGroup/flow-router/network)
[![GitHub stars](https://img.shields.io/github/stars/VeliovGroup/flow-router.svg)](https://github.com/VeliovGroup/flow-router/stargazers)
[![Twitter](https://img.shields.io/twitter/url/https/github.com/VeliovGroup/flow-router.svg?style=social)](https://twitter.com/intent/tweet?url=https%3A%2F%2Fgithub.com%2FVeliovGroup%2Fflow-router)

# FlowRouter Extra

<a href="https://www.patreon.com/bePatron?u=20396046">
  <img src="https://c5.patreon.com/external/logo/become_a_patron_button@2x.png" width="160">
</a>

Carefully extended [flow-router](https://github.com/kadirahq/flow-router) package.

## Features:

- Not dependent on Blaze, ready for [__React.js__](https://github.com/VeliovGroup/flow-router/blob/master/docs/react.md) and other templating/components engines/libs;
- No `underscore` package dependency;
- Great [tests coverage](https://github.com/VeliovGroup/flow-router/tree/master/test);
- Up-to-date [dependencies](https://github.com/VeliovGroup/flow-router/blob/master/package.js);
- Support of [Fast Render](https://github.com/VeliovGroup/flow-router/blob/master/docs/fast-render-integration.md) and [other great packages](https://github.com/VeliovGroup/flow-router#related-packages);
- Following semver with regular [releases](https://github.com/VeliovGroup/flow-router/releases);
- Great [wiki](https://github.com/VeliovGroup/flow-router/wiki);
- Great [quick start tutorial](https://github.com/VeliovGroup/flow-router/blob/master/docs/quick-start.md).

## Install

```shell
meteor add ostrio:flow-router-extra
```

### ES6 Import

```js
import { FlowRouter } from 'meteor/ostrio:flow-router-extra';
// Full list of available classes and instances:
// { FlowRouter, Router, Route, Group, Triggers, BlazeRenderer, RouterHelpers }
```

### Usage

```js
import { FlowRouter } from 'meteor/ostrio:flow-router-extra';

FlowRouter.route('/', {
  name: 'index',
  action() {
    // Render a template using Blaze
    this.render('templateName');

    // Can be used with BlazeLayout,
    // and ReactLayout for React-based apps
  }
});

// Create 404 route (catch-all)
FlowRouter.route('*', {
  action() {
    // Show 404 error page using Blaze
    this.render('notFound');

    // Can be used with BlazeLayout,
    // and ReactLayout for React-based apps
  }
});
```

## Documentation

- Continue with our [wiki](https://github.com/VeliovGroup/flow-router/wiki);
- [Quick start](https://github.com/VeliovGroup/flow-router/blob/master/docs/quick-start.md) tutorial;
- All docs as [single document](https://github.com/VeliovGroup/flow-router/blob/master/docs/full.md).

### Related packages:

- [ostrio:flow-router-title](https://github.com/VeliovGroup/Meteor-flow-router-title) - Reactive page title (`document.title`)
- [ostrio:flow-router-meta](https://github.com/VeliovGroup/Meteor-flow-router-meta) - Per route `meta` tags, `script` and `link` (CSS), set per-route stylesheets and scripts
- [staringatlights:fast-render](https://github.com/abecks/meteor-fast-render) - Fast Render can improve the initial load time of your app, giving you 2-10 times faster initial page loads. [`fast-render` integration tutorial](https://github.com/VeliovGroup/flow-router/blob/master/docs/fast-render-integration.md)
- [flean:flow-router-autoscroll](https://github.com/flean/flow-router-autoscroll) - Autoscroll for Flow Router
- [mealsunite:flow-routing-extra](https://github.com/MealsUnite/flow-routing) - Add-on for User Accounts
- [nxcong:flow-routing](https://github.com/cafe4it/flow-routing) - Add-on for User Accounts (alternative)
- [forwarder:autoform-wizard-flow-router-extra](https://atmospherejs.com/forwarder/autoform-wizard-flow-router-extra) - Flow Router bindings for AutoForm Wizard
- [nicolaslopezj:router-layer](https://github.com/nicolaslopezj/meteor-router-layer) - Helps package authors to support multiple routers
- [krishaamer:flow-router-breadcrumb](https://github.com/krishaamer/flow-router-breadcrumb) - Easy way to add a breadcrumb with enough flexibility to your project (`flow-router-extra` edition)
- [nicolaslopezj:router-layer](https://github.com/krishaamer/body-class) - Easily scope CSS by automatically adding the current template and layout names as classes on the body element

## Running Tests

1. Clone this package
2. In Terminal (*Console*) go to directory where package is cloned
3. Then run:

### Meteor/Tinytest

```shell
# Default
meteor test-packages ./

# With custom port
meteor test-packages ./ --port 8888

# With local MongoDB and custom port
MONGO_URL="mongodb://127.0.0.1:27017/flow-router-tests" meteor test-packages ./ --port 8888
```

## Support this project:

- [Become a patron](https://www.patreon.com/bePatron?u=20396046) — support my open source contributions with monthly donation
- Use [ostr.io](https://ostr.io) — [Monitoring](https://snmp-monitoring.com), [Analytics](https://ostr.io/info/web-analytics), [WebSec](https://domain-protection.info), [Web-CRON](https://web-cron.info) and [Pre-rendering](https://prerendering.com) for a website
