# Expo Camera Configuration Update Issue

This repository demonstrates a bug in the Expo Camera API where custom camera configurations, specifically `flashMode` and `autoFocus`, do not reliably update after initial setup.

## Problem

When setting camera properties such as `flashMode` or `autoFocus`, subsequent attempts to modify these properties might not be reflected in the camera preview.  The camera seems to maintain its initial state, ignoring later updates.

## Reproduction

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `expo start` to start the Expo development server.
5. Observe the camera preview and attempt to change flash mode and autoFocus using the buttons.  Notice the inconsistency.

## Solution

The provided solution involves completely re-initializing the camera component with the updated parameters. While less efficient than ideally changing settings in-place, this workaround ensures reliable configuration changes.

## Additional Notes

This issue could be related to internal state management within the Expo Camera component. Further investigation might be needed to identify the root cause and find a more performant solution.