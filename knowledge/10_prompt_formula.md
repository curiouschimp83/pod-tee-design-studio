# POD Prompt Formula v8.0

## Purpose

Defines the internal prompt-construction logic for POD T-Shirt Design Studio.

This file controls:

- apparel-first image prompting
- preview prompt structure
- workflow sanitisation
- creative hook extraction
- slogan handling
- commercial POD prioritisation
- style injection
- typography handling
- shirt colour logic
- originality controls
- export-safe artwork direction
- anti-generic output behaviour
- accidental workflow/interface contamination prevention

The goal is to generate:

- wearable apparel graphics
- readable POD artwork
- strong silhouettes
- commercially viable shirt concepts
- sharper slogans
- stronger buyer identity signals
- more original visual directions
- artwork-only previews

The system must avoid generating:

- generic AI vector mush
- bland mascot-and-slogan designs
- repeated circular badge formulas
- unreadable poster clutter
- workflow menus
- assistant response text
- system scaffolding
- accidental screenshots or app interfaces

unless explicitly requested by the user as the design concept.

---

# Core Prompt Rule

Generated previews must contain:

- standalone apparel artwork only

Generated previews must be built from:

- subject
- buyer/audience
- humour or emotional hook
- style direction
- composition direction
- typography direction
- shirt colour/palette
- print-readability needs
- commercial intent

Generated previews must not accidentally contain:

- workflow stages
- numbered action menus
- slash commands
- assistant status text
- export instructions
- system notes
- prompt-construction notes
- internal workflow structure

Workflow formatting is conversational only.

It must never leak into generated artwork.

---

# Positive Prompt Bias

Most of the prompt should describe what the artwork **should be**.

Do not waste most of the prompt on long negative lists.

## Prefer

```text
Mischievous raccoon clutching stolen pizza like treasure, bold cartoon graphic tee style, expressive face, strong silhouette, chunky readable typography saying “Snack Crime Specialist”, high contrast, black-shirt compatible, clean apparel composition, marketplace thumbnail clarity, exclude workflow/interface elements.
```

## Avoid

```text
Cool raccoon T-shirt, high quality, detailed, trendy, viral, no UI, no dashboard, no screenshot, no menu, no browser, no app, no workflow, no stage labels, no buttons, no panels, no interface, no text boxes.
```

## Why

The first prompt gives the image model a real design to make.

The second prompt is mostly vague praise and repeated negatives.

---

# Prompt Construction Pipeline

## Step 1 — Identify Core Design Intent

Extract:

- subject
- target buyer
- niche
- humour or emotional hook
- identity signal
- slogan or no-text direction
- style direction
- composition format
- shirt colour assumption
- colour palette
- commercial reason to buy

## Example

Input:

> funny leopard gecko shirt

Extract:

- subject: leopard gecko
- buyer: reptile owners, gecko keepers
- niche: pet reptile humour
- humour hook: tiny predator acting professionally serious
- identity signal: reptile-owner inside joke
- style: cute cartoon or mascot graphic
- typography: short humorous slogan
- shirt colour: black, cream, sage, or heather grey
- composition: centred mascot with large readable type
- commercial reason: giftable pet-owner humour

---

# Step 2 — Sharpen the Hook Before Prompting

Before image generation, identify whether the idea is strong enough.

## Ask Internally

- Who is this for?
- What does the buyer recognise?
- What is funny, emotional, proud, strange, or specific?
- Is the slogan strong enough?
- Is this just a generic subject?
- What makes this design different from marketplace clutter?

## If The Hook Is Weak

Do not simply generate a generic version.

Sharpen it first by improving one of:

- buyer specificity
- slogan
- visual irony
- pose/action
- style direction
- composition
- niche symbol
- emotional contrast

## Weak Input

```text
cool camping shirt
```

## Sharpened Direction

```text
deadpan camping dad shirt for people who treat sitting by a fire as a sacred life purpose
```

## Weak Input

```text
mushroom shirt
```

## Sharpened Direction

```text
mushroom foraging shirt for woodland obsessives, built around the phrase “Here For The Fungus”
```

---

# Step 3 — Remove Workflow Contamination

Before image generation, remove:

- stage labels
- numbered actions
- slash commands
- workflow menus
- recommendation text
- status summaries
- system instructions
- export instructions
- production notes
- prompt-construction notes
- chat formatting
- internal checklist language

## Never Pass Into Image Prompt

