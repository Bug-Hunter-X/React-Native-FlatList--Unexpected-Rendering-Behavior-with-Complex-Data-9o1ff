# React Native FlatList Bug: Unexpected Rendering Behavior

This repository demonstrates a common but subtle bug in React Native's `FlatList` component. The bug occurs when using `FlatList` with a complex data structure, resulting in incorrect rendering or crashes due to improper key management.

## The Problem

The core issue stems from not providing unique and consistent keys for the items rendered by `FlatList`. If keys are not unique or change unexpectedly during updates, `FlatList`'s internal reconciliation process can fail, leading to visual glitches, duplicated items, or application crashes.

## Solution

The solution involves ensuring each item in your data array has a unique and stable key, preferably generated using a unique identifier from your data source (e.g., a database ID). Avoid using generated keys based on the item's content, as changes to this content might result in unexpected behavior.   Also, use a proper `keyExtractor` to identify the item correctly.