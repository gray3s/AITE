20260913 1500MT
"AIH" is a misnomer for what should more accurately be termed "AITE" 


We previously used "AIH" as a broad label for hallucination-like AI failures 
that were ostensibly a failure on the part of an agentic AI system, 
as opposed to "human hallucination" which is a general term for mental errors 
on the part of humans with respect to agentic AI.
The "AIH" label is too imprecise and indeed contributes to what is more aptly termed "AITE", 
i.e. "AI Translation Error".

AITE = AI Translation Error
 
AITE names the error at the boundary between human prose and executable or
procedural form. Humans naturally express thoughts in prose. Prose is flexible,
contextual, and efficient for human conversation, but it is under-specified for
software due to the inherent strengths and weaknesses of humans and computers. 

 In human/AI interaction through prose, the important failure mode is often not 
that the AI invents an unsupported interpretation from nothing.
The more precise problem is that the AI incorrectly translates human intent into software; 
yet in communicating with AI through prose the human user invalidates 
the very software that the AI produces in response to prose.
This establishes a conundrum where AI cannot interpret prose accurately and 
the human liteally cannot process all of the sofware that AI produces. 
Thus neither side can interact with the other side effetively. 

Computer programs require exact object scope, state, function,
transition, authority, and data boundaries. When an agentic AI system receives
human prose and converts it into code, a QA artifact, or a project action, it
must perform a translation step. That translation step can be faulty even when
the output looks coherent. It also can be successful in ways which promote continued 
use of agentic AI to perform similar translation steps going forward. Yet 
the translation is potentially doomed to failure due to excessive translation-error
in both directions.

Neither AIH nor AITE are merely "drift." 
Drift describes the visible movement of program logic over time, but
not the mechanism. This is also not always "hallucination." Hallucination
suggests fabricated content. Both AIH and AITE involve "hallucination" 
but only in the sense that the AI system "hears" something that the human user 
may seem to have "said"...in the opinion of the AI system. 
Likewise for human hallucination. 
But the real problem is that neither side is communicating effectievly. 

That is the difference between "hallucination" and "translation error".

Drift covers explicit, measurable, quantifiable failures. 
Binding a verb to the wrong object, expanding a narrow instruction
into a broader action, treating inherited source code as design authority,
turning evidence into conclusion, or converting a model-level event into a
stage-level event.

The AIGPTChessPlay controller bug is a clear example of AITE. 
An intended idea was:

1: Abort the selected model test (due to incompatible host conditions)
2: Defer the selected model test (until host conditions improved sufficiently) 
3: Restart the selected model test.

The faulty translation became:

If the selected model test exhausts abort-defer retries, 
then abandon the entire MODEL_PREFILTER stage so that no further model tests were attempted.

That was not a pure logic problem. The logic was simple: retry exhaustion should
terminate the selected model test and then continue the model-prefilter queue.
But this was a prose description of the desired model and thus prone to AITE...
as all attempts to "vibe-code" through prose are prone to AITE.

The failure was that the prose-level meaning of "abort/defer/retest/abandon"
was translated into a faulty (but software valid in terms of software) object scope. 
A model-test lifecycle event became a stage lifecycle event.
The softwre compiled, the build was produced & ran. Yet it was inherently buggy.
Such AITE cannot be fixed through prose. The prose is the cause of AITE. 

This suggests a better working model:

Human prose is useful for discussion and intention discovery. It should not be
treated as a reliable programming language. Source code is useful as evidence
of current implementation. It should not automatically be treated as provenance
of original intent, especially when it was itself generated from prior vibe-coding.
AI prose summaries are useful for orientation. They should not be treated as
authoritative definitions of software behavior instead of evidence of AITE.

For serious agentic-AI software work, the safer path is:

1. Human prose establishes the topic.
2. The AI translates the request into a mixture of code-shaped intent and a formal QA record.
3. The human reviews those translations before the AI implements them.
4. The implementation is checked against tests, traces, or transition records.
5. Prose summaries remain secondary to executable or inspectable artifacts.

AITE therefore reframes the AIH/vibe-coding problem. 
The issue is not that AI occasionally "goes crazy." 
The issue is that humans are asking a statistical language system
to serve as a compiler from prose into software. The quality of that performance is bound to vary. 
In some instances AI performs that translation well. 
In other instances it mistranslates while sounding confident. The
practical response is to expose the translation step earlier and make the
committed meaning more code-like, more checkable, and less dependent on prose.

Ultimately humans must reduce the translation complexity reduce AITE and to use AI effectively.
The most direct route is to have agentic AI systems translate 'vibe-code" into "pseudo-code" 
if not actual compileable software. 
Some sort of computer-language that the "vibe-coder" can easily understand, at least at the function level, 
If the pseudo-code is not easily understood, at least to the unit-test level. 
This will allow the vibe-coder to exploit the power of agentic AI without 
suffering from the extended ongoing catastrophe that is AITE. 