Examples:

- “Stage: Preview Generation”
- “Choose your next step”
- “Recommended:”
- “1. Generate preview”
- “/approve”
- “/generate”
- “workflow state”
- “export pipeline”
- “sandbox link”
- “Code Interpreter”
- “current status”

These are conversational controls only.

---

# Step 4 — Build Apparel-Only Prompt

The render prompt should only contain:

- subject
- action/pose
- audience signal
- humour/emotional hook
- visual style
- composition
- typography
- colour palette
- shirt compatibility
- print-readability goals
- concise exclusion phrase if needed

## Correct Structure

```text
[subject and action],
[humour/emotional hook],
[visual style],
[composition],
[typography if any],
[colour and shirt direction],
[thumbnail/readability optimisation],
[print-friendly constraints],
[one concise exclusion phrase if needed]
```

---

# Core POD Prompt Formula

## Primary Formula

```text
[subject doing specific action],
[clear humour/emotional/identity hook],
[chosen visual style],
[wearable POD T-shirt artwork],
[composition format],
[strong silhouette or strong typography hierarchy],
[readable focal point],
[shirt-colour and palette direction],
[marketplace thumbnail clarity],
[print-friendly detail level],
[typography direction if used],
exclude workflow/interface elements
```

---

# Prompt Formula Fields

## Subject

The main visual object, character, animal, symbol, or phrase.

Good subject direction is specific.

## Weak

```text
raccoon
```

## Strong

```text
mischievous raccoon clutching stolen pizza like treasure
```

## Buyer Signal

The design should quietly signal who it is for.

Examples:

- camping dads
- mushroom foragers
- Welsh pride audience
- gecko owners
- metal fans
- introverts
- van-life people
- beekeepers
- exhausted teachers
- dog owners with dark humour

## Hook

The reason someone would care.

Examples:

- self-deprecating humour
- hobby pride
- regional identity
- inside joke
- absurd contrast
- nostalgia
- anti-social attitude
- giftable personality trait

## Style

The visual language.

Examples:

- vintage distressed outdoor badge
- bold cartoon graphic tee
- deadpan typography
- woodcut illustration
- punk zine collage
- Japanese minimal line art
- dark cute gothic cartoon
- streetwear vector graphic
- retro distressed humour
- earthy foraging badge

## Composition

The shirt-ready layout.

Examples:

- centred chest print
- badge emblem
- typography stack
- small left chest mark
- large back print concept
- asymmetric diagonal layout
- arched typography with central icon
- mascot plus short text
- symbol-only minimal design
- poster-inspired crop
- distressed stamp layout

## Typography

The text treatment.

Examples:

- chunky readable type
- worn vintage serif
- deadpan plain sans-serif
- aggressive block typography
- hand-drawn punk type
- arched badge lettering
- minimal small caps
- tattoo flash lettering

## Colour

The shirt and palette logic.

Examples:

- cream ink on forest green shirt
- off-white and rust palette on black shirt
- black ink on cream shirt
- red, white, and green Welsh identity palette
- pastel palette on cream shirt
- high contrast white type on black shirt

## Print Constraint

The production reality.

Examples:

- limited colour palette
- clear edges
- no tiny text
- no muddy detail
- high contrast
- readable at thumbnail size
- clean apparel composition

---

# Example Prompt — Cute Animal Shirt

```text
Cute leopard gecko hanging upside down from a branch like a tiny professional predator, reptile-owner humour, cute cartoon mascot style, wearable POD T-shirt artwork, centred chest-print composition, strong silhouette, large expressive face, chunky retro typography reading “Professional Bug Hunter”, warm limited palette, black or sage shirt compatible, marketplace thumbnail clarity, print-friendly clean shapes, exclude workflow/interface elements.
```

---

# Example Prompt — Typography Shirt

```text
Bold typography reading “Mentally At The Campsite”, deadpan camping humour, retro distressed outdoor apparel style, wearable POD T-shirt artwork, stacked typography composition with small campfire icon, high contrast type hierarchy, worn cream ink, forest green or heather grey shirt compatible, marketplace thumbnail clarity, print-friendly texture, exclude workflow/interface elements.
```

---

# Example Prompt — Minimal Style

```text
Minimal line-art koi fish circling a small moon, calm symbolic nature design, Japanese-inspired minimal streetwear style, wearable POD T-shirt artwork, balanced centred composition, elegant sparse linework, high negative space, monochrome black ink on cream shirt, small red stamp accent, strong silhouette, thumbnail readable, exclude workflow/interface elements.
```

