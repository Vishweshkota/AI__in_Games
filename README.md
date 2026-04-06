# Echoes of the Five: AI Concept Art Pipeline

**CSYE 7270 Take-Home Midterm | Category A — AI Ideation**  
**Student:** Vishwesh Kota | **NU ID:** 002470987

Companion repository for the essay *"The Prompt Is the Pipeline: Why One-Shot AI Concept Art Fails Ancient Indian Fantasy Game Environments — and What to Do Instead."*

## Topic Claim

> After reading this piece, a practitioner will understand structured multi-iteration prompt engineering as an AI concept art pipeline well enough to design a prompt taxonomy that enforces GDD consistency, cultural specificity, and technical asset requirements across a full production asset library — without making the compounding errors of cultural drift, technical misclassification, and style incoherence that emerge from treating AI image generation as a one-shot process.

## Reproduce the Failure (Under 5 Minutes)

1. Clone this repo
2. Open `promts/prompts.md` and copy the **ETHER-02 V1** prompt
3. Paste into [Google ImageFX](https://aitestkitchen.withgoogle.com/tools/image-fx) (free Google account required)
4. Observe: centered mandala or crystal pattern — an accent-type output
5. Now copy the **ETHER-02 V3** prompt from the same file
6. Generate again and compare: edge-extending organic veins, no focal center — a tileable output
7. Tile both outputs 4×4 in any image editor to see the grid artifact in V1 and seamless tiling in V3

## Repository Structure

```
AI_IN_GAMES/
├── README.md
├── Author_Note/
│   └── authors_note.md
├── Eddy_review/
│   ├── Initial_Old/
│   └── eddy_final_audit.md
├── Essays/
│   ├── Initial_Old/
│   └── ai_concept_art_pipeline_essay.md
├── Images/
│   ├── Air/
│   ├── Batch_test/
│   ├── Characters/
│   ├── Earth/
│   ├── Ether/
│   ├── Fire/
│   └── Water/
├── notebook/
│   └── pipeline_demo.ipynb
├── promts/
│   ├── Initial_Old/
│   ├── prompts.md
│   └── figure-architect-complete-output.md
└── Tiling_test/
    ├── corrected-tiling-4x4.png
    └── failed-tiling-4x4.png
```

## Key Deliverables

| Deliverable | Location |
|---|---|
| **Technical Essay** (~2,150 words) | `Essays/ai_concept_art_pipeline_essay.md` |
| **Demo Notebook** (Jupyter) | `notebook/pipeline_demo.ipynb` |
| **Prompt Library** (all V1/V2/V3) | `promts/prompts.md` |
| **Eddy Audit Trail** | `Eddy_review/` |
| **All Generated Assets** | `Images/` (organized by level) |
| **Tiling Test** (4×4 grid proof) | `Tiling_test/` |
| **Author's Note** (3-page reflection) | `Author_Note/` |

## Human Decision Nodes

Two documented Human Decision Nodes appear in the demo notebook (`pipeline_demo.ipynb`):

1. **HDN #1 — EARTH-01 Rejection:** AI produced elaborately carved Indian temple sculpture — culturally Indian but not the GDD's specific vocabulary (no Om, no lotus, no Sanskrit). Rejected. V2 regenerated with explicit cultural register.

2. **HDN #2 — ETHER-02 Three-Pass Iteration:** V1 produced an environment scene (not a texture). V2 produced a texture with center-weighted vein density. V3 added "veins extending to all four edges" — the definitive anti-centering constraint. Only V3 is tileable.

## Tools Used

- **Google ImageFX** (Imagen 3) — All texture generation (free)
- **Google Gemini** — All character design generation (free)
- **Bookie the Bookmaker** — Essay drafting
- **Eddy the Editor** — Essay audit (4 revision cycles documented in `Eddy_review/`)
- **Figure Architect** — Figure zone analysis and prompt generation
- **Unreal Engine 5** — Game engine (Echoes of the Five)

## License

All AI-generated images produced via Google ImageFX and Google Gemini. Per Google Terms of Service, users retain rights to generated outputs. All prompt engineering, iteration methodology, pipeline design, and documentation are original work by the student.

## Demo Link
https://youtu.be/KqG2r604RT8

## Unreal Project Link
https://northeastern-my.sharepoint.com/:u:/g/personal/kota_vi_northeastern_edu/IQDK3ClWjR6-T62Oyw4-9-O6AYAp2Z44ePTd0zYST-2qZAw?e=N04S8l
