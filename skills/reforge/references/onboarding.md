# Mobile onboarding

Design toward a concrete first useful outcome, such as creating a workspace or saving a first project. Establish what information or permission is required before that outcome. Recommend deferring optional setup when it would reduce effort; implement changes to steps, required fields, permissions, or navigation only within the authorized product scope.

## Map the existing flow

Inspect the relevant screens and their implemented transitions. Make a compact working map, scaled to the requested scope, with each step's purpose, required input, next action, failure recovery, and saved state. Include branches such as skipping, permission denial, and returning after interruption when they exist. Distinguish observed behavior from assumptions about unavailable backend or device behavior.

For each step, identify what it contributes to the first useful outcome and where effort or uncertainty occurs. For a visual-only task, use these findings to improve hierarchy, instructions, and feedback while preserving navigation and business logic. Record suggested flow changes separately. For an authorized flow redesign, preserve required business and consent constraints while simplifying the path.

## Design each step

- Give each step one clear task or idea, a visible primary action, and concise supporting copy. Explain the benefit before requesting effort.
- Show progress when the sequence is finite and predictable. Keep Back and Skip available where the product permits them, preserve entered data, and make resuming understandable.
- Ask for permissions in context, explaining their purpose. Provide a usable denial path where possible; do not simulate operating-system prompts or coerce consent.
- Use illustrations and background treatments to support the current step. Keep fields, controls, error messages, and keyboard interaction on calm, readable surfaces.
- Respect safe areas, platform back behavior, dynamic text, screen readers, and keyboard avoidance. Aim for at least 44 pt touch targets on iOS and 48 dp on Android; use appropriately generous targets on mobile web.
- Check loading, invalid input, offline or request failure, permission denial, and return-to-flow behavior where relevant to the changed screens. Put useful recovery actions next to the problem.
- Keep progress and entered data stable through transitions. Support reduced motion; avoid auto-advancing screens that interrupt reading.
- End with a meaningful next action or the useful product state, rather than an ornamental completion screen.

## Verify the path

Walk from entry to the defined first useful outcome and confirm that the final action reaches a useful product state. For changed steps, check applicable branches from the map: Back, Skip, invalid input, request failure and retry, permission denial, and leaving and returning. Confirm that progress and entered data follow the existing persistence contract; do not introduce storage of sensitive inputs merely to make resuming easier.

Inspect the active field, its error message, and the next action with the keyboard open where device tools permit. Check long labels and enlarged text in the actual layout. Report inaccessible device or backend paths as unverified instead of inferring success from screenshots.

For each identified issue, connect the correction to an observable result: an error now explains recovery, the keyboard no longer covers Continue, or Back retains previously entered non-sensitive data as intended. Recheck the affected path after changes.