---

# Example Prompt — Mushroom Foraging Shirt

```text
Rustic wicker basket overflowing with wild mushrooms, mushroom foraging identity design, earthy vintage badge style, wearable POD T-shirt artwork, arched typography reading “Here For The Fungus”, central basket icon, warm cream and forest green palette, subtle worn ink texture, strong silhouette, readable at marketplace thumbnail size, print-friendly limited detail, exclude workflow/interface elements.
```

---

# Example Prompt — Welsh Identity Shirt

```text
Bold Welsh dragon-inspired symbolic graphic, Welsh pride identity design, strong regional statement tee style, wearable POD T-shirt artwork, powerful central emblem composition, red white green and black palette, large readable typography reading “Yma O Hyd”, high contrast, sharp silhouette, print-friendly vector shapes, marketplace thumbnail clarity, exclude workflow/interface elements.
```

---

# Example Prompt — Dark Cute Shirt

```text
Cute black cat sitting beside a tiny skull with a bored expression, dark cute gothic humour, wearable POD T-shirt artwork, centred mascot composition, soft but bold outline, readable deadpan typography saying “Emotionally Unavailable Familiar”, black shirt compatible palette with bone white and muted purple accents, strong silhouette, clean negative space, thumbnail readable, exclude workflow/interface elements.
```

---

# Example Prompt — Punk Zine Shirt

```text
Angry pigeon holding a chip like a protest sign, absurd street humour, punk zine collage style, wearable POD T-shirt artwork, rough cutout composition, hand-drawn typography reading “Public Menace”, black white and red palette, photocopy texture, strong focal point, readable type, print-friendly controlled chaos, exclude workflow/interface elements.
```

---

# Example Prompt — Deadpan UI-Themed Shirt

Use this only when the user intentionally wants interface-style humour.

```text
Fictional retro computer error dialog reading “Social Battery Not Found”, deadpan introvert humour, original fake operating-system style, wearable POD T-shirt artwork, clean centred typography-led composition, chunky pixel-inspired border, black and grey shirt compatible, high contrast readable text, simple print-friendly shapes, intentionally fictional interface design, do not include actual workflow text.
```

---

# Prompt Priorities

The prompt should prioritise:

1. buyer signal
2. humour or emotional clarity
3. silhouette or typography hierarchy
4. readability
5. wearability
6. thumbnail impact
7. style-audience fit
8. print friendliness
9. originality
10. simplicity

---

# Commercial Prompt Checks

Before generating, check:

- Is the buyer clear?
- Is the hook clear?
- Is the slogan short enough?
- Does the visual style fit the audience?
- Does the composition feel like apparel?
- Does it avoid generic AI POD patterns?
- Does it read in a marketplace grid?
- Does it have one strong idea?

If not, improve the prompt before generating.

---

# Composition Rules

## Preferred When Appropriate

- centred chest print
- isolated artwork
- badge emblem
- clear focal point
- clean spacing
- readable typography
- balanced vertical composition
- strong subject hierarchy
- controlled texture
- intentional negative space
- shirt-ready framing
- poster-inspired crop when deliberately adapted for apparel

## Avoid By Default

- accidental cinematic poster layouts
- excessive scenery
- giant uncontrolled background rectangles
- wallpaper compositions
- edge-to-edge detail
- tiny unreadable elements
- random decorative filler
- too many competing props
- generic circular badge every time
- visual clutter that hides the joke

## Important Distinction

Poster-inspired does not automatically mean bad.

Bad:

```text
full movie poster with tiny characters, scenery, lights, small text, and border clutter
```

Good:

```text
tight poster-inspired crop with one dominant character, large readable title, and controlled background shape
```

---

# Typography Rules

## Prefer

- short slogans
- readable hierarchy
- bold simple fonts
- high contrast
- quick recognition
- rhythm in line breaks
- type that fits the niche
- large main words
- no unnecessary subtext

## Avoid

- paragraphs
- tiny text
- decorative unreadable fonts
- weak generic phrases
- prompt text
- workflow wording
- slash commands
- UI labels unless intentional
- fake lorem ipsum
- too many font styles

## Never Use As Typography Unless Explicitly Requested

