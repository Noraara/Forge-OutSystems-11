# Equipment Notes

Equipment Notes is a fictional Reactive Web walkthrough for a lab technician who needs to save a short equipment note and find it again. It exercises native form behavior, server validation, persistence, and ownership without introducing a second module or a new design system.

## Brief

A signed-in technician can add a note with an equipment label and a description, then see their saved notes. Require an equipment label of 1–80 characters and a note of 1–250 characters after trimming whitespace. Every note belongs to the signed-in user who created it.

## Build in Service Studio

1. Use a disposable OutSystems 11 Reactive Web application and module. Confirm the module belongs to the intended app and identify the existing layout, authentication flow, and available roles. Use the existing registered-user flow for this sample.
2. Add an `EquipmentNote` entity with a record identifier, `EquipmentLabel`, `NoteText`, `OwnerId` using the user identifier type, and `CreatedOn`. Keep the entity operations behind a server action for creates.
3. Add `SaveEquipmentNote` with label and note inputs. Require an authenticated caller, trim and validate both inputs on the server, derive the owner from the authenticated user, and set the creation timestamp on the server. Return an outcome that distinguishes invalid input from a successful save. Do not accept a client-supplied owner.
4. Add an authenticated `MyNotes` screen using the app’s existing layout. Bind labeled inputs to a native form, surface validation beside the fields, and include a clear save action. Filter the notes data source by the authenticated user on the server and sort newest first. After a save, refresh the list and show success. Preserve input on validation or persistence failure.
5. Validate the module, publish to the sandbox you are authorized to use, then run the [verification checklist](verification.md) against its served URL.

This repository provides a walkthrough and acceptance checks for your sandbox. Build status and runtime outcomes depend on the module and environment you test.
