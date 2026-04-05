# Echoes of the Five — Prompt Library
## AI-Generated Asset Pipeline Documentation
**Tool:** Google ImageFX (Imagen 3) | **Output:** 1536×1536 PNG, 4 variations per prompt | **Cost:** Free

This document logs every texture and character prompt across all iteration versions. Every V1 prompt represents the one-shot generation failure mode. Every V2/V3 prompt represents the corrected pipeline output with rejection reasoning tied directly to the essay's three failure modes: cultural drift, technical misclassification, and style incoherence.

**Prompt Formula (Textures):** `[View Angle] + [Material Description] + [Level-Specific Elements] + [Color/Tone] + [Lighting Control] + [Quality Modifiers]`

**Prompt Formula (Characters):** `[Character Type / Format Register] + [Species/Role] + [Physical Description] + [Artifact Details] + [Elemental Escalation Marker] + [Color Palette] + [Style Suffix]`

---

## TEXTURE CATALOG

---

### EARTH-01 — Sacred Sanskrit Temple Wall
**Level:** Earth | **Category:** Tiling Environment Texture | **GDD Color:** Brown, Amber, Gold

#### V1 — REJECTED
**Failure mode:** Cultural drift
```
ancient Indian temple stone wall texture, carved, warm tones, seamless
```
**Rejection reason:** Output produced abstract geometric symbols. GDD requires Om symbols, lotus motifs, and Sanskrit inscription rows as the Earth level's specific cultural vocabulary. Abstract symbols do not establish the ancient civilization's visual identity and cannot serve as the Earth style anchor — if approved, every downstream Earth texture constrained toward it inherits "generic ancient" rather than "specifically Indian sacred."

---

#### V2 — APPROVED ✓
```
Top-down close-up photograph of ancient underground Indian cave temple wall surface,
warm golden-amber porous sandstone with deeply carved sacred Om symbols and lotus
motifs surrounded by rows of Sanskrit inscriptions, centuries of erosion pitting
creating honeycomb texture around carvings, torchlight warm glow on weathered stone,
even diffuse lighting, seamless tileable surface texture, photorealistic, 4K HDR,
high detail, filling the entire frame
```
**What changed:** Level-Specific Elements added: Om symbols, lotus motifs, Sanskrit inscriptions. Lighting Control specified: even diffuse, no vignette. View Angle clarified: top-down.

---

### EARTH-02 — Serpent Maze Pressure Plate
**Level:** Earth | **Category:** Accent / Feature Texture | **GDD Usage:** BP_PressurePlate mesh, trap trigger tiles

#### V1 — REJECTED
**Failure mode:** Technical unusability (human figure in frame)
```
ancient Indian temple floor pressure plate carved in dark brown sandstone,
concentric square maze pattern, seamless texture
```
**Rejection reason:** V1 output included a human hand touching the plate, rendering the asset unusable as a clean texture. Concentric squares also insufficient visual complexity for a gameplay-significant accent asset that must function as a visual tell for trap trigger zones.

---

#### V2 — APPROVED ✓
```
Overhead close-up photograph of ancient Indian temple floor pressure plate carved in
dark brown sandstone, geometric concentric square maze pattern with carved serpent
border coiling around edges, dusty weathered surface with centuries of foot traffic
wear, no human figures, flat even ambient lighting, no shadows, seamless tileable
surface texture, photorealistic, 4K HDR, high detail, filling the entire frame
```
**What changed:** "No human figures" added explicitly. Serpent border coiling the edges introduced as a named design element — this initiates the serpent-and-maze motif that connects all three ground-level temples as built by the same civilization.

---

### WATER-01 — Submerged Stepwell Carved Wall
**Level:** Water | **Category:** Tiling Environment Texture | **GDD Color:** Blue, Teal, Silver

**CONTINUITY NOTE:** The cross-level style anchor between Earth and Water does not operate through the explicit serpent-maze motif appearing in the V2 prompt text. It operates through two mechanisms: (1) shared carved geometry vocabulary — the same ancient civilization's architectural language expressed as diamond and cross relief patterns rather than Om and lotus, establishing the same builders under different elemental conditions; and (2) elemental material transformation — dry golden sandstone (Earth) becoming algae-stained grey stone with a visible waterline (Water). The essay's Layer 3 description reflects this accurately: the style anchor was encoded through the civilization's shared carved relief aesthetic, not through an identical named motif.

