# Equipment Notes verification

Use two separate synthetic users, A and B, in isolated browser sessions. Create a unique equipment label for the run and record the build under test. Keep identity and session details out of shared artifacts.

| Scenario | Steps | Expected evidence |
| --- | --- | --- |
| Model | Inspect the module and validate dependencies and affected model elements in Service Studio. | The module belongs to the intended app, and the validation outcome is recorded. |
| Successful save | As A, add a valid unique label and note. | The row appears once with the submitted values, and the UI reports success. |
| Persistence | Reload the page in A’s authenticated session. | The same row remains visible after reload. |
| Input validation | Submit a blank or whitespace-only label, and test the upper length bounds. | The relevant field explains the rejection, input remains available for correction, and no invalid row is created. |
| Ownership | Sign in as B in another context and open My Notes. | B’s list excludes A’s unique note. Confirm the server-side filter using the model. |
| Signed-out access | Open the screen in a fresh signed-out context. | The app requires authentication and exposes no note data. |
| Responsive and keyboard use | Submit with the keyboard at a desktop width, then repeat at a representative phone width. | Focus is visible, messages are associated with fields, and inputs and actions remain usable without horizontal overflow. |
| Runtime errors | Review page and server errors relevant to these actions. | Record the evidence for the attempted flows and any unresolved errors. |

Record observed outcomes using the [delivery record](../../skills/forge-outsystems-11/assets/delivery.md). Mark each row **pass**, **fail**, **unverified**, or **not applicable** according to the build you actually checked. Model validation and a successful publish are separate from runtime proof.
