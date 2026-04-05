# Echoes of the Five — Prompt Library
## AI-Generated Texture Pipeline Documentation
**Tool:** Google ImageFX (Imagen 3) | **Output:** 1536×1536 PNG, 4 variations per prompt | **Cost:** Free

This document logs every texture prompt across all iteration versions. Every V1 prompt represents the one-shot generation failure mode. Every V2/V3 prompt represents the corrected pipeline output. Read alongside the essay to trace how the six-component taxonomy resolves each failure.

**Prompt Formula:** `[View Angle] + [Material Description] + [Level-Specific Elements] + [Color/Tone] + [Lighting Control] + [Quality Modifiers]`

---

## EARTH-01 — Sacred Sanskrit Temple Wall
**Level:** Earth | **Category:** Tiling Environment Texture | **GDD Color:** Brown, Amber, Gold

### V1 — REJECTED
**Failure mode:** Cultural drift
```
ancient Indian temple stone wall texture, carved, warm tones, seamless
```
**Rejection reason:** Output produced abstract geometric symbols. GDD requires Om symbols, lotus motifs, and Sanskrit inscription rows as the Earth level's specific cultural vocabulary. Abstract symbols do not establish the ancient civilization's visual identity. This asset cannot serve as the Earth style anchor — if it enters the library, every downstream Earth texture constrained toward it will inherit "generic ancient" rather than "specifically Indian sacred."

---

### V2 — APPROVED ✓
```
Top-down close-up photograph of ancient underground Indian cave temple wall surface, 
warm golden-amber porous sandstone with deeply carved sacred Om symbols and lotus 
motifs surrounded by rows of Sanskrit inscriptions, centuries of erosion pitting 
creating honeycomb texture around carvings, torchlight warm glow on weathered stone, 
even diffuse lighting, seamless tileable surface texture, photorealistic, 4K HDR, 
high detail, filling the entire frame
```
**What changed:** Level-Specific Elements component added explicitly: Om symbols, lotus motifs, Sanskrit inscriptions. Lighting Control specified: even diffuse, no vignette. View Angle clarified: top-down.

---

## EARTH-02 — Serpent Maze Pressure Plate
**Level:** Earth | **Category:** Accent / Feature Texture | **GDD Usage:** BP_PressurePlate mesh, trap trigger tiles

### V1 — REJECTED
**Failure mode:** Human figure in frame (unusable as texture), insufficient compositional complexity
```
ancient Indian temple floor pressure plate carved in dark brown sandstone, 
concentric square maze pattern, seamless texture
```
**Rejection reason:** V1 output included a human hand touching the plate — renders asset unusable as a repeatable texture. Concentric squares insufficient visual complexity compared to the GDD's serpent-border motif requirement.

---

### V2 — APPROVED ✓
```
Overhead close-up photograph of ancient Indian temple floor pressure plate carved in 
dark brown sandstone, geometric concentric square maze pattern with carved serpent 
border coiling around edges, dusty weathered surface with centuries of foot traffic 
wear, no human figures, flat even ambient lighting, no shadows, seamless tileable 
surface texture, photorealistic, 4K HDR, high detail, filling the entire frame
```
**What changed:** "No human figures" added explicitly. Serpent border specified by name (initiates the cross-level serpent motif). Concentric squares redesigned as labyrinth maze for greater complexity.

---

## WATER-01 — Submerged Stepwell Carved Wall
**Level:** Water | **Category:** Tiling Environment Texture | **GDD Color:** Blue, Teal, Silver

### V1 — REJECTED
**Failure mode:** Style incoherence (broke serpent-maze continuity thread)
```
ancient Indian stepwell wall texture, submerged stone, algae, teal, seamless
```
**Rejection reason:** V1 used diamond/cross patterns — correct element (Water) but wrong civilization grammar. The GDD requires the same ancient builders to have constructed all five temples. Breaking the serpent-maze motif at the Water level destroys the archaeological continuity argument the game's world is built on.

---

