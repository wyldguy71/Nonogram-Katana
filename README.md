# Nonogram-Katana
This is a tracker for Nonogram Katana. It tracks buildings, technologies, quests, dependencies, costs, character requirements, collections, craftifacts, recommended building order, and shows what is Ready, One Away, etc.

# Nonograms Katana Tracker

## Player Instructions

### What This Tracker Does

The Nonograms Katana Tracker is designed to help you determine what you can work on now, what is coming next, and what resources you need to continue progressing through the game.

The tracker follows dependencies between:

* Buildings and building levels
* Technologies
* Quests and quest objectives
* Citadel upgrades
* Collections
* Craftifacts
* Character levels and skills
* Other game states and progression requirements

As you update your progress, the tracker automatically recalculates which targets are **COMPLETED**, **READY**, or **BLOCKED**.

Most of your normal interaction with the workbook takes place on four tabs:

1. **Dashboard**
2. **Player**
3. **Checklist**
4. **cost checklist**

The other tabs primarily contain game data and calculations used by the tracker.

---

# Getting Started

When using the tracker for the first time, update your information in this order:

1. Update the **Player** tab.
2. Update completed items on the **Checklist** tab.
3. Update resources already paid on the **cost checklist** tab.
4. Return to the **Dashboard**.

Once those three areas reflect your current game, the Dashboard should give you an overview of your current progression.

---

# Player Tab

The **Player** tab contains information about your character that cannot be determined from the normal completion checklist.

Currently this includes:

* Character Level
* Cartographer level
* Cooking level

Enter your current value for each item in the **Value** column.

For example, if your character is level 80, enter:

`80`

beside Character Level.

The tracker uses these values automatically when checking requirements such as Character Level 40 or Cartographer Level 3. You do not need to separately mark each lower character level as completed.

### Player Type

The Player tab also contains the **Player Type** selection.

Choose:

* **Active**
* **Passive**

This controls which building progression order is shown in the tracker.

The recommended building order is based on the game's recommended progression and differs depending on whether you play actively or rely more heavily on passive income.

Changing this selection automatically changes the recommended building order shown elsewhere in the workbook.

---

# Checklist Tab

The **Checklist** is the primary place where you record completed game progress.

Each row represents a trackable target such as:

* Building level
* Technology
* Quest state
* Collection
* Craftifact
* Citadel upgrade
* Other trackable game state

## PlayerCompleted

Use the **PlayerCompleted** column to indicate that you have completed an item in the game.

Set the value to **TRUE** when the item is complete.

Leave it **FALSE** until it has actually been completed.

You generally should not need to modify any of the calculated columns.

### Important

Some progression states are calculated automatically and should not be manually recreated.

For example, character-level requirements are calculated from the **Player** tab.

Likewise, some automatic targets are calculated from their dependencies rather than requiring a manual check.

---

## PlayerSort

The **PlayerSort** column allows you to assign your own priority to targets.

Lower numbers have higher priority.

For example:

* `1` = highest priority
* `2` = second priority
* `3` = third priority

You do not need to assign a number to every item.

The Dashboard uses PlayerSort when displaying certain lists, allowing you to control the order in which targets appear.

This is useful if several things are available but you have decided that one particular building, technology, quest, or other target is more important to you.

---

## Recommended

For buildings, the **Recommended** column shows the recommended construction order based on the Player Type selected on the Player tab.

If **Active** is selected, the Active recommendation order is used.

If **Passive** is selected, the Passive recommendation order is used.

This value is informational. You are not required to follow the recommended order.

---

## Successors

The **Successors** column identifies items that depend on the current target.

This can be useful when deciding what to complete next.

For example, completing one state or upgrade may unlock several later targets. The Successors field allows you to see what progression is waiting behind that requirement.

---

## ChainAwareStatus

This field shows the current calculated progression status of the target while considering its dependency chain.

The tracker calculates this automatically.

Do not manually edit it.

---

# Cost Checklist Tab

The **cost checklist** tracks individual resources required to purchase or complete targets.

A target may require several different resources, so a single target can have multiple rows.

For example, an upgrade might require:

* Coins
* Planks
* Steel
* Mechanisms
* Blueprints

Each resource is tracked separately.

## PlayerPaid

This is the primary field you update on this tab.

Set **PlayerPaid** to TRUE after you have paid or committed that particular resource requirement in the game.

Leave it FALSE if the resource is still required.

This allows partially funded targets to be tracked correctly.

