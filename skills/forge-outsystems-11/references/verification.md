# Verify the feature, not just a tool response
Before publishing, use current model validation and inspect changed module/dependency state. Publish only to the authorized target. Then test the served build, waiting for a screen-specific readiness signal rather than an arbitrary sleep.
Browser: use isolated synthetic identities per role, not shared stale sessions. Confirm visible account/role and data state. Keep session files and credentials outside knowledge/evidence exports.
For UI changes, inspect relevant desktop, intermediate and phone widths. 1440x900 and 390x844 are useful starting fixtures, not universal acceptance. Check keyboard focus/activation, labels, clickability, error association, wrapping, overlays, zoom and touch where relevant.
For UI changes, inspect screenshots visually and actual computed spacing. Verify all card insets, separators, dropdown arrow clearance, title gaps and header alignment. Include realistic long and missing data, not only an empty screenshot.
For writes: successful save then reload, invalid input, forbidden record access and applicable retry/stale-update cases. Check runtime errors. A publish pass does not imply usability or authorization correctness.
Native/offline mobile needs actual device/build/sync evidence; browser emulation is only partial coverage. Test Traditional Web with its matching lifecycle.
Evidence table: scenario, target/build, actor/fixture, expected, observed, status (pass/fail/unverified/not-applicable), artifact reference and date. Report limits and remaining defects.
Use rollback/version recovery appropriate to the actual environment. Do not reset user edits or delete live data as a test. Scale regression checks to impacted shared components.