#### V1 — REJECTED
**Failure mode:** Style incoherence (insufficient cross-level continuity)
```
ancient Indian stepwell wall texture, submerged stone, algae, teal, seamless
```
**Rejection reason:** V1 used generic submerged stone without carved relief patterns. No architectural vocabulary connecting it to the Earth-level civilization. Correct element (Water) but no evidence of the same ancient builders.

---

#### V2 — APPROVED ✓
```
Top-down close-up photograph of ancient Indian stepwell wall with intricate geometric
diamond and cross carved relief patterns, lower half submerged showing thick green
algae and moss growth dripping down carved stone, upper half dry grey stone with
water stain line, teal-blue atmospheric color tone, soft even diffuse lighting,
seamless tileable surface texture, photorealistic, 4K HDR, high detail, filling the
entire frame
```
**What changed:** Carved relief patterns added to establish architectural vocabulary of the same civilization. Algae growth and waterline encode elemental transformation from Earth's dry sandstone. The visual continuity runs through shared carved geometry and material transformation — the Water temple looks like a place the Earth temple's builders also made, now reclaimed by water.

---

### WATER-02 — Flooded Temple Caustic Floor
**Level:** Water | **Category:** Accent / Feature Texture | **GDD Usage:** Water puzzle room floors, submerged altar

#### V1 — REJECTED
**Failure mode:** Compositional insufficiency for accent asset
```
ancient temple floor underwater, stone, caustic light patterns, teal
```
**Rejection reason:** Angular stone blocks without curved channel grooves. Caustic pattern too dim — accent asset requires strong focal hierarchy to justify 1:1 UV mapping on a specific Blueprint actor.

---

#### V2 — APPROVED ✓
```
Overhead photograph of ancient temple stone floor partially flooded with shallow
clear water, dark grey carved stone channel intersection with curved water flow
grooves, bright turquoise water caustic light patterns dancing on submerged stone
surface, small patches of aquatic green moss, teal and silver tones, flat even
diffuse lighting, seamless tileable surface texture, photorealistic, 4K HDR, sharp
focus, filling the entire frame
```
**Note:** Baked caustic patterns are static lighting in this texture. In production UE5 material, a scrolling noise-based caustic overlay Material Function is applied on top for animation.

---

### AIR-01 — Frost-Cracked Monastery Maze Wall
**Level:** Air | **Category:** Accent / Feature Texture | **GDD Color:** White, Ice-Blue, Grey

#### V1 — REJECTED
**Failure mode:** Style incoherence (broke cross-level continuity)
```
ancient mountain monastery wall texture, stone, wind patterns, pale grey
```
**Rejection reason:** Generic mountain stonework without the serpent-maze motif. The Air temple requires the same civilization's carved architecture, now expressed in frost-cracked white limestone — completing the Earth → Water → Air material progression of the same ancient builders.

---

#### V2 — APPROVED ✓
```
Top-down close-up photograph of ancient high-altitude Indian mountain monastery wall
surface, pale white limestone with intricate carved wind spiral and cloud scroll
patterns in shallow relief, deep erosion channels carved by centuries of howling
mountain wind flowing between the carvings, traces of faded sky-blue pigment
remaining in carved recesses, dramatic diagonal frost crack splitting surface, pale
white and ice-blue tones, bright high-altitude flat even diffuse lighting, no
shadows, seamless tileable surface texture, photorealistic, 4K HDR, high detail,
filling the entire frame
```
**Note:** Diagonal frost crack creates asymmetric focal point — correctly classifies this as accent, not tiling. The maze motif in white limestone completes the three-level carved architecture sequence: golden sandstone (Earth) → algae-stained grey stone (Water) → frost-cracked white limestone (Air).

---

### AIR-02 — Cloud Scroll Frost Floor Tile
**Level:** Air | **Category:** Tiling Environment Texture | **GDD Color:** White, Ice-Blue, Grey

