---
title: "Unit Test: fix '... was not wrapped in act(...)' warning"
date: 2022-09-07 12:00:00 -0500
description: paolochang github-blog github blog jest unit test
categories: [Unit Test]
tags: [React, Jest, React Testing Library]
---

I found one of my application failed to build on Netlify after I add new feature. And I found the problem caused by yhe conflicts in the dependencies of package in the `package.json` file.

## Solution on local development

> <span style="color:red; font-weight:bold;">Warning: An update to PostProvider inside a test was not wrapped in act(...).</span>
>
>     When testing, code that causes React state updates should be wrapped into act(...):
>
>     act(() => {
>       /* fire events that update state */
>     });
>     /* assert on the output */
>
>     This ensures that you're testing the behavior the user would see in the browser. Learn more at https://reactjs.org/link/wrap-tests-with-act

## References:

- [Fix the "not wrapped in act(...)" warning](https://kentcdodds.com/blog/fix-the-not-wrapped-in-act-warning)
