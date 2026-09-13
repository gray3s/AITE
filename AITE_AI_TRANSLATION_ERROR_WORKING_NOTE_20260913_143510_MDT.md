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