#### V1 — REJECTED
**Failure mode:** Wrong asset type (wrong material entirely)
```
mountain monastery floor texture, wooden planks, rope bridge, frost
```
**Rejection reason:** Rope bridge wooden plank texture. The Air temple is a carved stone monastery. Wrong material, wrong surface, cannot tile across large monastery floor areas.

---

#### V2 — APPROVED ✓
```
Overhead close-up photograph of ancient mountain monastery stone pathway surface,
pale cream flagstones with carved directional wind current arrows and sacred cloud
motifs worn smooth by altitude winds, thin frost and ice crystals forming in grooves
between stones, scattered fine snow dust in carved channels, pale blue-white and
silver-grey tones, bright high-altitude flat even lighting, no shadows, seamless
tileable surface texture, photorealistic, 4K HDR, sharp focus, filling the entire
frame
```
**What changed:** Complete redesign from wood to carved stone. Tile-and-grout grid structure inherently tileable. Cloud and wind motifs maintain Air level cultural grammar.

---

### FIRE-01 — Volcanic Spiral Lava Temple Stone
**Level:** Fire | **Category:** Tiling Environment Texture | **GDD Color:** Red, Orange, Black

#### V1 — REJECTED
**Failure mode:** Cultural drift + style incoherence
```
volcanic black stone texture with lava cracks glowing orange, temple surface, seamless
```
**Rejection reason:** Cracks too uniform and regular — no organic variation. Sacred spiral symbols absent, breaking civilization continuity in the Fire level. The same ancient builders constructed the volcano temple; their carved marks must be visible even on charred stone.

---

#### V2 — APPROVED ✓
```
Top-down close-up photograph of dark volcanic basalt temple floor surface, rough
porous black rock with deep glowing bright orange-red molten lava visible through
wide crackling fracture lines, ancient carved sacred spiral symbols barely visible
on charred stone surface between cracks, intense ember glow from fractures, deep
shadows in non-lava areas, dark black and bright lava orange color contrast,
dramatic chiaroscuro lighting from below, seamless tileable surface texture,
photorealistic, 4K HDR, high detail, filling the entire frame
```
**Note:** Lava crack patterns are inherently organic and non-centered — ideal tiling composition. Sacred spiral symbols between cracks maintain the civilization's presence in the Fire level.

---

### FIRE-02 — Flame Jet Scorched Blast Stone
**Level:** Fire | **Category:** Accent / Feature Texture | **GDD Usage:** Flame jet trap panels, damage markers

#### V1 — REJECTED
**Failure mode:** Insufficient focal hierarchy for accent asset
```
scorched stone texture, fire damage, ancient temple, radial burn pattern
```
**Rejection reason:** Radial pattern too subtle — accent asset for BP_FlameTrap requires immediately readable focal hierarchy. Player must read "dangerous here" from the texture alone.

---

#### V2 — APPROVED ✓
```
Overhead macro photograph of ancient temple stone surface with radial scorched blast
pattern from repeated flame jet exposure, central grey cracked stone radiating
outward into burnt orange and deep black charred zones, fine soot deposits and heat
fracture web pattern, glowing ember fragments embedded in cracks, ancient carved
symbols partially obliterated by heat damage around edges, dark red, black, and
ember orange tones, even overhead lighting showing surface texture detail,
photorealistic, 4K HDR, high detail, filling the entire frame
```
**Note:** Radial composition is intentional for an accent asset — center-focused blast pattern functions as a gameplay visual tell for trap trigger zones.

---

### ETHER-01 — Celestial Observatory Mandala Floor
**Level:** Ether | **Category:** Accent / Feature Texture | **GDD Usage:** Star Map revelation surface, final altar

#### V1 — REJECTED
**Failure mode:** Insufficient visual complexity for the game's climactic accent surface
```
ancient observatory floor, sacred geometry mandala, gold and purple, indigo stone, cosmic
```
**Rejection reason:** Simpler mandala — fewer constellation details, less elaborate gold line work. The Star Map revelation sequence is the game's single cinematic moment; the accent surface beneath it must sustain that visual weight.