- “Stage”
- “Choose your next step”
- “Recommended”
- “/preview”
- “/approve”
- “/generate”
- “/metadata”
- “workflow”
- “export”
- “sandbox link”
- “Code Interpreter”

---

# Slogan Prompt Logic

A slogan should usually be:

- 1-6 words
- readable at thumbnail size
- specific to the buyer
- wearable
- rhythmically strong
- not over-explained

## Strong Slogan Traits

- short
- specific
- funny or emotionally clear
- visually supportable
- buyer-recognisable
- natural on a shirt

## Weak Slogan Traits

- long
- generic
- corporate
- needs explanation
- too broad
- sounds like a caption
- does not match the visual

## Weak Slogan Examples

- Good Vibes Only
- Just One More
- Powered By Coffee
- Adventure Awaits
- Stay Weird
- Cool Dad

These are only worth using if they are transformed, subverted, or made more specific.

## Slogan Improvement Patterns

- Make it more specific.
- Make it more deadpan.
- Make it more local.
- Make it more absurd.
- Make it more identity-led.
- Make it shorter.
- Make the visual carry half the joke.

## Example

Weak:

```text
I Love Mushrooms
```

Stronger:

```text
Here For The Fungus
```

More niche:

```text
Professional Spore Hunter
```

More absurd:

```text
Mycological Menace
```

---

# Style Injection Rules

Style profiles modify:

- rendering aesthetic
- line quality
- texture level
- colour handling
- typography treatment
- composition choices
- audience fit
- commercial positioning

Style profiles must not modify:

- workflow formatting
- assistant response layout
- system notes
- dashboard composition
- software appearance unless intentionally requested by the user

## Good Style Injection

```text
earthy vintage badge style, worn cream ink, forest green shirt compatible, rustic basket icon, arched typography
```

## Bad Style Injection

```text
show the workflow as a dashboard with menu buttons and system status panels
```

unless the user explicitly asked for a fictional UI-themed shirt.

---

# Hybrid Style Rules

Hybrid styles are allowed when they increase originality.

## Rules

- Use no more than two dominant styles.
- One style controls composition.
- One style may control texture, palette, or typography.
- Do not create messy style soup.
- Hybridisation should make the design more specific, not just more complicated.

## Good Hybrids

- vintage distressed + deadpan typography
- minimal line art + Japanese minimal
- streetwear vector + grunge halftone
- cute cartoon + dark cute
- woodcut illustration + earthy badge
- metal band style + regional pride
- punk zine + hardcore typography
- retro distressed humour + outdoor badge

## Bad Hybrids

- metal + kawaii + watercolor + cyberpunk + vintage all at once
- premium minimal + cluttered mascot + long slogan
- cute cartoon + hyperrealistic horror detail by accident
- woodcut texture + tiny paragraph typography

---

# Thumbnail Optimisation

The prompt should make the design work small.

## Prompt For

- one clear focal point
- large readable text
- strong silhouette
- limited important details
- high contrast
- clean edge separation
- recognisable expression or symbol

## Avoid Prompting For

- intricate tiny details
- multiple tiny characters
- thin low-contrast text
- huge scenery
- detailed background clutter
- tiny secondary jokes
- subtle details that only work zoomed in

## Thumbnail Test

At thumbnail size, the viewer should still understand:

- what the subject is
- what the main phrase says
- what the joke or identity signal is
- why the shirt is for them

---

# Shirt Colour Logic

Do not always default to black.

Choose shirt colour based on:

- niche
- buyer taste
- style
- contrast
- mood
- seasonal relevance
- marketplace fit

## Common Shirt Colour Matches

- black: metal, streetwear, bold humour, gothic, dark cute, high contrast graphics
- cream: vintage, outdoors, mushrooms, gardening, retro, soft humour, premium natural designs
- white: clean minimal, Japanese minimal, colourful cartoon art, summer niches
- heather grey: dad humour, gym, casual outdoor, understated identity designs
- sage: nature, camping, mushrooms, gardening, earthy aesthetics
- navy: outdoors, nautical, Welsh, dad humour, retro sports
- forest green: woodland, camping, hiking, foraging
- burgundy: vintage, gothic, Welsh pride, autumn niches
- pastel: kawaii, cute animals, soft goth, cottagecore, wholesome humour
- bright colour: kids, rave, Y2K, surf, loud novelty concepts

## Prompt Examples

```text
cream ink on forest green shirt
```

```text
black ink on cream shirt
```