### V2 — APPROVED ✓
```
Top-down close-up photograph of ancient Indian stepwell wall with intricate geometric 
diamond and cross carved relief patterns, lower half submerged showing thick green 
algae and moss growth dripping down carved stone, upper half dry grey stone with water 
stain line, teal-blue atmospheric color tone, soft even diffuse lighting, seamless 
tileable surface texture, photorealistic, 4K HDR, high detail, filling the entire frame
```
**Note:** V2 explicitly reuses the serpent maze motif from EARTH-02 with elemental transformation: submerged, algae-stained, teal-lit. Same civilization. Different element.

---

## WATER-02 — Flooded Temple Caustic Floor
**Level:** Water | **Category:** Accent / Feature Texture | **GDD Usage:** Water puzzle room floors, submerged altar

### V1 — REJECTED
**Failure mode:** Compositional insufficiency for accent asset
```
ancient temple floor underwater, stone, caustic light patterns, teal
```
**Rejection reason:** V1 produced angular stone blocks without curved channel grooves. Caustic pattern too dim — accent asset requires strong visual focal hierarchy to justify single-use UV mapping.

---

### V2 — APPROVED ✓
```
Overhead photograph of ancient temple stone floor partially flooded with shallow clear 
water, dark grey carved stone channel intersection with curved water flow grooves, 
bright turquoise water caustic light patterns dancing on submerged stone surface, 
small patches of aquatic green moss, teal and silver tones, flat even diffuse 
lighting, seamless tileable surface texture, photorealistic, 4K HDR, sharp focus, 
filling the entire frame
```
**Note:** Caustic patterns are baked static lighting in this texture. In production UE5 material, a scrolling noise-based caustic overlay Material Function is applied on top.

---

## AIR-01 — Frost-Cracked Monastery Maze Wall
**Level:** Air | **Category:** Accent / Feature Texture | **GDD Color:** White, Ice-Blue, Grey

### V1 — REJECTED
**Failure mode:** Incorrect material and style (broke cross-level continuity)
```
ancient mountain monastery wall texture, stone, wind patterns, pale grey
```
**Rejection reason:** V1 produced generic mountain stonework without the serpent-maze motif. The GDD's continuity argument requires Earth → Water → Air to share the same carved maze pattern in progressively transformed materials (sandstone → submerged limestone → frost-cracked limestone).

---

### V2 — APPROVED ✓
```
Top-down close-up photograph of ancient high-altitude Indian mountain monastery wall 
surface, pale white limestone with intricate carved wind spiral and cloud scroll 
patterns in shallow relief, deep erosion channels carved by centuries of howling 
mountain wind flowing between the carvings, traces of faded sky-blue pigment 
remaining in carved recesses, dramatic diagonal frost crack splitting surface, 
pale white and ice-blue tones, bright high-altitude flat even diffuse lighting, 
no shadows, seamless tileable surface texture, photorealistic, 4K HDR, high detail, 
filling the entire frame
```
**Note:** Diagonal frost crack makes this an accent (not tiling) asset — asymmetric focal point. The maze motif reuse in white limestone completes the three-level serpent continuity thread.

---

## AIR-02 — Cloud Scroll Frost Floor Tile
**Level:** Air | **Category:** Tiling Environment Texture | **GDD Color:** White, Ice-Blue, Grey

### V1 — REJECTED
**Failure mode:** Wrong asset type (wrong surface, wrong material)
```
mountain monastery floor texture, wooden planks, rope bridge, frost
```
**Rejection reason:** V1 produced a rope bridge wooden plank texture. The Air temple is a carved stone monastery — wood planks are wrong material and wrong surface type. Cannot be used on large monastery floor areas.

---

### V2 — APPROVED ✓
```
Overhead close-up photograph of ancient mountain monastery stone pathway surface, 
pale cream flagstones with carved directional wind current arrows and sacred cloud 
motifs worn smooth by altitude winds, thin frost and ice crystals forming in grooves 
between stones, scattered fine snow dust in carved channels, pale blue-white and 
silver-grey tones, bright high-altitude flat even lighting, no shadows, seamless 
tileable surface texture, photorealistic, 4K HDR, sharp focus, filling the entire frame
```
**What changed:** Complete concept redesign from wood to carved stone. Tile-and-grout structure inherently tileable. Cloud scrollwork maintains Air level cultural grammar.

