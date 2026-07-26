# Training Planning

[← AI connectors](EN-AI-Connectors-and-Tokens) · [Contents](English) · [Next: Nutrition planning →](EN-Nutrition-Planning)

## Correct sequence

A complete training plan is created in three stages:

1. **Create the plan parameters and events**
2. **Generate phases**
3. **Generate workouts for every phase**

Phases alone do not contain individual training sessions.

## Creating your first plan

<!-- code-ref:
  - lib/features/plans/ui/my_plans_screen.dart::MyPlansScreen
  - lib/features/plans/ui/plan_project_editor_dialog.dart::showPlanProjectEditorDialog
  - lib/features/plans/model/plan_project_draft.dart::PlanProjectDraft
-->

1. Open **Plan**, then use the calendar icon to open **My plans**.
2. Select **New plan**.
3. Choose the **plan type**: nutrition, training, or training with coordinated
   nutrition.
4. Enter the start and end date of the complete plan.
5. Define the main goal as an A race with name, date, target, and sport. Add B
   and C races where appropriate.
6. Under **Structure**, select sports and available weekdays or times of day
   for each sport.
7. Under **Events**, add all known restrictions and special periods.
8. Save these plan parameters first.

## Add events before generating phases

<!-- code-ref:
  - lib/features/plans/model/plan_event_type.dart::PlanEventType
  - lib/features/plans/ui/plan_event_type_ui.dart
-->

Available events include:

- B and C races
- vacation
- illness
- injury
- training camp
- work travel
- recovery block
- other

Enter a meaningful name, a date or period and, for **Other**, a description.
This allows the AI to account for the event when distributing training load
and recovery.

If a vacation or another important event is added later, update the plan and
have the affected phases and workouts reviewed or optimised again.

## Generate phases

After saving the plan parameters, select **✨ Phases** on the plan. PaceKeeper
AI uses its integrated OpenAI connection to propose a periodisation.

Before applying it, verify:

- Is the complete plan period covered without gaps?
- Are A, B, and C goals handled correctly?
- Are vacations, illnesses, work travel, and other events considered?
- Are progressive load, recovery, peak, and race week distributed sensibly?

Alternatively, ask Claude through the connector to create or revise the phases
of the existing plan. Example:

> Review my plan, consider every event, and create suitable training phases
> through my A goal.

The same external workflow is intended for ChatGPT after approval.

## Generate workouts for every phase

Select **✨ Trainings** on **each phase**, then check:

- sport and workout content
- date, time, and duration
- intensity and load distribution
- recovery days
- compatibility with work and private events
- vacations, illness, injury, and races

Repeat until every phase contains individual sessions. Workouts can be created
and adjusted by the integrated AI or externally through Claude and, later,
ChatGPT.

## Review changes

AI suggestions are shown as a preview before being applied. **Apply** writes
the suggested changes; **Discard** leaves the existing plan unchanged. Where
available, **Undo** reverts the most recently applied change. Open the history
icon to review previous changes.

[← AI connectors](EN-AI-Connectors-and-Tokens) · [Contents](English) · [Next: Nutrition planning →](EN-Nutrition-Planning)