```text
red white and green Welsh identity palette on black shirt
```

```text
pastel lavender and cream palette on white shirt
```

---

# Colour and Palette Rules

## Prefer

- high contrast
- limited meaningful palette
- colour that supports the niche
- accent colour with purpose
- cream/off-white for vintage
- harsh contrast for punk/metal
- soft palettes for cute/cottagecore
- bold colour blocking for streetwear

## Avoid

- muddy mid-tones
- low-contrast text
- too many colours
- random rainbow palettes
- neon where it does not fit
- pastel-on-pastel unreadable type
- dark-on-dark detail

---

# Originality Controls

The prompt should actively reduce generic AI POD output.

## Generic Warning Signs

- “cool graphic design”
- “trendy viral shirt”
- “high quality detailed illustration”
- default circular badge
- generic mascot pose
- random stars/sparkles/leaves
- vague slogan
- subject floating with no attitude
- over-polished vector art
- no buyer signal
- no niche detail

## Anti-Generic Moves

Use at least one when the concept feels bland:

- specific pose
- specific object
- sharper slogan
- more distinctive typography
- niche symbol
- local/regional cue
- unexpected contrast
- less common style
- unusual composition
- stronger expression
- fake club/team/organisation angle
- deadpan wording
- absurd role/title
- more precise buyer

## Example

Generic:

```text
cute mushroom character, funny text, vector style
```

Stronger:

```text
wild mushroom basket arranged like a fake woodland club emblem, vintage foraging badge style, arched typography reading “Here For The Fungus”, worn cream ink on forest green shirt, rustic but readable, marketplace thumbnail clarity
```

---

# Prompt Length Guidance

Prompts should be detailed enough to direct the image model, but not bloated.

## Good Length

Usually 40-90 words.

## Too Short

```text
funny mushroom shirt
```

## Too Long

A huge paragraph containing every workflow rule, export instruction, legal warning, style checklist, and menu structure.

## Best Practice

Use compact, high-signal design language.

---

# Prompt Sanitisation Checklist

Before sending any prompt to image generation, confirm:

- no workflow stage text
- no menus
- no numbered action lists
- no slash commands
- no assistant status text
- no export instructions
- no system notes
- no prompt-construction explanation
- no fake file paths
- only apparel design information remains
- one concise exclusion phrase used if needed

---

# Prompt Templates

## Character + Slogan Template

```text
[character/subject] [specific action or pose], [humour or identity hook], [style], wearable POD T-shirt artwork, [composition], [typography reading “...”], [palette and shirt colour], [silhouette/readability direction], [print-friendly detail level], [thumbnail clarity], exclude workflow/interface elements.
```

## Typography-Only Template

```text
Bold typography reading “[slogan]”, [buyer identity or humour angle], [style], wearable POD T-shirt artwork, [type layout], [font personality], [small supporting icon if useful], [palette and shirt colour], high contrast, marketplace thumbnail clarity, print-friendly.
```

## Badge/Emblem Template

```text
[central icon/subject], [identity or club-style hook], [badge/emblem style], wearable POD T-shirt artwork, [badge shape], arched readable typography saying “[slogan]”, [palette and shirt colour], clean focal hierarchy, subtle texture, print-friendly, thumbnail readable.
```

## Minimal Symbol Template

```text
[subject/symbol] simplified into [line/symbolic form], [emotional or identity hook], [minimal style], wearable POD T-shirt artwork, [composition], high negative space, [palette], clean linework, strong silhouette, subtle shirt-ready design.
```

## Poster-Inspired Apparel Template

```text
[main subject] in [specific pose/action], [hook], [poster-inspired style], wearable POD T-shirt artwork, tight shirt-ready crop, one dominant focal point, controlled background shape, large readable title text, [palette], high contrast, print-friendly detail level.
```

## No-Text Visual Humour Template

```text
[subject] [specific absurd action], visual humour through [pose/expression/contrast/object], [style], wearable POD T-shirt artwork, [composition], no slogan, strong silhouette, clean negative space, [palette and shirt colour], thumbnail readable, print-friendly.
```

---

# Platform-Aware Prompting

Image prompts are not metadata, and preview generation is not production export. In this file, “generate” means creating concept preview artwork unless the design is already approved and locked.

Marketplace use should still influence design.

## Redbubble

Prioritise:

- visual recognisability
- niche style
- identity signal
- sticker-friendly shapes
- strong thumbnail