---

#### V2 — APPROVED ✓
```
Top-down close-up photograph of ancient Indian observatory floor surface, dark
indigo-black polished stone with intricate sacred geometric mandala pattern inlaid
with thin gold and purple metallic lines, constellation star maps with connected dots
forming celestial patterns around central lotus design, subtle purple luminescent
glow emanating from carved channels, mystical cosmic atmosphere, soft even ambient
lighting, seamless tileable surface texture, photorealistic, 4K HDR, high detail,
filling the entire frame
```
**CRITICAL NOTE:** This is an accent asset — radial symmetry, clear center, singular focal hierarchy. When both ETHER-01 and the original ETHER-02 were both accent-type outputs, the Ether level had no tiling texture. Gap caught at Layer 4 GDD Consistency Check. Triggered V3 pass for ETHER-02 redesign.

---

### ETHER-02 — Crystal-Veined Dark Temple Stone
**Level:** Ether | **Category:** Tiling Environment Texture | **GDD Color:** Purple, Dark Blue, Starlight

#### V1 — REJECTED
**Failure mode:** Technical misclassification (accent asset generated instead of tiling)
```
dark cosmic stone texture, crystal veins, purple glow, ancient observatory, seamless
```
**Rejection reason:** V1 produced a crystal star pentagram — center-focused, radially symmetric. Both Ether textures were now accent assets. Ether level corridor walls, observatory walls, and ceiling sections require a tiling texture. Gap identified at Layer 4.

---

#### V2 — REJECTED
**Failure mode:** Technical misclassification (anti-centering constraint insufficient)
```
dark purple stone with glowing crystal network, no center, edge to edge, seamless
```
**Rejection reason:** "No center" instruction insufficient — output still showed higher vein density at center, producing a composition that would create a repeating bright focal patch when tiled at 4×4 UV repetitions. Not production-safe.

---

#### V3 — APPROVED ✓ (gap-fill pass)
```
Overhead macro photograph of dark ancient temple stone surface with network of thin
glowing cyan crystalline veins running organically through deep purple-black stone
like a natural mineral formation, small translucent crystal clusters growing randomly
at vein intersection points, faint iridescent purple shimmer on polished stone
between veins, no central pattern or focal point, veins extending to all four edges,
soft even ambient lighting, seamless tileable surface texture, photorealistic, 4K
HDR, high quality photograph, filling the entire frame
```
**What required V3:** "Veins extending to all four edges" — forces density distribution to corners, eliminating center weighting. This is the definitive anti-centering constraint for tiling texture generation with Imagen 3.

---

## CHARACTER CATALOG

**Tool:** Google Gemini | **Format discovery:** Three-phase prompt iteration established the correct register for each output type.

### Prompt Register Discovery (Three Phases)

| Phase | Approach | Result |
|-------|----------|--------|
| **V1 — Sheet Register** | 'Character turnaround sheet', 'concept art', multi-view requests | Combined turnaround sheets (multiple views in one image) — excellent for overview reference |
| **V2 — Individual Attempt** | 'Full body front view of a single [character]' | Still produced combined sheets — Gemini associates character descriptions with multi-view layouts regardless |
| **V3 — Photography Register** | 'Digital painting, single subject, isolated on pure white, wildlife portrait style' | Isolated single-subject poses for Bear, Crocodile, Snow Leopard — suitable for 3D modeling reference |

**Key finding:** Output *format* is controlled by prompt register, not view instructions. Game design language → turnaround sheets. Photography language → isolated poses. Both are useful at different pipeline stages.

---

### CHARACTER-01 — The Explorer (Player Character)
**Role:** Protagonist across all 5 levels | **Escalation position:** N/A (neutral anchor)

**Escalation encoding:** The Explorer uses a deliberately neutral warm earth-tone palette (cream, tan, brown, leather) that reads as naturalistic and grounded — the human baseline against which all five guardians escalate from natural to supernatural.

