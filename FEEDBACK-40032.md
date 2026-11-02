# Feedback 40032 — pain points and corrections

HitApp: Call Judging (`hitapp.html`)

## Pain points and corrections

| Pain point | Correction |
|---|---|
| Call type (PA or MA) was not shown | Added Call Type at the top using placeholder `${CallType}` next to Call ID |
| Transcript panel was short (`200px`) and questions sat below it | Increased transcript height to `400px`. On wide screens, questions sit beside the transcript (`.layout` flex). On narrow screens they stack |
| Tone rating (1–5) had no meaning | Added a short rubric under Q2: **1 = rude, 5 = excellent** |
| Q1 and Q2 could be submitted empty | Q1 (radio) and Q2 (select) are required. Submit is blocked with a clear error if either is missing. Q2 starts with “Select a rating” so a choice is not pre-filled |
| Comments were optional even when the task was not completed | Comments are required when Task Completed = **No**; submit is blocked with a clear error otherwise |
| Submit button had no styling | Submit uses a solid button style (blue background, white text, padding, rounded corners, hover state) |

## Notes

- Existing field names were kept: `TaskCompleted`, `ToneRating`, `Comments`.
- Markup and CSS stay simple (Arial, basic classes), matching the previous file.
- Questions were wrapped in a `<form>` so submit and validation work.
