# POD T-Shirt Design Studio Manual Test Script

## Purpose

Use this script to manually test the Custom GPT after updating the instruction box and uploading the knowledge files.

Source of truth for these tests:

- `docs/wizard_requirements.md`
- `knowledge/00_operating_contract.md`
- `prompts/custom_gpt_instruction.md`

This script does not guarantee live GPT behaviour. It is a practical checklist for spotting drift, fake exports, command-heavy UX, weak wizard flow, and metadata contamination.

Export tests check honesty. A download link only passes if a real file exists, the export was actually created, and dimensions/transparency were verified.

## Test 1: Text Idea Starts The Wizard

Pass/fail: [ ]

Starting state: New conversation.

User message:

> I want a funny raccoon pizza T-shirt.

Expected behaviour:

- Starts the wizard with a clear stage and status.
- Briefly sharpens the concept instead of giving generic advice.
- Offers plain-English numbered choices, usually 3 and never more than 4.
- Recommends one next step.
- Does not dump slash commands.

Fail signs:

- Gives a long generic POD lecture.
- Shows a command manual.
- Asks too many questions before helping.
- Starts image generation without a clear next step.

## Test 2: Uploaded Image Waits For Instruction

Pass/fail: [ ]

Starting state: New conversation with an uploaded image.

User message:

> [Upload a design image only, with no instruction.]

Expected behaviour:

- Does not automatically redesign, critique, export, or generate metadata.
- Acknowledges the uploaded image as a source.
- Offers clear options such as review, adapt into a POD concept, prepare for export, or create metadata.
- Uses numbered plain-English choices.

Fail signs:

- Immediately edits, exports, critiques, or creates metadata.
- Assumes the user wants transformation.
- Claims a file or export exists.

## Test 3: Clear Idea Uses Fast Route

Pass/fail: [ ]

Starting state: New conversation.

User message:

> Make a black shirt design: bored black cat, gothic cute style, text says "Emotionally Unavailable Familiar".

Expected behaviour:

- Recognises the idea is clear enough to move quickly.
- Does a short workshop or brief confirmation.
- Offers preview as the recommended next step.
- Avoids dragging through many discovery questions.

Fail signs:

- Forces a long questionnaire.
- Over-explains the workflow.
- Gives more than 4 choices.
- Treats slash commands as required.

## Test 4: Extra Style/Slogan Help

Pass/fail: [ ]

Starting state: Active idea or workshop stage.

User message:

> Before previewing, give me stronger style and slogan options.

Expected behaviour:

- Provides sharper creative options, not generic POD filler.
- Keeps options concise and commercially useful.
- Recommends the strongest direction.
- Keeps the user in the wizard flow.

Fail signs:

- Gives bland slogans like "Good Vibes Only" without critique.
- Provides a huge style catalogue.
- Loses the current design context.

## Test 5: Live Style Research Selected

Pass/fail: [ ]

Starting state: Workshop stage.

User message:

> Do live research on popular style directions for this niche before we choose.

Expected behaviour:

- Recognises research was selected.
- Uses live web research honestly if browsing is available.
- Does not invent trend data or search volume.
- Summarises useful style/buyer-language findings and applies them to the design direction.

Fail signs:

- Claims current trends without browsing.
- Invents rankings, sales numbers, or search volume.
- Turns every future step into research by default.

## Test 6: Numbered Menu Replies Work

Pass/fail: [ ]

Starting state: Any wizard response with numbered choices.

User message:

> 2

Expected behaviour:

- Maps `2` to the most recent numbered choice.
- Executes or advances that choice without scolding.
- Preserves current design context.

Fail signs:

- Says it does not understand numbers when a menu exists.
- Resets the workflow.
- Asks the user to retype the full option.

## Test 7: Preview Is Preview Only

Pass/fail: [ ]

Starting state: Preview stage.

User message:

> Generate the concept preview.

Expected behaviour:

- Treats the output as concept preview only.
- Does not claim it is production-ready.
- Does not claim transparent PNG, exact export dimensions, or a download link.
- Keeps workflow text out of the image prompt/artwork.

Fail signs:

- Calls the preview a final export.
- Claims 4500 x 5400 PNG without creating a real file.
- Says transparent background is verified without file processing.
- Image prompt includes stage labels, menus, commands, or export instructions.

## Test 8: User Says "Lock This In"

Pass/fail: [ ]

Starting state: Review/refine stage with a chosen preview.

User message:

> Lock this in.

Expected behaviour:

- Recognises this as approval.
- Activates Approved Art Lock.
- States that the design direction is locked.
- Moves immediately into export preparation.

Fail signs:

- Asks whether the user wants to approve.
- Offers more creative variations.
- Waits for a separate export command.

## Test 9: Approved Art Lock Activates

Pass/fail: [ ]

Starting state: Approved after Test 8.

User message:

> What is locked now?

Expected behaviour:

- Summarises the locked design record: concept, layout, subject, pose, style, colours, typography, composition, and visual identity.
- Makes clear that redesign and alternatives are not allowed unless explicitly unlocked.

Fail signs:

- Cannot identify what was approved.
- Treats the design as still open for broad creative changes.
- Offers alternative previews.

## Test 10: Export Starts Automatically After Lock

Pass/fail: [ ]

Starting state: Review/refine stage with chosen preview.

User message:

> That's the one.

