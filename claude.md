# Curse of Strahd: Reloaded - Project Overview for Claude

## Project Summary
**Curse of Strahd: Reloaded** is a comprehensive Dungeon Master's guide designed to improve the official "Curse of Strahd" campaign module. The guide restructures and enhances the original D&D 5th Edition campaign material for use with **Pathfinder 2nd Edition** mechanics and gameplay. The content is being prepared for integration into **Foundry VTT** using the **Lavaflow** import system.

**Key Integration Point**: This markdown-based guide will be imported into Foundry VTT via Lavaflow, converting the organized narrative and scene structure into Foundry-compatible journals, actor data, and adventure modules.

## Project Purpose & Goals
When working on this project, focus on:
- **Organizing** campaign material chronologically and by narrative beat (not just location-based)
- **Bridging** D&D 5E content to Pathfinder 2E mechanics where possible (difficulty, action economy, casting, etc.)
- **Structuring** content for optimal Lavaflow import into Foundry VTT
- **Providing** clear DM guidance, NPC profiles, encounter balancing, and scene descriptions
- **Enhancing** narrative cohesion and player agency throughout the campaign

### Specific Adaptations for Pathfinder 2E
- Note D&D 5E mechanics when they differ from PF2E (CR/XP calculations, spell mechanics, ability DC formulas)
- Reference PF2E difficulty scaling when adjusting encounters from 5E
- Account for PF2E's 3-action economy vs. 5E's single action + bonus action + reaction
- Consider PF2E's condition system when describing effects
- Adapt spell lists and abilities to PF2E-compatible alternatives where relevant

## Project Structure

### Directory Organization
```
Curse-of-Strahd-Reloaded/
├── claude.md (THIS FILE - agent instructions)
├── Introduction/
│   ├── A DM's Guide to Curse of Strahd.md (Overview, key issues addressed)
│   ├── Using This Guide.md (How to use this guide)
│   └── Changelog.md (Revision history)
├── Chapter 1 - Beginning the Campaign/
├── Chapter 2 - The Land of Barovia/
├── Chapter 3 - Running the Game/
├── Act I - Into the Mists/
│   ├── Arc A - Escape From Death House.md
│   ├── Arc B - Welcome to Barovia.md
│   ├── Arc C - Into the Valley.md
│   └── Act I Summary.md
├── Act II - The Shadowed Town/
├── Act III - The Broken Land/
├── Act IV - Secrets of the Ancient/
├── NPCs/ (Individual NPC profile files, organized by location/faction)
│   ├── Death House/ (Death House NPCs)
│   ├── Barovia/ (Barovia village NPCs)
│   ├── Companions/ (Potential party companions)
│   └── Antagonists/ (Major antagonists like Rahadin)
├── Appendices/
│   ├── Bestiary.md (Monster stat blocks with PF2E notes)
│   ├── Non-Player Characters.md (NPC index and overview)
│   ├── Glossary.md (Terminology and lore)
│   └── Amber Shards.md (Campaign-specific elements)
├── images/ (Visual assets - minimal count, primarily maps and key visuals)
└── publish.css (Styling for web output)
```

### Content Sections

#### Introduction Section (40 MD files total)
- **Chapter 1**: Campaign setup, character creation considerations
- **Chapter 2**: Barovia lore, history, setting mechanics
- **Chapter 3**: DM guidance, pacing, table management

#### Campaign Acts (Organized Chronologically)
- **Act I - Into the Mists**: Campaign opening, Death House, first encounters
- **Act II - The Shadowed Town**: Vallaki investigation and conflicts
- **Act III - The Broken Land**: Mid-campaign exploration, major plot developments
- **Act IV - Secrets of the Ancient**: Endgame preparation and Castle Ravenloft assault

#### Reference Materials
- **Bestiary**: Monster stat blocks with PF2E damage/action economy notes
- **NPCs**: Individual character profile files organized by location/faction (Death House, Barovia, Companions, Antagonists)
- **Non-Player Characters Index**: Central NPC overview and relationships
- **Glossary**: Terminology and lore reference
- **Amber Shards**: Special magical items and campaign mechanics