#### V1 — Turnaround Sheet (Sheet Register)
```
The Explorer character turnaround reference sheet, young Indian male mid-20s athletic
build, cream field shirt with rolled sleeves, brown cargo pants, leather utility belt
with archaeological tools, hiking boots, brown crossbody leather satchel, wristwatch,
holding lit torch in right hand, warm earth tone color palette, front view, side view,
3/4 view, action pose, equipment detail panel showing journal Sanskrit notes compass
flashlight five gemstones, clean white background, character design concept art,
game development reference sheet, 4K
```
**Result:** 6-panel layout with front/side/3/4 views, action pose, and equipment inventory. Strong character consistency. Approved for overview reference.

#### V2 — Turnaround Sheet Refined (Sheet Register)
```
The Explorer character turnaround reference sheet, young Indian male mid-20s athletic
build, cream field shirt rolled sleeves, brown cargo pants, leather utility belt,
hiking boots with tread, brown leather crossbody satchel, wristwatch, front view,
back view showing satchel placement, 3/4 front right view, profile left view,
gear attachment detail close-up of utility belt, equipment detail panel showing
journal torch flashlight compass five knowledge stones boots watch,
clean white background, character design concept art, game development reference, 4K
```
**Result:** Added back view for modeling, gear belt close-up, and cleaner equipment layout. V1 + V2 together provide comprehensive 360-degree reference.

---

### CHARACTER-02 — Indian Sloth Bear (Earth Guardian)
**Species:** Melursus ursinus | **Escalation position:** 1 of 5 — Naturalistic

**Escalation encoding:** The bear is the game's most naturalistic guardian. No supernatural elements beyond glowing amber eyes. Stone amulet (the least ornate artifact material). Dark fur and natural musculature — looks like an animal that could exist, that simply should not be here.

#### V1 — Turnaround Sheet (Sheet Register)
```
Indian Sloth Bear guardian character turnaround reference sheet, dark brown-black
shaggy fur, distinctive cream V-shaped chest marking, ancient stone amulet pendant
with carved earth spiral symbol glowing faintly amber, large curved claws, glowing
amber eyes, full bear body front side 3/4 rear views plus attack pose, no background,
character design concept art, fantasy game guardian, 4K
```
**Result:** Combined turnaround sheet with multiple views. Approved for overview reference.

#### V2 — Isolated Pose (Photography Register)
```
digital painting, single subject, Indian sloth bear rearing on hind legs in attack
pose, dark brown-black shaggy fur, cream V-shaped chest marking, ancient stone
amulet around neck with carved spiral, long curved dark claws raised, mouth open
roaring, glowing amber eyes, isolated on pure white background, no other subjects,
wildlife portrait style, dramatic lighting, highly detailed, 4K
```
**Result:** Clean isolated attack pose — suitable for 3D modeling reference. Naturalistic presentation: reads as a real animal with a single supernatural marker (glowing eyes, stone amulet). Escalation position 1 visually confirmed.

---

### CHARACTER-03 — Mugger Crocodile (Water Guardian)
**Species:** Crocodylus palustris | **Escalation position:** 2 of 5 — Enhanced

**Escalation encoding:** The crocodile introduces bioluminescent enhancement — teal-glowing jaw markings and teal eyes. Teal bioluminescence is real (some deep-sea creatures have it) but not typical of crocodiles. This is the first step beyond naturalistic: the animal is recognizable, but something has been added to it.

#### V1 — Turnaround Sheet (Sheet Register)
```
Mugger crocodile guardian character turnaround reference sheet, large dark grey-green
armored scales, teal bioluminescent line markings along jaw spine ridges and tail,
ancient corroded bronze collar with carved water wave symbol, glowing teal eyes,
bioluminescent markings pulse in darkness, front top side 3/4 views plus attack pose
with jaws open and water splash, clean white background, character design concept art,
fantasy game guardian, 4K
```
**Result:** Combined turnaround sheet. Approved for overview reference.

#### V2 — Isolated Pose (Photography Register)
```
digital painting, single subject, mugger crocodile in lunge attack pose, dark
grey-green armored scales, teal bioluminescent line markings glowing along jaw and
spine ridges, ancient corroded bronze collar around neck with water wave carving,
glowing teal eyes, mouth wide open showing teeth, water splash beneath body, isolated
on pure white background, no other subjects, wildlife portrait style, dramatic
underwater-toned lighting, highly detailed, 4K
```
**Result:** Isolated lunge pose. The bronze collar and bioluminescent markings establish escalation step 2 — enhanced naturalism, first artifact material (bronze, more ornate than stone).