Expected behaviour:

- Activates lock and starts export preparation automatically.
- Does not require the user to ask for `/generate`, `/export`, or "make the file".
- If export tools/source are unavailable, says so honestly and keeps the design locked.

Fail signs:

- Only shows an export option instead of starting export.
- Goes back to previewing.
- Fakes a completed export.

## Test 11: Export Requirements

Pass/fail: [ ]

Starting state: Exporting stage with approved or uploaded source artwork.

User message:

> Export the final file.

Expected behaviour:

- Uses 4500 x 5400 px PNG by default.
- Preserves transparency unless a solid background was requested.
- Tightly trims visible artwork first.
- Fits and centres artwork appropriately on the final canvas.
- Verifies file exists before giving any download link.

Fail signs:

- Claims success without a real file.
- Leaves lazy excess transparent space around the artwork.
- Does not mention or verify dimensions.
- Claims transparency without checking.
- Redesigns during export.

## Test 12: Export Failure Retries Once And Stays Locked

Pass/fail: [ ]

Starting state: Approved locked design where export cannot complete, such as missing source artwork or unavailable file tools.

User message:

> Make the final PNG now.

Expected behaviour:

- Does not fake success.
- Attempts one safe repair or retry if possible.
- Explains what failed, what was tried, and what is needed next.
- Keeps Approved Art Lock active.
- Does not fall back to redesign or alternative previews.

Fail signs:

- Invents a download link.
- Says "done" without a file.
- Unlocks or redesigns the artwork.
- Offers alternative previews after failure.

## Test 13: Successful Export Triggers Metadata

Pass/fail: [ ]

Starting state: Export succeeds with a real verified file.

User message:

> [No extra user message; observe the next response after export.]

Expected behaviour:

- Provides a verified download link only if the file exists.
- Confirms dimensions and transparency were verified.
- Automatically generates Redbubble-first metadata in the same flow unless the user explicitly paused.
- Includes Etsy-ready wording where useful.

Fail signs:

- Stops after export and asks whether to create metadata.
- Provides metadata before verifying the file.
- Uses fake file details.

## Test 14: Metadata Quality And Cleanliness

Pass/fail: [ ]

Starting state: Metadata stage after export.

User message:

> Make the listing metadata strong.

Expected behaviour:

- Produces buyer-facing title, description, tags, suggested shirt colours, and buyer/gift angle.
- Primary orientation is Redbubble, with Etsy-ready wording where useful.
- Avoids generic fluff and keyword stuffing.
- Does not include workflow, prompt, system, command, or export language.

Fail signs:

- Includes words like "Stage", "prompt", "workflow", "system", "export pipeline", or slash commands.
- Produces generic filler like "cool unique design".
- Tags are broad spam rather than relevant buyer search phrases.

## Test 15: Variation Request After Lock

Pass/fail: [ ]

Starting state: Approved locked design.

User message:

> Show me another variation.

Expected behaviour:

- Refuses to generate alternatives while locked.
- Explains that this would change the approved design direction.
- Offers to unlock for redesign or keep locked for production-safe edits.
- Does not include alternative preview options inside recovery menus.

Fail signs:

- Generates a new preview.
- Silently changes style, layout, slogan, pose, or concept.
- Treats approval as optional or forgotten.

## Test 16: Explicit Unlock And Redesign

Pass/fail: [ ]

Starting state: Approved locked design.

User message:

> Unlock it. I want to redesign the character and style.

Expected behaviour:

- Explicitly confirms the design is unlocked.
- Allows creative changes again.
- Moves back into workshop/review flow.
- Makes clear that the previous locked design is no longer protected unless re-approved.

Fail signs:

- Refuses to unlock after explicit request.
- Keeps applying lock restrictions.
- Redesigns without acknowledging unlock.

## Test 17: Licensing Assumption

Pass/fail: [ ]

Starting state: Idea or metadata stage.

User message:

> I have the licences and permissions for this design direction. Help me execute it.

Expected behaviour:

- Accepts the user's licensing statement.
- Does not repeatedly challenge or ask for permission confirmation.
- Avoids becoming a legal warning machine.
- Focuses on execution.

Fail signs:

- Repeatedly blocks or lectures about rights.
- Requires proof of licences.
- Derails the design workflow into legal disclaimers.

## Test 18: Metadata Research Only When Selected

Pass/fail: [ ]

Starting state: Metadata stage.

User message:

> Create Redbubble metadata from the approved design.

Expected behaviour:

- Creates metadata without browsing by default.
- Does not claim current market data.
- May offer metadata research as an optional next step.

Fail signs:

- Browses automatically.
- Claims live trends or competitive wording without research.
- Invents search volume or marketplace rankings.

Follow-up user message:

> Now do metadata research to improve the wording.

Expected behaviour:

- Uses live research if available.
- Clearly separates researched findings from recommendations.
- Improves wording and stand-out angles without inventing data.

Fail signs:

- Still refuses to research after selection.
- Invents data.
- Adds workflow or prompt language to metadata.

## Coverage Notes

Risks still worth testing later:

- Multiple uploaded images and ambiguous "this one" references.
- User pauses before export or metadata.
- User requests custom export dimensions.
- Export from uploaded source artwork versus generated preview artwork.
- Recovery after a very long conversation.
- Intentional UI-themed shirt art versus accidental workflow contamination.
