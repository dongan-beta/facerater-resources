# Reading facial proportions from a photo: follow the endpoints

A ratio becomes useful when you can see what was measured. A number such as 0.75 is incomplete until you know its numerator, denominator and capture conditions. This guide shows how to inspect a front-view measurement and decide what to compare next.

Written by the **FaceRater product team**, 29 October 2026. This is a companion to our tools, not an independent review or a clinical measurement standard.

## First ask: which two spans produced the ratio?

FaceRater's [facial proportions calculator](https://face-rater.com/tools/facial-ratios?utm_source=github&utm_medium=resource&utm_campaign=reading_proportions) opens these five ratios and three visible vertical bands without a report purchase:

| Reading | Numerator | Denominator | What to check on the diagram |
|---|---|---|---|
| Visible face length / width | Upper visible forehead landmark to chin | Cheek width | The upper endpoint is a detected forehead point, **not the hairline**. |
| Eye spacing / eye width | Distance between the inner eye corners | Mean width of the two visible eyes | Compare the gap with the eye spans used in the same photo. |
| Jaw / cheekbone width | Detected front-view jaw width | Cheek width | Keep both cheek endpoints and the jaw outline visible. |
| Mouth / cheekbone width | Mouth-corner distance | Cheek width | Expression changes the numerator. |
| Nose / mouth width | Visible nose-wing width | Mouth-corner distance | This denominator is **mouth width**, not face width. A smile can change the ratio even when the nose span barely moves. |
| Upper, middle and lower visible bands | Each forehead–brow–nose–chin interval | Their combined visible height | These describe the detector's visible window; they are not three equal anatomical thirds. |

The same headline phrase can describe different calculations in different products. Before comparing two tools, check their endpoint definitions rather than assuming matching labels mean matching measurements.

## A worked example: why the denominator matters

These are **invented teaching numbers**, not a customer's result or a target range.

Suppose the marked jaw span is 240 pixels and cheek width is 320 pixels:

`240 ÷ 320 = 0.75`

If you uniformly resize the photo by half, the spans become 120 and 160 pixels. The ratio remains 0.75. This is why a ratio is more useful than an isolated pixel distance when displaying the same photograph at different sizes.

Now suppose a second photograph yields a jaw span of 240 and cheek width of 300:

`240 ÷ 300 = 0.80`

The ratio increased because its **denominator changed**. It does not establish that the person's jaw became wider. Inspect pose, perspective, expression and the detector's endpoints before attributing a difference to a physical change. Uniform image resizing is not the same thing as changing camera distance or viewing angle.

## What a front-view jawline reading can answer

The [front-view jawline tool](https://face-rater.com/tools/jawline-rating?utm_source=github&utm_medium=resource&utm_campaign=reading_proportions) opens the jaw/cheek ratio, two paired contour readings, the lower visible band and the head-roll reading. It helps inspect width and left/right alignment in that photograph.

It does **not** measure a side-profile gonial angle, chin projection or a clinical bone dimension. Turning a front-view width ratio into one of those claims would add information that the image does not supply. The tool's declared balance score is a product calculation; it is not a diagnostic threshold or a population attractiveness percentile.

For a practical styling comparison, choose one question: do you prefer more width around the temples, softer framing near the jaw, or less volume at the sides? Compare the silhouette at the same displayed size. A width reading can help explain that preference; it cannot choose the preference for you.

## Capture a second photo that answers one question

1. Keep the camera, distance, eye-level position and lighting as similar as practical.
2. Keep the forehead, eyes, cheeks and jaw visible, with a relaxed expression.
3. Change one thing you want to inspect, such as hair framing. Record other changes rather than pretending they did not happen.
4. Read the actual spans before comparing the overall score.
5. If an endpoint is obscured or appears misplaced, choose a clearer photo rather than treating its number as precise.

Use the [two-photo comparison worksheet](COMPARISON-WORKSHEET.md) to write down the change **before** looking at the result. A more flattering photograph and a physical change are different explanations; the score alone cannot distinguish them.

## Turn a reading into a decision

| If you notice… | Check first | A useful next action |
|---|---|---|
| The nose/mouth ratio changes between photos | Mouth expression and corner placement | Repeat with a similar relaxed expression. |
| One jaw contour looks different | Head position, hair and shadows | Retake with both sides visible before drawing conclusions. |
| The upper band seems unexpectedly short | Where the forehead landmark begins | Read it as a visible-window measurement, not hairline height. |
| Several ratios change together | A shared denominator, camera distance and pose | Inspect the common span instead of assuming several separate changes. |
| You prefer one hair silhouette | Length, side volume and face framing | Save that preference as a stylist discussion aid; do not chase a numerical target. |

The full report adds illustrated chapters, explanations and styling experiments. The free tools already expose the named readings above, so you can inspect the measurement before deciding whether the additional report is useful.

## What the sources support

- [Google's Face Landmarker documentation](https://developers.google.com/edge/mediapipe/solutions/vision/face_landmarker/web_js) describes landmark-coordinate output for images and video. It documents the detector capability; it does not validate a beauty score or establish ideal ratios.
- [Jenkins, White, Van Montfort and Burton (2011), *Variability in photos of the same face*](https://pubmed.ncbi.nlm.nih.gov/21890124/) reports substantial differences among photographs of the same people, including variation in attractiveness judgments. This supports caution about representing someone with one photo; it does not establish FaceRater's scoring accuracy.
- [FaceRater's measurement method](https://face-rater.com/methodology) defines our product calculations and their limits. A photo-based geometry reading does not establish health, personality or how everyone will perceive a person.

Free scan processing runs in the browser. Saving a device report, creating an authenticated cloud report and requesting AI hairstyle concepts are separate actions with different storage and processing requirements; see the live site's [data controls](https://face-rater.com/privacy).