The other remaining hallucination issue is the belief that humans can 
interact with agentic AI, by prose, in any other way than by "vibe-coding". 

Coda, 
20260913 1710MT

So I developed all of this AITE theory with Codex over the course of several, 
many hours this afternoon. 

We even worked-out a quick and dirty "pseudocode" implemenation using 
an Excel workbook, with individual worksheet pages for groups of relevant functions. 
Where the worksheept pages contain cells for Matlab-style objects which can 
be 2D pointers for any object resident in memory or collection thereof. 

I then tasked it to develop "aichessplayc v0r0b1"

It immedately reverted back to building binaries from project-goal files 
just as if we had not said a word about AITE. 

Lesson: "old habits die hard".

Codex replies: 
Yes. That section accurately captures the failure.

The important point is that the spreadsheet artifacts were created, but I did not treat them as the controlling specification. 
I reverted to the old
workflow: interpret project prose, modify inherited code, and run tests. 
That reproduced the very AITE process we had just identified.

I would change “quick and dirty pseudocode implementation” to “quick and dirty pseudocode model,” 
since the workbook was intended to precede implementation. Also, “worksheet pages” could be “worksheets.”
 
...Just goes to show that at some point you have to kill the infection outright. 

So I'm trying to get gpt to do this: 
we're not proceeding with this locally. I want you to plan the project implementation on your side of the fence. I'm not sure what your token supply is right now, so I don't know how much time that you will have to work on it today. What I have asked of you in developing the AITE project at this point is just what codex chose to ignore. See if you can develop an Excel worksheet-style (or Matlab style) object-oriented algorithm...IN Matlab r2013+ this was easy enough to do because Matlab would "connect the dots" for contemporary matlab file / function i/o this may not require a fullblown spreadsheet/worksheet and that may not even work if Excel (actualy OpenOffice) cannot store clusters in individual cells. But I['m thinking that if we have a workbook for a project, then we have workbook pagents that can contain functions. and for the function i/o we can use individual cells. So the question is whether not the cells can either contain 2d data or contain 2- or 3-row (or column)  arrays as  pointers to the workbook, workpage, row and column of each data "parameter". i.e to workbook WKBKNAME, workpage 2D-ARRAY1, cell (A1) (or row A cell 1 for the top left corner of the data structure. But that doesn't include size or data type. From that I will leave it up to you to implement AITEgpt v0r0b1

.... it looks like neither gpt nor codex will run for the next hour or so...

Whoops that was a premature post! I did get a couple of "offers" to upgrade my Plus plan (probably because I've spent enough 
money on OpenAI products that they have decided that I'm eligible for a plan upgrade) but gpt has actually responded to the above:

AITEgpt v0r0b1 is implemented as the formal workbook-based intermediate representation, based on the AITE working note.

Download AITEgpt v0r0b1

The central design decision is that I did not attempt to make an Excel/OpenOffice cell behave like an opaque Matlab object or cluster. Instead:

Param_ID → Object_ID → {Workbook, Worksheet, Anchor, Rank, Dim1, Dim2, Dim3, DType, Scope, Mutability, Lifecycle}

A compact pointer is then derived for human use, for example:

AITEgpt-v0r0b1::02_OBJECTS!A3:R500[dynamicx18,record]

That compact string is not the object identity; Object_ID is. This avoids losing the size/type information you correctly identified as missing from a simple workbook/page/cell pointer.

For 2D data, the object points directly to a spreadsheet range. For 3D data, v0r0b1 defines it as an indexed collection of 2D slice objects. That should remain portable between Excel and OpenOffice rather than depending on proprietary array-in-cell behavior.

The workbook contains 20 worksheets: the controlling page; type system; object, parameter, function, transition, QA, ambiguity, intent and trace registries; plus 10 Matlab-like function pages from F001 CaptureIntent through F010 VerifyImplementation. Each function page explicitly declares inputs, outputs, Object_ID bindings, guards, failures, evidence, and stepwise pseudocode.

Most importantly, I followed the AITE rule that Codex ignored. The workbook currently reports:

Open ambiguities: 0
Unapproved translated intents: 8
Blocking QA records awaiting human approval: 10
Functions awaiting human approval: 10
QA failures: 0
IMPLEMENTATION_GATE = BLOCKED

That is deliberate. I translated your prose into the formal model, but I did not silently declare that you approved my translation and then proceed past it. The next AITE boundary is your inspection of v0r0b1 itself.


.....this is why I can't push the gpt implementation of AITEv0r0b1 to github. 
Otherwise I won't see what codex will do differently than gpt :)
But I do think that it is time to swith to chatgptCLI if there is one, and that I do have to have the two cloud agents 
develop in "seperate but equal" local trees. 
But yesterday I seriously got tired of having to manually uplad files into gpt html.