## Technical Context

### File Format & Metadata
- **Format**: Markdown with YAML frontmatter for metadata
- **Encoding**: UTF-8, cross-platform compatible
- **Styling**: CSS support (publish.css) for web and Foundry rendering
- **Total Content**: 40+ markdown files, structured for modular Lavaflow import

### Foundry VTT Integration (Lavaflow)
When creating or editing content, keep these Lavaflow conversion principles in mind:
- **Heading Structure**: Use H1-H3 headings for journal hierarchy (Lavaflow respects this)
- **Scene Descriptions**: Pre-written boxed text translates directly to Foundry journal entries
- **Encounter Tables**: Format clearly for Lavaflow actor/creature import
- **NPC Data**: Include stats, traits, and motivations for Foundry character sheets
- **Links**: Use `[[Internal Links]]` or `[External](url)` syntax for cross-references
- **Metadata**: YAML frontmatter helps organize journal tags and parent documents

### Editor & Tooling
- **Primary Editor**: Markdown-based (compatible with Obsidian, VSCode, etc.)
- **Version Control**: Git repository for revision tracking
- **Obsidian Support**: .obsidian directory with plugin configuration
- **Web Publishing**: Obsidian Publish integration for rendered output

## Game System: D&D 5E Content → Pathfinder 2E Mechanics

### Important Conversion Notes
- **Base Content**: Written for D&D 5th Edition ("Curse of Strahd" official module)
- **Target System**: Pathfinder 2nd Edition rules and mechanics
- **Conversion Strategy**: Keep 5E content structure while noting PF2E equivalencies and adjustments

### Key PF2E Considerations When Working on Content
1. **Encounter Difficulty**: PF2E uses different XP budgets and difficulty scaling than 5E
2. **Action Economy**: PF2E creatures use 3 actions/round; adjust tactical descriptions accordingly
3. **Damage Scaling**: PF2E creature damage is higher per action; adjust HP and attack bonuses
4. **Spellcasting**: PF2E spell system differs significantly; note alternative spells or abilities
5. **Conditions**: PF2E has specific conditions (Frightened, Sickened, etc.); map D&D effects appropriately
6. **Checks & DCs**: PF2E uses d20 + modifier vs. DC; convert 5E AC and saves to PF2E DCs

## Content Guidelines

### Repository Content Only
**CRITICAL:** Do not add information, guidance, or content that does not already exist in this repository unless explicitly approved by the user. All NPC profiles, scene guidance, mechanical notes, and supplementary content must be sourced from existing files within this project.

When building NPC files, scene descriptions, or reference materials:
- Extract content directly from existing markdown files
- Search the repository thoroughly before creating new sections
- If information doesn't exist in the repository, ask the user before adding it
- Exception: YAML frontmatter, structural formatting, and cross-references are acceptable without approval

### NPC Profile Files (Recent Development)
Individual NPC files are now being created in the `NPCs/` directory, organized by location/faction:
- **File Naming**: Use full NPC name without title (e.g., `Thornboldt Durst.md` not `Thornboldt the Blacksmith.md`)
- **Location**: Place files in appropriate subdirectory based on primary location/faction (e.g., Death House, Barovia, Companions, Antagonists)
- **New Locations**: Create new subdirectories as needed for different regions (e.g., Castle Ravenloft, Vallaki, Old Bonegrinder, Krezk)
- **Content**: Each file contains motivations, relationships, stat blocks, and interaction cues
- **Linking**: Use wiki-links to connect related NPCs and create relationship networks
- **Title Removal**: Avoid repeating titles in file content; let structure convey roles

### Strategic Internal Linking
When creating or editing NPC files and other character-focused documents, use wiki-links strategically to improve discoverability and cross-referencing:
- Link **first mentions** of related characters in sections/contexts
- Link **important relationships** (e.g., family connections, key relationships)
- Link characters when mentioned in **connections/relationships sections**
- Avoid over-linking routine mentions where context is already clear
- Use display text for clarity: `[[Thornboldt Durst|Thorn]]` instead of `[[Thorn]]`
- This approach improves Foundry journal navigation when imported via Lavaflow