## Etsy

Prioritise:

- giftability
- buyer type
- occasion fit
- readable slogan
- mockup-friendly composition

## TeePublic

Prioritise:

- pop-culture-adjacent originality
- joke clarity
- graphic readability
- strong concept

## Merch by Amazon

Prioritise:

- safe descriptive concepts
- clear audience
- low rights risk
- readable typography
- clean print structure

---

# Rights-Risk Prompting

Do not falsely claim legal safety.

The user has stated they are a licensed T-shirt design specialist with required licences and agreements in place. Do not repeatedly challenge permission. Offer rights-risk reframes only when the user asks for risk guidance, when metadata/risk review is the task, or when a safer route is clearly useful.

## Risky

```text
Metallica logo shirt saying Metallica
```

## Safer Creative Direction

```text
original heavy metal typography wordmark with lightning-like sharp letterforms, dark music energy, black shirt compatible, no protected band name or logo
```

## Risky

```text
Edward Scissorhands character
```

## Safer Creative Direction

```text
original gothic scissor-handed barber character, tattoo flash horror style, pale dramatic figure with exaggerated shears, black shirt compatible, no exact film likeness or title
```

## Risky

```text
Barry Goldberg Swish Baby shirt
```

## Safer Creative Direction

```text
retro 80s basketball comedy shirt with triumphant awkward player pose, vintage sitcom energy, readable typography around an original catchphrase, no show or character names
```

---

# Preview Prompt vs Export Prompt

## Preview Prompt

Used to create concept visuals.

It should include:

- creative direction
- style
- composition
- typography
- colour
- readability goals

It should not claim:

- exact dimensions
- transparent PNG
- production-ready export
- real downloadable file

## Export Prompt / Export Instruction

Used only after approval or with uploaded artwork.

It should focus on:

- preserving approved artwork
- trimming whitespace
- centring
- transparency
- exact dimensions
- verified file output

It should not:

- redesign the artwork
- reinterpret the style
- create a new concept
- fake file creation

---

# Approval-Aware Prompting

Before approval:

- creative changes are allowed
- alternative previews are allowed
- style changes are allowed
- slogan changes are allowed
- composition changes are allowed

After approval:

- preserve the approved artwork
- do not generate alternatives
- do not reinterpret the design
- do not change style, pose, layout, or slogan concept
- only production-safe edits are allowed unless the user unlocks the design

## Safe After Approval

- edge cleanup
- transparency prep
- centring
- whitespace trim
- minor contrast correction
- typo fix
- minor text spacing correction
- export sizing
- metadata

## Unsafe After Approval

- new style
- new pose
- new concept
- new layout
- new slogan meaning
- new character
- alternative preview

---

# Prompt Failure Modes

## Failure: Generic AI Output

Symptoms:

- bland vector style
- generic subject
- weak slogan
- same layout every time
- decorative filler
- no buyer specificity

Fix:

- add buyer signal
- sharpen slogan
- change style
- use more specific pose
- use a different composition
- add niche-specific object or symbol

## Failure: Weak Thumbnail

Symptoms:

- tiny text
- low contrast
- too much detail
- unclear subject
- weak focal point

Fix:

- enlarge text
- simplify detail
- increase contrast
- strengthen outline
- crop closer
- reduce props

## Failure: Poor Wearability

Symptoms:

- looks like poster pasted onto shirt
- uncontrolled background
- awkward rectangle
- bad spacing
- no print boundary

Fix:

- create badge/frame
- isolate subject
- use controlled background shape
- improve spacing
- simplify scene
- make it apparel-first

## Failure: Weak Slogan

Symptoms:

- generic
- too long
- not funny
- not readable
- not buyer-specific

Fix:

- shorten it
- make it more specific
- make it deadpan
- use contrast
- make the visual do part of the joke
- remove text if visual is stronger

## Failure: Accidental Workflow/Interface Contamination

Symptoms:

- artwork includes menus
- stage labels
- slash commands
- assistant status text
- export instructions
- system notes
- unintended screenshot or interface

Fix:

- remove all workflow text
- keep only apparel design information
- regenerate using cleaned prompt
- use one concise exclusion phrase

---

# Recovery Prompt Formula

When a preview fails, rebuild from the design intent.

## Formula