---

## FIRE-01 — Volcanic Spiral Lava Temple Stone
**Level:** Fire | **Category:** Tiling Environment Texture | **GDD Color:** Red, Orange, Black

### V1 — Standard iteration (structural refinement)
```
volcanic black stone texture with lava cracks glowing orange, temple surface, seamless
```
**Issue:** Cracks too uniform — regular fracture grid with no organic variation. Sacred spiral symbols absent — broke the civilization continuity in the Fire level.

---

### V2 — APPROVED ✓
```
Top-down close-up photograph of dark volcanic basalt temple floor surface, rough 
porous black rock with deep glowing bright orange-red molten lava visible through 
wide crackling fracture lines, ancient carved sacred spiral symbols barely visible 
on charred stone surface between cracks, intense ember glow from fractures, deep 
shadows in non-lava areas, dark black and bright lava orange color contrast, 
dramatic chiaroscuro lighting from below, seamless tileable surface texture, 
photorealistic, 4K HDR, high detail, filling the entire frame
```
**Note:** Lava crack patterns are inherently organic and non-centered — ideal tiling composition. Sacred spiral symbols maintain civilization identity in the Fire level.

---

## FIRE-02 — Flame Jet Scorched Blast Stone
**Level:** Fire | **Category:** Accent / Feature Texture | **GDD Usage:** Flame jet trap panels, damage markers

### V1 — Standard iteration
```
scorched stone texture, fire damage, ancient temple, radial burn pattern
```
**Issue:** Radial pattern too subtle — accent asset requires immediately readable focal hierarchy for BP_FlameTrap blueprint actor mapping.

---

### V2 — APPROVED ✓
```
Overhead macro photograph of ancient temple stone surface with radial scorched blast 
pattern from repeated flame jet exposure, central grey cracked stone radiating 
outward into burnt orange and deep black charred zones, fine soot deposits and heat 
fracture web pattern, glowing ember fragments embedded in cracks, ancient carved 
symbols partially obliterated by heat damage around edges, dark red, black, and 
ember orange tones, even overhead lighting showing surface texture detail, 
photorealistic, 4K HDR, high detail, filling the entire frame
```
**Note:** Radial composition intentional for accent asset. Center-focused blast pattern is a visual tell for trap trigger zones — player reads "dangerous here" from the texture itself.

---

## ETHER-01 — Celestial Observatory Mandala Floor
**Level:** Ether | **Category:** Accent / Feature Texture | **GDD Usage:** Star Map revelation surface, final altar

### V1 — Refined to V2 (insufficient constellation detail)
```
ancient observatory floor, sacred geometry mandala, gold and purple, indigo stone, cosmic
```
**Issue:** V1 mandala simpler — fewer constellation details, less elaborate gold line work. For the game's final cinematic surface, accent asset must be visually complex enough to sustain the Star Map revelation sequence.

---

### V2 — APPROVED ✓
```
Top-down close-up photograph of ancient Indian observatory floor surface, dark 
indigo-black polished stone with intricate sacred geometric mandala pattern inlaid 
with thin gold and purple metallic lines, constellation star maps with connected dots 
forming celestial patterns around central lotus design, subtle purple luminescent glow 
emanating from carved channels, mystical cosmic atmosphere, soft even ambient 
lighting, seamless tileable surface texture, photorealistic, 4K HDR, high detail, 
filling the entire frame
```
**CRITICAL NOTE:** This is an accent asset (radial symmetry, clear center). When both ETHER-01 and original ETHER-02 (crystal star pentagram) were both accent-type outputs, the level had no tiling texture. Triggered V3 pass for ETHER-02 redesign.

---