For example, if an upgrade requires six resources and you have already supplied four of them, mark those four rows TRUE and leave the remaining two FALSE.

The Dashboard will then show that target as partially funded and identify the remaining resources.

### Important

Mark a resource as paid based on whether it has actually been committed to the target in the game, not simply because you currently possess enough of that resource.

The purpose of this checklist is to track what the target still requires.

---

# Dashboard

The **Dashboard** is the main player-facing overview.

It combines progression, dependencies, costs, quests, and player priorities into several sections.

You generally should not type directly into Dashboard results. They are calculated from the rest of the tracker.

---

# Current Cost

The **Current Cost** section shows READY targets that still have unpaid resource requirements.

It includes:

* **Target** – Name of the target
* **Type** – Building, Technology, Quest, Collection, Craftifact, Citadel, etc.
* **Sort** – Your PlayerSort priority
* **Funded** – How much of the target's cost has already been paid
* **Remaining** – Number of resource requirements still unpaid
* **Cost Details** – Remaining resources and quantities

Targets are ordered using **PlayerSort**, allowing you to place the things you care about most near the top.

A target disappears from Current Cost when all of its required resources have been marked paid.

---

# One Away

The **One Away** section identifies targets that are only **one dependency away** from becoming available.

This is useful for planning ahead.

Rather than only showing what you can do now, One Away shows what is sitting immediately behind your current progression.

The section identifies:

* Target
* Target Type
* Missing requirement
* Relevant cost information

For example, if a building upgrade only requires one additional technology, quest, state, or building level before becoming READY, it can appear here.

This is one of the most useful sections for answering:

**"What should I work on now if I want to unlock more things?"**

---

# Summary

The **Summary** section provides a quick count of progression throughout the tracker.

It includes counts such as:

* Completed
* Ready
* One Away
* Blocked
* Funded Ready
* Unfunded Ready

Use this section as a quick health check of your overall progression.

---

# Open Quests

The **Open Quests** section displays quests that are currently active and their outstanding objectives.

The two primary columns are:

* **Active Quest**
* **Outstanding Objective**

A quest can appear multiple times when it has multiple unfinished objectives.

As objectives are completed through the appropriate Checklist entries or other tracked progression, they disappear from the outstanding-objective list.

This section is particularly useful for chapter quests and quests with several simultaneous requirements.

---

# Pending Actions

The **Pending Actions** section highlights actions that can be taken and what those actions unlock.

It contains:

* **Action**
* **Unlocks**

Use this section to identify progression choices that may immediately open additional content.

It is especially useful when several possible actions are available and you want to know which ones have useful successors.

---

# Funded Not Complete

The **Funded not Complete** section identifies targets for which all required costs have been paid but the target itself has not yet been marked complete.

This is a useful reminder.

If something appears here, check the game to determine whether:

* the upgrade still needs to finish,
* another in-game action is required, or
* you simply forgot to mark the target complete on the Checklist.

Once the target is completed and recorded, it should disappear from this section.

---

# Resource Lookup

The Dashboard includes a **Select Resource** tool.

Use the dropdown to choose a resource.

Only resources currently needed by READY, unpaid targets are available for selection.

After selecting a resource, the tracker displays the READY targets that currently require that resource and the quantity required for each.

This is useful when deciding where to spend a resource.

For example, if several READY targets require Mechanisms, selecting **mechanism** allows you to see which targets are competing for them.

This turns the Dashboard into a quick answer to:

**"What currently needs this resource?"**

---

# Recommended Tab

The **Recommended** tab contains the recommended building progression for both Active and Passive play styles.

The tracker uses canonical TargetIDs internally so that the recommendation list can be matched directly to buildings in the rest of the workbook.

Completed buildings are visually identified so you can quickly see your position in the recommended progression.

The recommendation list is guidance rather than a requirement.

Your own **PlayerSort** priorities can override the order in which you personally choose to pursue available targets.

---

# Understanding Status

The tracker primarily uses three progression statuses.

## COMPLETED

The target has been completed.

No additional action is required.

## READY

All required dependencies have been satisfied.

The target is available to work on.

A READY target may still require resources before it can actually be purchased or completed.

## BLOCKED

One or more dependencies have not yet been satisfied.

The target is not currently available.

Use the Dashboard's **One Away** section and dependency information to determine what is preventing progression.

---

# Using Slicers

Some sheets use Excel **Slicers** to make large tables easier to navigate.

A slicer is a set of clickable filter buttons connected to a table.

Instead of opening the normal Excel filter menus, you can simply click the value you want to see.

