---
title: "Error: React Native Reanimated"
date: 2022-12-14 12:00:00 -0500
description: paolochang github-blog github blog reactnative mobile
categories: [Mobile, React Native]
tags: [React Native, Bug Fix]
---

## React Native Renanimated

> ```
> ERROR  Error: Failed to initialize react-native-reanimated library, make sure you followed installation steps here: https://docs.swmansion.com/react-native-reanimated/docs/fundamentals/installation/
> 1) Make sure reanimated's babel plugin is installed in your babel.config.js (you should have 'react-native-reanimated/plugin' listed there - also see the above link for details)
> 2) Make sure you reset build cache after updating the config, run: yarn start --reset-cache, js engine: hermes
>  ERROR  Invariant Violation: Failed to call into JavaScript module method AppRegistry.runApplication(). Module has not been registered as callable. Registered callable JavaScript modules (n = 11): Systrace, JSTimers, HeapCapture, SamplingProfiler, RCTLog, RCTDeviceEventEmitter, RCTNativeAppEventEmitter, GlobalPerformanceLogger, JSDevSupportModule, HMRClient, RCTEventEmitter.
>         A frequent cause of the error is that the application entry file path is incorrect. This can also happen when the JS bundle is corrupt or there is an early initialization error when loading React Native., js engine: hermes
>  ERROR  Invariant Violation: Failed to call into JavaScript module method AppRegistry.runApplication(). Module has not been registered as callable. Registered callable JavaScript modules (n = 11): Systrace, JSTimers, HeapCapture, SamplingProfiler, RCTLog, RCTDeviceEventEmitter, RCTNativeAppEventEmitter, GlobalPerformanceLogger, JSDevSupportModule, HMRClient, RCTEventEmitter.
>         A frequent cause of the error is that the application entry file path is incorrect. This can also happen when the JS bundle is corrupt or there is an early initialization error when loading React Native., js engine: hermes
> ```

## Troubleshoot & Problem Solve

Installing the package
First step is to install react-native-reanimated as a dependency in your project:

> ```
> yarn add react-native-reanimated
> ```

Babel plugin
Add Reanimated's Babel plugin to your babel.config.js:

> ```
>  module.exports = {
>    presets: [
>      ...
>    ],
>    plugins: [
>      ...
>      'react-native-reanimated/plugin',
>    ],
>  };
> ```

> CAUTION: Reanimated plugin has to be listed last.
{: .prompt-warning }

## Reference

- [React Native Reanimated > Fundamentals > Installation](https://docs.swmansion.com/react-native-reanimated/docs/fundamentals/installation/)