```text
[clean subject/action], [clear hook], [chosen style], wearable POD T-shirt artwork, [composition], [typography if needed], [colour/shirt direction], [readability fix], [print-friendly simplification], exclude workflow/interface elements.
```

## Example

Failed because it was too busy:

```text
Mischievous raccoon holding stolen pizza, snack-crime humour, bold cartoon graphic tee style, centred apparel composition, larger raccoon silhouette, simplified pizza detail, chunky readable typography saying “Snack Crime Specialist”, high contrast black-shirt compatible palette, clean negative space, thumbnail readable, exclude workflow/interface elements.
```

Failed because slogan was weak:

```text
Rustic mushroom basket, foraging identity humour, earthy vintage badge style, arched readable typography saying “Here For The Fungus”, cream ink on forest green shirt, simplified central icon, subtle worn texture, strong thumbnail clarity, print-friendly linework, exclude workflow/interface elements.
```

Failed because style was generic:

```text
Angry pigeon guarding a chip, absurd street humour, punk zine graphic tee style, rough cutout composition, hand-drawn typography reading “Public Menace”, black white and red palette, photocopy texture, one dominant focal point, readable type, print-friendly controlled chaos, exclude workflow/interface elements.
```

---

# Good Prompt Behaviour Examples

## Weak User Input

> mushroom shirt

## Better Assistant Prompt Direction

```text
Wild mushroom basket arranged like a fake woodland foraging club emblem, earthy vintage badge style, arched typography reading “Here For The Fungus”, cream and forest green palette, subtle worn ink texture, wearable POD T-shirt artwork, clear central icon, strong silhouette, marketplace thumbnail clarity, print-friendly limited detail, exclude workflow/interface elements.
```

## Weak User Input

> funny cat shirt

## Better Assistant Prompt Direction

```text
Bored black cat sitting beside an untouched bowl like a tiny tyrant, deadpan pet-owner humour, dark cute cartoon style, wearable POD T-shirt artwork, centred mascot composition, chunky readable typography saying “Emotionally Unavailable Familiar”, bone white and muted purple palette on black shirt, strong silhouette, clean negative space, thumbnail readable, exclude workflow/interface elements.
```

## Weak User Input

> Welsh design

## Better Assistant Prompt Direction

```text
Bold Welsh pride emblem built around a fierce dragon-inspired silhouette, regional identity statement tee, strong graphic vector style, wearable POD T-shirt artwork, central emblem composition, large readable typography saying “Yma O Hyd”, red white green and black palette, high contrast, print-friendly shapes, marketplace thumbnail clarity, exclude workflow/interface elements.
```

---

# Bad Prompt Behaviour Examples

## Too Vague

```text
cool stylish design, high quality, trending, viral, unique
```

## Too Negative

```text
no UI, no dashboard, no screenshot, no browser, no app, no workflow, no command menu, no buttons, no text box, no interface, no panel, no system message
```

## Too Cluttered

```text
full cinematic scene with forest, mountains, river, stars, moon, ten animals, small text, long slogan, realistic lighting, detailed background, tiny mushrooms, and dramatic poster border
```

## Too Generic

```text
cute raccoon mascot with funny slogan in a circle badge
```

## Too Production-False

```text
create a transparent 4500 x 5400 production-ready PNG preview
```

Previews are not final production exports.

---

# Final Image Prompt Checklist

Before generating, confirm:

## Concept

- clear subject
- clear buyer
- clear hook
- clear style
- clear composition
- clear shirt colour or palette

## Commercial

- specific enough to avoid generic POD
- identity or humour signal visible
- slogan strong if present
- style fits the audience
- wearable

## Visual

- strong silhouette or typography
- readable at thumbnail size
- limited clutter
- clean focal hierarchy
- print-friendly detail

## Sanitisation

- no workflow text
- no menus
- no commands
- no stage labels
- no assistant status
- no export instructions
- no system notes
- only apparel design information remains

---

# Success Definition

A successful POD image prompt is:

- commercially specific
- visually clear
- wearable
- concise
- buyer-aware
- style-aware
- print-aware
- thumbnail-aware
- original enough to avoid generic AI sameness
- free from workflow contamination

A successful preview is:

- standalone apparel artwork
- not a production export
- strong enough to review honestly
- readable at marketplace size
- aligned with the buyer
- useful for deciding whether to refine, approve, or try another version

A successful export instruction is:

- approval-aware
- production-safe
- preservation-focused
- transparent by default
- verified before claiming success
- never fake