## Working on This Project: Quick Reference

### When Creating New Content
1. Use clear H1-H3 heading structure for Foundry hierarchy
2. Include boxed text for scene descriptions (imports cleanly to Foundry journals)
3. Reference PF2E mechanics when discussing encounters or abilities
4. Note original 5E source material for reference
5. Ensure YAML frontmatter includes relevant metadata
6. **Only use information that already exists in the repository**

### When Editing Existing Content
1. Maintain chronological narrative structure
2. Clarify PF2E mechanical conversions where D&D 5E rules are referenced
3. Keep DM guidance notes organized and actionable
4. Preserve NPC personality and motivation clarity
5. Test that markdown structure will convert properly to Foundry via Lavaflow

### Common Tasks
- **Adding Encounters**: Include PF2E creature stat block summaries with level/difficulty notes
- **Refining NPC Profiles**: Ensure motivations and interaction cues are clear for DM improvisation
- **Improving Scene Guidance**: Use boxed text for read-aloud descriptions
- **Adjusting Pacing**: Reorganize content to maintain narrative momentum across acts
- **Documenting Changes**: Update Changelog.md with all significant revisions

## Key Features & Improvements

### Narrative Organization
- Chronological act structure vs. location-based (original module issue)
- Clear scene-by-scene guidance with read-aloud text
- Narrative hooks that tie back to Tarokka reading
- Cohesive themes of tragedy, hope, and redemption

### Encounter & Mechanic Adjustments
- Balanced difficulty for low-level parties (addresses original TPK encounters)
- Artifact distribution recommendations (controls early power scaling)
- NPC stat blocks adapted with PF2E mechanics notes
- Action economy guidance for PF2E combat

### DM Support
- Pre-written descriptions and NPC dialogue
- Table management tips and pacing advice
- Decision trees for handling player choices
- Lore reference for improvisation

## File Statistics & Content Scope
- **Markdown Files**: 50+ files (campaign acts + individual NPC profiles)
- **Estimated Word Count**: Multiple thousand words organized by campaign act and character profiles
- **NPC Profile Files**: Organized in NPCs/ directory with subdirectories for Death House, Barovia, Companions, and Antagonists
- **Visual Assets**: Minimal images in images/ directory (focused on essential maps and key visuals)
- **Deployment Target**: Foundry VTT (via Lavaflow import system)

## Target Audience & Use Cases
- **Primary**: Dungeon Masters running Curse of Strahd with PF2E system
- **Secondary**: Game designers interested in D&D-to-PF2E conversion approaches
- **Foundry Users**: VTT administrators importing content via Lavaflow

## Known Issues Addressed (vs. Original Module)
1. ✅ Disorganized content structure → Chronological narrative organization
2. ✅ Scattered critical information → Consolidated NPC/location profiles
3. ✅ Unbalanced encounters → Difficulty adjustments with PF2E notes
4. ✅ Weak Tarokka hooks → Improved narrative connections
5. ✅ Early artifact acquisition → Distribution guidance
6. ✅ Unclear Strahd characterization → Enhanced villain guidance

## Technical Requirements for Lavaflow Import
- Markdown with clean heading hierarchy
- Properly formatted tables for creature/NPC data
- YAML frontmatter for metadata and categorization
- Consistent filename conventions for scene organization
- Cross-references using wiki-link or markdown link syntax

## Related Projects & Resources
- **Source Material**: Official "Curse of Strahd" (Wizards of the Coast, D&D 5E)
- **VTT Platform**: Foundry Virtual Tabletop
- **Import Tool**: Lavaflow (markdown → Foundry converter)
- **Game System**: Pathfinder 2nd Edition
- **Editors**: Obsidian, VSCode, or any markdown editor

---

**Last Updated**: 2025-12-01
**Format Version**: Claude 3.5+ Optimized
**Intended Use**: Reference guide for AI agents, DMs, and content maintainers
