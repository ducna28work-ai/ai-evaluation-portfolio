# Multimodal Artifact Evaluation

A practical project demonstrating structured evaluation of AI-generated multimodal artifacts, including websites, applications, games, visualizations, presentations, reports, and other interactive outputs.

## Purpose

The project demonstrates how two AI-generated artifacts can be evaluated independently against the same task requirements and then compared at an overall level.

The evaluation process separates:

- Task understanding
- Artifact availability
- Loading and rendering behavior
- Interactive functionality
- Rubric-level evaluation
- Overall comparison
- Rejection handling
- Evaluation QA

## Evaluation Model

Each task contains:

- A prompt
- Input materials
- Response A
- Response B
- Rubric criteria
- Overall evaluation dimensions

The two responses are evaluated independently before making an overall comparison.

## Evaluation Workflow

**Read Prompt → Review Input Materials → Open Response A → Open Response B → Check Loading State → Test Artifact → Evaluate Rubric Criteria → Review Overall Dimensions → QA → Submit**

## Artifact Types

The framework can be applied to different AI-generated outputs, including:

- Websites
- Applications
- Games
- Interactive visualizations
- Presentations
- Reports
- Code-based interfaces
- Other multimodal artifacts

## Loading vs Broken Interface

An evaluator should distinguish between an artifact that is still loading and one that is actually broken.

### Loading

Possible indicators include:

- Spinner
- Progressive rendering
- Partial content appearing
- Interface continuing to load

The evaluator should allow sufficient time for the artifact to render before making a failure judgment.

### Broken or Blank

Examples include:

- Persistent blank screen
- Persistent black screen
- Error message preventing use
- Only a small unusable interface fragment
- Indefinite loading with no usable output

A broken or blank interface may qualify for rejection according to the evaluation rules.

## Interactive Testing

Artifacts should not be evaluated only from their initial screen.

Depending on the artifact, testing may include:

- Buttons
- Menus
- Forms
- Scrolling
- Navigation
- Mouse interaction
- Keyboard controls
- Arrow keys
- WASD
- Space
- Enter
- Focus behavior

For interactive games, the evaluator should test the actual interaction rather than judging only the initial visual presentation.

## Rejection Logic

Rejection should be reserved for cases where the artifact is fundamentally unavailable for evaluation.

Examples include:

- One or both outputs have a broken or blank interface
- An output cannot become usable after the required loading period

Poor quality should not automatically result in rejection.

Examples that should normally remain available for scoring include:

- Incomplete output
- Poor visual quality
- Missing requirements
- Broken individual interactions
- Poor game mechanics
- Low-quality content

These are quality issues and should be reflected in the rubric evaluation.

## Independent Rubric Evaluation

Each rubric criterion should be evaluated independently for Response A and Response B.

Possible outcomes include:

- A: Good
- A: Bad
- B: Good
- B: Bad

Both responses may receive Good.

Both responses may receive Bad.

One response may receive Good while the other receives Bad.

The rubric should not be treated as a winner-selection mechanism at the individual criterion level.

## Rubric Editing

When rubric editing is available, changes should be made only when justified.

### Remove

Remove a criterion when:

- It cannot be evaluated from the available prompt or input materials.
- It is clearly not applicable.

### Clarify

Clarify a criterion when a small wording change makes the requirement objectively evaluable without changing its original intent.

### Correct

Correct a criterion when it directly conflicts with the prompt or references material that does not exist.

Rubric changes should:

- Preserve the original intent.
- Apply equally to Response A and Response B.
- Be supported by the available task information.
- Never be changed to favor one response.

## Overall Evaluation

After independent rubric evaluation, the evaluator compares the overall quality of the two artifacts.

The overall decision should consider:

- Rubric performance
- Task fulfillment
- Artifact usability
- Interactive behavior
- Overall quality

The overall comparison should be based on the evidence collected during evaluation.

## QA Principles

A high-quality evaluation should:

- Inspect both responses.
- Allow sufficient loading time.
- Distinguish loading from broken interfaces.
- Test interactive functionality.
- Evaluate rubric criteria independently.
- Avoid rejecting outputs solely because they are poor quality.
- Modify rubrics only when justified.
- Apply rubric changes equally.
- Base overall comparisons on observed evidence.

## Dataset

The included dataset is synthetic and demonstrates evaluation records without exposing production task data, real artifacts, customer information, or confidential project details.

## Limitations

The repository does not contain the original production artifacts or internal evaluation platform.

The project demonstrates the evaluation methodology and QA framework using synthetic records.

## Status

The multimodal artifact evaluation framework, synthetic dataset, rubric, and QA analysis are complete.