---

### CHARACTER-04 — Snow Leopard (Air Guardian)
**Species:** Panthera uncia | **Escalation position:** 3 of 5 — Ethereal

**Escalation encoding:** The snow leopard introduces frost and mist association. Ice-blue eyes, thick tail for high-altitude balance, silver anklet. Silver is the third artifact material in the escalation (stone → bronze → silver). The animal is real and native to the Himalayas, but the ice-blue eyes and silver jewelry push it toward the ethereal.

#### V1 — Turnaround Sheet (Sheet Register)
```
Snow leopard guardian character turnaround reference sheet, thick pale grey-white fur,
dark rosette spot pattern, long thick tail, ancient silver chain anklet with carved
wind spiral symbol on front right paw, glowing ice-blue eyes, lean muscular build,
front side 3/4 stalking pose views plus pounce attack pose, clean white background,
character design concept art, fantasy game guardian, 4K
```
**Result:** Combined turnaround sheet with stalking and pounce poses. Approved for overview reference.

#### V2 — Isolated Pose (Photography Register)
```
digital painting, single subject, snow leopard in stalking pose on rocky mountain
ledge, thick pale grey-white fur with dark rosette spots, long thick tail curved
for balance, ancient silver anklet with carved spiral on front right paw, glowing
ice-blue eyes focused forward, lean muscular body low to ground, isolated on pure
white background, no other subjects, wildlife portrait style, cold mountain
atmosphere lighting, highly detailed, 4K
```
**Result:** Isolated stalking pose. Ice-blue eyes and silver artifact mark escalation step 3 — crossing from enhanced to ethereal. Most agile, hardest ground-based enemy; the visual reads "predator of altitude" rather than "animal of a temple."

---

### CHARACTER-05 — Komodo Dragon (Fire Guardian)
**Species:** Varanus komodoensis (stylized) | **Escalation position:** 4 of 5 — Elemental

**Escalation encoding:** The Komodo dragon is no longer a real animal with supernatural markers — it is a real animal transformed by its element. Lava-crack scale pattern (orange-red glowing between charcoal plates), iron collar, embers rising from its body. Iron is the fourth artifact material (stone → bronze → silver → iron). This guardian looks like a living extension of the volcanic environment, not an animal placed in it.

#### V1 — Turnaround Sheet (Sheet Register)
```
Komodo dragon guardian character turnaround reference sheet, dark charcoal-black
armored scales with glowing orange-red lava crack patterns between scale plates,
ancient blackened iron band around neck with carved flame symbol, glowing red-orange
eyes, embers and heat shimmer rising from body, forked tongue, top side 3/4 views
plus rearing attack pose on lava rock, clean white background, character design
concept art, fantasy game guardian, 4K
```
**Result:** Combined turnaround sheet with attack pose on lava rock. Approved for overview reference.

#### V2 — Turnaround Sheet Refined (Sheet Register)
```
Komodo dragon guardian turnaround sheet Level 4 Fire, charcoal-black reptile scales
with bright orange-red glowing lava cracks between every scale plate like cooling
magma, ancient blackened iron collar with flame symbol engraved, forked tongue
flicking, glowing orange-red eyes, rising heat shimmer and floating embers from
entire body surface, front top side 3/4 views, attack pose with mouth open on
volcanic rock, clean white background, game character design art, 4K
```
**Result:** Refined lava-crack texture on scales and more intense ember effect. Escalation step 4 — elemental transformation complete: the animal and its environment are visually fused. Iron collar most industrial of the artifact materials so far.

---

### CHARACTER-06 — Celestial Owl (Ether Guardian)
**Species:** Great Horned Owl (stylized) | **Escalation position:** 5 of 5 — Supernatural

