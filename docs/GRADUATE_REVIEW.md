# Fresh computer-science graduate persona review

**Review date: 2026-10-01. This is an AI-simulated learner perspective, not an independent human study or a measured learning-gain result.** The assumed learner can run beginner Python but has no prior expertise in this infrastructure domain.

## Does the beginning actually start at zero?

I start with a user request and its result, then learn that logs describe events, metrics summarize measurements, and a trace relates operations. Spans, identities, duration units, counters, gauges, and histogram buckets are introduced before pipelines, sampling, and incident diagnosis.

Every concept includes an analogy, worked example, misconception, glossary, practice explanation, and a four-state narrated animation. Play, Pause, Back, Next, pace, and the slider let me predict a change and inspect it. Reduced-motion handling and a readable state transcript provide another way to follow the explanation.

## Can I do more than remember names?

By the final levels I can inspect parent-child relationships, distinguish one operation's failure from caller symptoms, propagate context, reason about overlapping durations and the critical path, recognize N+1 calls, and justify sampling and attribute choices. The real Python SDK produces spans, metrics, and correlated logs. A separate example crosses real HTTP boundaries and executes a SQLite query.

Five-question assessments require at least 80%, and a badge additionally requires the practical plan to pass two scenario variants. Later assessments unlock in order. Python recomputes practical results and owns the progress transaction; an AI answer or submitted success flag cannot award a badge. All lessons can still be previewed.

In the browser I advanced the request animation and ran the first trace experiment. The interface displayed nine SDK spans across three trace IDs, three correlated logs, and a populated waterfall. Separately, the official Collector accepted the three connected spans from the actual HTTP example.

## Changes made after the review

The review tightened the distinction between correlated symptoms and a cause, made selected-topic questions such as 'explain this' use their current lesson, and emphasized that deleting a user.email attribute does not sanitize message bodies or every other privacy-bearing field. Authored tutor explanations are labelled clearly; optional generation is not treated as verified truth.

Shared improvements include retrieval of glossary terms and practice explanations, clearer quiz distractors, selected-topic tutor context, vertically stacked mobile animation scenes, and badge ordering that remains 0 through 10 on narrow screens. These changes address observed usability and reasoning gaps; they are not proof of human learning gains.

## What a badge establishes, and what remains

Passing establishes the included, bounded learning objectives and guided lab checks. Worked solutions and source code are available, attempts can be repeated, and these are not proctored exams. A badge alone cannot establish retention, independent diagnosis, or production expertise.

The UI's services and N+1 workload are small local models. The debug exporter is not a storage or search backend, and default experiments do not implement tail sampling or validate production load. My next step is to instrument a new application and verify broken and restored propagation without copying the sample.

The [independent capstone](INDEPENDENT_CAPSTONE.md) asks for a new, evidence-based report with a manual rubric. Complete it with the worked plan closed and have a knowledgeable person review the reasoning. There is no claim that an actual learner has passed it.

## Verdict

The course supports a path from beginner vocabulary to a capable practitioner of its included labs and advanced reasoning exercises. Calling that universal production mastery would overstate the evidence. The final transfer challenge and supervised practice make the remaining step explicit.

See [validation evidence](VALIDATION.md) for what actually executed.