For example, a slicer might allow you to display only:

* BUILDING
* TECH
* QUEST
* COLLECTION
* CRAFTIFACT
* CITADEL

## Selecting One Item

Click a slicer button once.

The table immediately filters to show only rows matching that selection.

## Selecting Multiple Items

Click the **Multi-Select** button in the upper-right corner of the slicer.

Then click each item you want included.

Depending on your version of Excel, you can also hold **Ctrl** while clicking multiple slicer buttons.

## Clearing a Slicer

Click the **Clear Filter** button in the upper-right corner of the slicer.

The table returns to showing all applicable records.

### If Something Seems Missing

Always check the slicers before assuming data has disappeared.

A slicer selection can remain active even after you move to another part of the workbook.

If a table appears unexpectedly short or an item you expect to see is missing:

1. Look at the connected slicers.
2. Clear their filters.
3. Check the table again.

---

# Other Tabs

Most players will not need to edit the remaining tabs during normal use.

## TargetStatus

This is the tracker's progression engine.

It calculates information such as:

* Player completion
* Dependency totals
* Completed dependencies
* Missing dependencies
* Status
* Funding status

This tab drives much of the Dashboard.

**Do not manually edit calculated values on this tab.**

---

## Targets

Contains the canonical list of targets recognized by the tracker.

Each target has a unique TargetID used throughout the workbook.

This is one of the core data tables and normally should not be edited during gameplay.

---

## Dependencies

Defines prerequisite relationships between targets.

For example, it tells the tracker that one building level, technology, state, or quest must be completed before another target becomes available.

Do not modify this tab during normal gameplay.

---

## QuestObjectives

Contains requirements associated with quest objectives.

These requirements are included in the dependency calculations used to determine quest progression.

Do not modify this tab during normal gameplay.

---

## CostStatus

Calculates funding progress for targets with resource costs.

It is used by the Dashboard to determine whether a target is unfunded, partially funded, or fully funded.

Do not manually edit this tab.

---

## Buildings

Contains the building data used by the tracker.

---

## Technologies

Contains technology data used by the tracker.

---

## Quests

Contains quest and quest-chapter data used by the tracker.

---

## Citadel

Contains Citadel progression data.

---

## Collections

Contains Collection progression data.

---

## Craftifacts

Contains Craftifact progression data.

---

## States

Contains state-based progression requirements, including character requirements and other game conditions used by dependencies and quest objectives.

---

## Recommended

Contains the Active and Passive recommended building progression.

Players may use this as a planning reference, but normally do not need to modify the recommendation data.

---

## Aliases

Contains mappings between names used by source data and the canonical names and TargetIDs used by the tracker.

This is primarily a maintenance/import tool.

---

## Inspector

Used for inspecting and validating relationships within the tracker.

This is primarily a maintenance and troubleshooting tab.

---

## Validation

Contains validation checks used to identify invalid or inconsistent tracker data.

This is primarily a maintenance tab.

---

## Exceptions

Used to record known exceptions or special cases that cannot safely follow the normal automated rules.

This is primarily a maintenance tab.

---

## Lists / Config / Import and Temporary Tabs

Tabs such as Lists, Config, Dep_Import, CostDependency, and CostTemp support calculations, imports, validation, or workbook maintenance.

They are not intended for normal player interaction.

---

# Normal Playing Routine

Once the tracker has been set up, keeping it current should be simple.

### When your character progresses

Update the relevant value on the **Player** tab.

Examples include:

* Character Level
* Cartographer
* Cooking

### When you complete something

Find the item on the **Checklist** and set **PlayerCompleted** to TRUE.

### When you pay resources toward something

Find the applicable resource rows on the **cost checklist** and set **PlayerPaid** to TRUE.

### When deciding what to do next

Return to the **Dashboard**.

Use:

* **Current Cost** for things you can currently fund
* **One Away** for near-future targets
* **Open Quests** for outstanding quest objectives
* **Pending Actions** to see what actions unlock
* **Funded not Complete** for things you may need to finish or mark complete
* **Resource Lookup** when deciding where to spend a particular resource
* **Recommended** building order as a progression guide

As long as the Player, Checklist, and cost checklist remain current, the rest of the tracker should update automatically.

---

# A Note About Tracker Recommendations

The tracker is intended to provide information, not dictate how you play.

The recommended building order represents a suggested progression strategy, while PlayerSort allows you to establish your own priorities.

You can freely choose a different path.

The tracker will continue recalculating available targets based on what you actually complete.