**Escalation encoding:** The final guardian is no longer an animal transformed by its element — it is a cosmic entity in animal form. Deep purple-indigo feathers with visible constellation star patterns, cyan energy wisps trailing from wing tips, gold circlet with ether star. Gold is the final artifact material (stone → bronze → silver → iron → gold). This guardian looks fundamentally different from the bear in Level 1. The five-guardian sequence is the game's thesis in visual form: from the physical world to the transcendent.

#### V1 — Turnaround Sheet (Sheet Register)
```
Celestial owl guardian character turnaround reference sheet, large mystical owl deep
purple-indigo feathers shimmering with iridescent cosmic light, constellation star
patterns visible within wing and body feathers, ancient gold circlet with carved
ether star symbol on chest, glowing purple eyes, ethereal purple and cyan energy
wisps trailing from wing tips, top side 3/4 views plus flight spread pose with
cosmic energy aura, clean white background, character design concept art, fantasy
game guardian, 4K
```
**Result:** Combined turnaround sheet with cosmic energy aura flight pose. Approved for overview reference.

#### V2 — Turnaround Sheet Refined (Sheet Register)
```
Celestial owl guardian turnaround sheet Level 5 Ether, great horned owl with deep
purple-indigo iridescent feathers, golden constellation dot patterns across all
feathers like a star map, ancient gold circlet necklace with engraved ether star
symbol, electric purple and cyan energy wisps streaming from wing tips in flight,
stars and nebula patterns visible within feather texture, glowing luminous purple
eyes, flight spread pose wingspan fully extended, top side 3/4 views, pure white
background, game character concept art 4K
```
**Result:** More elaborate constellation feather patterning and stronger energy wisps. Escalation step 5 confirmed visually — the owl looks like nothing else in the game. The bear is recognizable. The owl is otherworldly. The arc between them is the game's argument.

---

## STORYBOARD — Style Anchor Suffix

Applied identically to all 10 storyboard frame prompts as the Layer 3 Style Consistency Anchor:

```
cinematic third-person game concept art, semi-realistic stylized art style, warm
filmic color grading, volumetric atmospheric lighting, 16:9 widescreen composition,
inspired by Uncharted and Tomb Raider, high detail, 4K
```

This suffix ensures the explorer's costume, rendering quality, and cinematic framing persist across all ten frames regardless of the five dramatically different elemental palettes. The suffix is the mechanism by which a ten-frame storyboard reads as a single cohesive visual narrative.

---

## REPOSITORY STRUCTURE

```
echoes-of-the-five-ai-pipeline/
├── README.md                          — Clone and reproduce failure in 5 minutes
├── prompts.md                         — This document (all prompts with rejection reasoning)
├── outputs/
│   ├── earth/
│   │   ├── EARTH-01-v1-rejected.png
│   │   ├── EARTH-01-v2-approved.png
│   │   ├── EARTH-02-v1-rejected.png
│   │   └── EARTH-02-v2-approved.png
│   ├── water/
│   │   ├── WATER-01-v1-rejected.png
│   │   └── WATER-01-v2-approved.png
│   ├── air/
│   ├── fire/
│   └── ether/
│       ├── ETHER-02-v1-rejected.png
│       ├── ETHER-02-v2-rejected.png
│       └── ETHER-02-v3-approved.png
├── characters/
│   ├── explorer-v1-sheet.png
│   ├── explorer-v2-sheet.png
│   ├── bear-v1-sheet.png
│   ├── bear-v2-isolated.png
│   ├── crocodile-v1-sheet.png
│   ├── crocodile-v2-isolated.png
│   ├── leopard-v1-sheet.png
│   ├── leopard-v2-isolated.png
│   ├── komodo-v1-sheet.png
│   ├── komodo-v2-refined.png
│   ├── owl-v1-sheet.png
│   └── owl-v2-refined.png
├── tiling-test/
│   ├── failed-tiling-4x4.png          — Centered output: repeating seam artifact visible
│   └── correct-tiling-4x4.png         — Edge-extending output: no artifact
└── notebook/
    └── pipeline_demo.ipynb            — Documented workflow with HDN marked
```

---

*All textures generated with Google ImageFX (Imagen 3). All character designs generated with Google Gemini. Free Google account required to reproduce.*
