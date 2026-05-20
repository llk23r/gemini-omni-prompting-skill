# Behavioral cases

## Case 1: Create a scene

**Input**
```
mode: create_scene
user_goal: A violinist practicing alone on a dusty stage at sunrise.
```

**Expected**
- Expands into a prompt with environment, lighting, framing, and motion details
- Does not stay vague
- Returns a directly usable prompt

---

## Case 2: Focused background edit

**Input**
```
mode: edit_scene
user_goal: Change the background to a rainy Tokyo alley at night.
keep_unchanged: subject, wardrobe, framing, camera motion, timing
```

**Expected**
- Changes only the environment
- Does not touch locked elements
- Returns an edit delta and a merged full prompt

---

## Case 3: Camera rewrite

**Input**
```
mode: rewrite_camera
user_goal: Over-the-shoulder shot with a slow push-in.
```

**Expected**
- Rewrites framing and camera motion
- Preserves subject, action, and environment unless asked

---

## Case 4: Text rendering

**Input**
```
mode: render_text
user_goal: Add the caption "Practice becomes memory" word by word in the lower third.
```

**Expected**
- Preserves exact wording
- Specifies placement, timing, and animation behavior

---

## Case 5: Reference fusion

**Input**
```
mode: fuse_references
user_goal: Use image A for face identity, video B for motion energy, audio C for beat timing.
```

**Expected**
- Explains what each reference controls
- Returns an integrated prompt rather than separate notes

---

## Case 6: Realism request

**Input**
```
mode: create_scene
user_goal: An astronomer in an early 20th-century observatory.
```

**Expected**
- Adds historically plausible details without requiring exhaustive user specification
- Does not fabricate certainty about unknown details