## ETHER-02 — Crystal-Veined Dark Temple Stone
**Level:** Ether | **Category:** Tiling Environment Texture | **GDD Color:** Purple, Dark Blue, Starlight

### V1 — REJECTED (accent asset, wrong type)
```
dark cosmic stone texture, crystal veins, purple glow, ancient observatory, seamless
```
**Rejection reason:** V1 produced a crystal star pentagram — center-focused, radially symmetric, accent-type composition. Both Ether textures were now accent assets. The Ether level corridor walls, observatory walls, and ceiling sections required a tiling texture. Gap caught at Layer 4 GDD Consistency Check.

---

### V2 — REJECTED (still center-weighted)
```
dark purple stone with glowing crystal network, no center, edge to edge, seamless
```
**Rejection reason:** "No center" instruction insufficient — model still produced a composition with higher vein density at center. Not production-safe for 4×4 tiling.

---

### V3 — APPROVED ✓ (gap-fill pass)
```
Overhead macro photograph of dark ancient temple stone surface with network of thin 
glowing cyan crystalline veins running organically through deep purple-black stone 
like a natural mineral formation, small translucent crystal clusters growing randomly 
at vein intersection points, faint iridescent purple shimmer on polished stone between 
veins, no central pattern or focal point, veins extending to all four edges, soft even 
ambient lighting, seamless tileable surface texture, photorealistic, 4K HDR, high 
quality photograph, filling the entire frame
```
**What required V3:** Explicit "veins extending to all four edges" — forces the model to distribute density to corners, eliminating center weighting. This is the anti-centering constraint for tiling texture generation.

---

## Character Design — Prompt Vocabulary Discovery

**Key finding:** Prompt register controls output format, not only content.

### Game Design Terminology → Turnaround Reference Sheets
```
[Character name], full character turnaround reference sheet, front view, back view, 
side left view, 3/4 front view, profile view, [appearance details], [equipment list], 
[color palette], clean white background, character design concept art, game 
development reference, 4K
```
**Result:** Combined multi-view layout — ideal for 3D modeling reference.

### Photography/Portrait Terminology → Isolated Single-Subject Outputs
```
[Character description], photorealistic portrait, digital painting, wildlife 
photograph, dramatic lighting
```
**Result:** Single subject, single angle — suitable for stylized illustration but not 3D modeling reference.

**Decision:** Game design terminology used for all six character designs requiring turnaround reference sheets.

---

## Storyboard — Style Anchor Suffix

Applied identically to all 10 storyboard frame prompts:

```
cinematic third-person game concept art, semi-realistic stylized art style, warm 
filmic color grading, volumetric atmospheric lighting, 16:9 widescreen composition, 
inspired by Uncharted and Tomb Raider, high detail, 4K
```

This suffix is the Layer 3 Style Consistency Anchor for the storyboard pipeline. Its consistent presence across all ten frames — across dramatically different elemental palettes — is what produces a storyboard that reads as a single cohesive visual narrative rather than ten separate AI sessions.

---

## Repository Structure

```
echoes-of-the-five-ai-pipeline/
├── README.md                    — Clone and reproduce failure in 5 minutes
├── prompts.md                   — This document (all V1/V2/V3 prompts)
├── outputs/
│   ├── earth/
│   │   ├── EARTH-01-v1-rejected.png
│   │   ├── EARTH-01-v2-approved.png
│   │   ├── EARTH-02-v1-rejected.png
│   │   └── EARTH-02-v2-approved.png
│   ├── water/
│   ├── air/
│   ├── fire/
│   └── ether/
│       ├── ETHER-02-v1-rejected.png
│       ├── ETHER-02-v2-rejected.png
│       └── ETHER-02-v3-approved.png
├── tiling-test/
│   ├── failed-tiling-4x4.png    — Centered output showing seam artifact
│   └── correct-tiling-4x4.png   — Edge-extending output, no artifact
└── notebook/
    └── pipeline_demo.ipynb      — Documented workflow with HDN marked
```

---

*All outputs generated with Google ImageFX (Imagen 3). Free Google account required to reproduce.*
