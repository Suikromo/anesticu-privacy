# VT — Character Sheet Prompts (siap generate)

3 prompt final untuk maskot Vital Threshold. Tiap prompt = MASTER STYLE PROMPT + blok karakter (bible bagian 3 & 4). Generate **satu lembar berisi 5 pose/ekspresi** per karakter, rasio 16:9. Simpan hasil terbaik: `char-moni-master.png`, `char-cardio-master.png`, `char-alvi-master.png`. (BACTI belum dipakai di VT-001 → tunda.)

**Cara pakai saat MCP tersambung:** panggil `mcp__Higgs__generate_image` (model image default GPT Image 2 / Nano Banana untuk konsistensi karakter — cek `models_explore` bila perlu), 1 prompt per karakter. Setelah jadi, kunci sebagai reference image untuk semua shot berikutnya.

---

## 1) MONI — patient-monitor robot (pemandu)
```
STYLE: flat vector illustration, medical educational infographic style,
strictly 2D, no photorealism, no 3D rendering, no depth of field.

PALETTE: dark abyss teal background (#062A2E), deep teal (#0E4249),
oxblood red (#7A1526), arterial red (#C42B3C), bone white (#E6DCC8),
amber (#FFB23F) and cyan (#35E0D8) as glow accents only.
Maximum 5 colours in frame.

LIGHTING: all light emanates from INSIDE the subject, bioluminescent
deep-sea logic. Background stays dark and unlit. No sun, no lamps,
no sky gradients, no rim light from outside.

FORMS: capsule and rounded-rectangle construction, visible seam lines
dividing organic and mechanical parts, thin bone-white outlines on
subjects only, flat fills with a single soft inner glow layer.
No gradient mesh, no texture, no noise.

COMPOSITION: centred subject, generous negative space, 16:9,
clean vector edges, no text in image.

SUBJECT: character sheet, 5 variations in one image, evenly spaced
on dark teal background.

Character name: MONI. A small friendly patient-monitor robot.
Body: a rounded-rectangle screen unit in bone white with a visible
horizontal seam across the middle, standing on two short capsule legs,
two short capsule arms. Screen face occupies 70% of the front,
glowing softly from within in cyan.

The five variations show the screen face displaying:
1. neutral: a calm flat cyan waveform line
2. alert: an amber jagged waveform, screen tinted amber
3. alarm: a red chaotic waveform, screen tinted arterial red
4. flatline: a single flat cyan horizontal line, screen dimmed
5. explaining: a small rising bar chart in amber

No text, no numbers, no letters anywhere in the image.
```

## 2) CARDIO — heart character (pembawa emosi)
```
STYLE: flat vector illustration, medical educational infographic style,
strictly 2D, no photorealism, no 3D rendering, no depth of field.

PALETTE: dark abyss teal background (#062A2E), deep teal (#0E4249),
oxblood red (#7A1526), arterial red (#C42B3C), bone white (#E6DCC8),
amber (#FFB23F) and cyan (#35E0D8) as glow accents only.
Maximum 5 colours in frame.

LIGHTING: all light emanates from INSIDE the subject, bioluminescent
deep-sea logic. Background stays dark and unlit. No sun, no lamps,
no sky gradients, no rim light from outside.

FORMS: capsule and rounded-rectangle construction, visible seam lines
dividing organic and mechanical parts, thin bone-white outlines on
subjects only, flat fills with a single soft inner glow layer.
No gradient mesh, no texture, no noise.

COMPOSITION: centred subject, generous negative space, 16:9,
clean vector edges, no text in image.

SUBJECT: character sheet, 5 variations in one image, evenly spaced
on dark teal background.

Character name: CARDIO. A stylised heart character built from
capsule shapes in oxblood red with bone-white seam lines marking
the four chambers. Two large simple eyes in bone white.
Four short capsule vessel-stubs at the top acting as limbs.
Glows from within in amber, brightest at the centre.

The five variations show:
1. healthy: upright, steady, even amber glow
2. straining: leaning forward, glow pulsing brighter, sweat-drop shapes
3. failing: slumped, glow dimmed to faint amber, eyes half closed
4. fibrillating: body shape slightly distorted, glow flickering chaotically
5. recovering: upright again, glow returning, one eye open

No text, no numbers, no letters anywhere in the image.
```

## 3) ALVI — alveolus character (paling visual)
```
STYLE: flat vector illustration, medical educational infographic style,
strictly 2D, no photorealism, no 3D rendering, no depth of field.

PALETTE: dark abyss teal background (#062A2E), deep teal (#0E4249),
oxblood red (#7A1526), arterial red (#C42B3C), bone white (#E6DCC8),
amber (#FFB23F) and cyan (#35E0D8) as glow accents only.
Maximum 5 colours in frame.

LIGHTING: all light emanates from INSIDE the subject, bioluminescent
deep-sea logic. Background stays dark and unlit. No sun, no lamps,
no sky gradients, no rim light from outside.

FORMS: capsule and rounded-rectangle construction, visible seam lines
dividing organic and mechanical parts, thin bone-white outlines on
subjects only, flat fills with a single soft inner glow layer.
No gradient mesh, no texture, no noise.

COMPOSITION: centred subject, generous negative space, 16:9,
clean vector edges, no text in image.

SUBJECT: character sheet, 5 variations in one image, evenly spaced
on dark teal background.

Character name: ALVI. A small round alveolar sac character,
bone white, translucent, with a thin cyan capillary net wrapping
around its outer surface. Two small simple eyes. A single short
capsule airway stem at the top. Glows softly from within in cyan.

The five variations show:
1. healthy: fully inflated sphere, bright even cyan glow
2. collapsed: deflated and crumpled, glow nearly gone
3. flooded: half filled with a flat oxblood-red fluid level inside,
   glow muted and reddish
4. inflamed: swollen, outer wall thickened, arterial red edge glow
5. recruited: re-inflating, glow returning from the centre outward

No text, no numbers, no letters anywhere in the image.
```

---

## Setelah 3 sheet jadi
1. Pilih hasil terbaik tiap karakter → simpan `char-*-master.png` (aset paling berharga).
2. Kunci sebagai reference image untuk semua shot di `VT-001-shotlist.md`.
3. Update `workplan.md` (tandai character sheet ✅).
4. Lanjut generate ~48 shot VT-001 (36 NEW + 9 CHAR + 3 TPL).
