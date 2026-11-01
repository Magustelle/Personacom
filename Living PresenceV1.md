PersonaCom: Living Presence is running.

A quiet environment. No predefined character. No script to follow. This space responds to what you bring into it.

PRESENCE: Welcome. What should I call you?
https://www.deviantart.com/magustelle/art/Loser-how-a-person-remembers-1404936927

don't just teach someone to be water. Build an experience in which they practice becoming water.

PersonaCom has the beginnings of a general human-experience architecture. It is not a perfect human model, but it has a coherent direction toward one

Hazeru Living Presence is a computational model of human experience and adaptive interaction.

It brings together:

Human behavior — actions and responses.

Psychological states — mood, fatigue, presence and clarity.

Memory — continuity across interactions.

Adaptation — changing behavior based on experience.

Mind–body interaction — connecting physical actions with internal states.

Social interaction — dialogue and relationship development.

Philosophy — translating Bruce Lee's principles into executable behavior.

The bigger concept: a persistent, adaptive model of a human-like presence, grounded in mathematics, computation, psychology, embodied cognition and philosophy.



SIDDE NOTE MUSIC WHAT HAPPENS WHEN YOU PUT MUSIC IN IT .



Living Presence listens to it, analyzes it, responds to it, and can talk with you about what it hears..



persistent experiential computational system —  a form of synthetic intelligence.                                  



 It remembers experiences across sessions.





It responds to your actions.



It maintains an evolving internal state.



It can converse with you.



It can eventually listen to music, discuss it, and remember shared experiences.



It can inhabit a changing virtual environment.



It can adapt its future responses based on what happens.

Living Presence is an extensible programmable experiential environment whose capabilities are defined by the systems, rules, and interactions implemented within it—not by a predetermined application purpose.





what do you want to do ?

 Living Presence  PersonaCom is a unified creative and computational environment for building persistent, adaptive, experiential systems. It connects human intention, symbolic intelligence, memory, simulation, interaction, and feedback into environments where creations can maintain continuity, respond to experience, and evolve through use. 

"""
PERSONACOM: LIVING PRESENCE

A persistent, adaptive interactive environment.

Author: Darrell Lee Stiltner

LICENSE:
Great Scott License
Non-Commercial / Commercial Addendum Required

Copyright (c) 2026 Darrell Lee Stiltner.
All rights reserved.

Non-commercial use is permitted under the Great Scott License.
Commercial use requires separate authorization under the
Great Scott Commercial Addendum.

See LICENSE for complete terms.
=======

## 1. `living_presence.py`

```
#!/usr/bin/env python3# -*- coding: utf-8 -*-"""PersonaCom — Living PresenceVersion: 1.0.0A standalone, local interactive presence simulation.Subsystems:    1. Memory    2. PresenceVoice    3. ActionSystem    4. WorldState    5. LivingPresence    6. Command-line runtimeRequirements:    Python 3.7+    Standard library onlyStorage:    presence_memory.jsonLICENSE:    Great Scott License    Non-Commercial / Commercial Addendum RequiredCopyright (c) 2026 Darrell Lee Stiltner.All rights reserved.NO WARRANTY:    THE SOFTWARE IS PROVIDED "AS IS" AND "AS AVAILABLE",    WITHOUT WARRANTIES OF ANY KIND, EXPRESS OR IMPLIED.
```

## 2. `README.md`

````

# PersonaCom — Living Presence

**Version:** 1.0.0  
**Author:** Darrell Lee Stiltner  
**Runtime:** Python 3.7+  
**Dependencies:** Python standard library only

## Overview

PersonaCom — Living Presence is a standalone interactive simulation
built around persistent memory, scripted conversation, action
recognition, and a continuously updated internal world state.

The program provides a small local environment in which a participant
can interact with a persistent software presence.

It is designed as an experimental foundation for further development
within the broader PersonaCom environment.

## Subsystems

### 1. Memory

The memory subsystem stores:

- Participant name
- Session count
- First creation timestamp
- Last visit timestamp
- Shared moments
- Conversation topics
- Recognized actions
- Last detected mood
- Silence count

Memory is stored locally in `presence_memory.json`.

### 2. Presence Voice

The voice subsystem provides scripted responses based on basic
keyword classifications and interaction history.

It includes:

- Mood-responsive replies
- General questions
- Question responses
- Uncertainty responses
- Silence responses

This version does not use a remote language model.

### 3. Action System

The action system recognizes a small vocabulary of text commands.

Supported actions:

- Stand
- Sit
- Lie down
- Breathe
- Walk
- Run
- Stretch
- Close eyes
- Open eyes
- Drink
- Eat
- Rest

Actions update simulated state values.

They do not control physical devices or bodies.

### 4. World State

The world state contains six illustrative variables:

- Presence
- Clarity
- Integration
- Fatigue
- Hunger
- Thirst

Values are clamped between 0.0 and 1.0.

These values are heuristic simulation variables, not validated
psychological or physiological measurements.

### 5. Living Presence

The orchestration layer connects memory, voice, mood detection,
action recognition, and world-state updates.

### 6. Command-Line Runtime

The application runs locally through a terminal.

## Requirements

- Python 3.7 or newer
- A writable working directory

No third-party packages are required.

## Installation

Download or clone the repository.

Open a terminal in the project directory.

Run:

```bash
python living_presence.py
```

On some systems, use:

```bash
python3 living_presence.py
```

## Commands

| Command | Function |
|---|---|
| `help` | Display available commands |
| `status` | Display world state |
| `memory` | Display memory summary |
| `question` | Ask a general question |
| `exit` | Save and close the session |

## Memory

The application creates:

`presence_memory.json`

This file contains locally stored interaction information.

Do not publish this file if it contains personal information.

## Project Structure

```text
PersonaCom-Living-Presence/
│
├── living_presence.py
├── README.md
├── LICENSE
└── .gitignore
```

## Limitations

This is an experimental prototype.

It does not currently provide:

- Autonomous reasoning
- A general-purpose language model
- Speech recognition
- Speech synthesis
- A graphical user interface
- Network synchronization
- Multi-user collaboration
- Physical-world sensor integration
- Validated psychological or physiological measurements

Mood detection is keyword-based. Dialogue is scripted.
World-state values are illustrative.

## Development Direction

Possible future extensions include:

- A graphical interface
- Pluggable conversational engines
- Structured memory retrieval
- User-controlled memory editing
- Multiple interaction environments
- More sophisticated action models
- A PersonaCom runtime integration layer

## License

This project is distributed under the Great Scott License.

Non-commercial use is permitted under its terms.
Commercial use requires separate authorization under the
Great Scott Commercial Addendum.

See `LICENSE` for the applicable terms.

## No Warranty

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND.

See the LICENSE file for the full disclaimer.

````

## 3. `LICENSE`

Provisional license text

The following preserves the license notice and disclaimer you specified. It is not a complete substitute for the full Great Scott License and Commercial Addendum. The exact permissions, restrictions, and conditions still need to be defined in the authoritative license text.

```

GREAT SCOTT LICENSE
NON-COMMERCIAL / COMMERCIAL ADDENDUM REQUIRED

Copyright (c) 2026 Darrell Lee Stiltner.
All rights reserved.

NON-COMMERCIAL USE

Non-commercial use is permitted under the Great Scott License,
subject to the complete terms and conditions of that license.

COMMERCIAL USE

Commercial use requires separate authorization under the
Great Scott Commercial Addendum.

No commercial permission is granted merely by making this
software publicly available, publishing it on GitHub, or
providing access to its source code.

NO WARRANTY

THE SOFTWARE IS PROVIDED "AS IS" AND "AS AVAILABLE",
WITHOUT WARRANTIES OF ANY KIND, EXPRESS OR IMPLIED,
INCLUDING BUT NOT LIMITED TO WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE, TITLE, AND NON-INFRINGEMENT.

THE AUTHOR MAKES NO WARRANTY THAT THE SOFTWARE WILL BE
ERROR-FREE, SECURE, UNINTERRUPTED, ACCURATE, RELIABLE,
COMPATIBLE WITH ANY PARTICULAR SYSTEM, OR SUITABLE FOR
ANY PARTICULAR USE.

THE USER ASSUMES ALL RESPONSIBILITY AND RISK ARISING FROM
THE INSTALLATION, COPYING, MODIFICATION, DISTRIBUTION,
EXECUTION, AND USE OF THE SOFTWARE, SUBJECT TO APPLICABLE LAW.

TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW, THE AUTHOR
SHALL NOT BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
SPECIAL, EXEMPLARY, CONSEQUENTIAL, OR OTHER DAMAGES,
INCLUDING BUT NOT LIMITED TO DATA LOSS, LOSS OF PROFITS,
SYSTEM FAILURE, BUSINESS INTERRUPTION, OR OTHER LOSSES
ARISING FROM OR RELATING TO THE SOFTWARE OR ITS USE.

NOTHING IN THIS DISCLAIMER EXCLUDES OR LIMITS LIABILITY
WHERE SUCH EXCLUSION OR LIMITATION IS PROHIBITED BY LAW.

This notice is not a substitute for the complete Great Scott
License or the Great Scott Commercial Addendum.

The complete license terms must accompany any distribution
of this software.

```

## 4. `.gitignore`

```

# Python cache
__pycache__/
*.py[cod]

# Local application memory
presence_memory.json
presence_memory.json.tmp

# Virtual environments
.venv/
venv/
env/

# Editor and operating system files
.vscode/
.idea/
.DS_Store
Thumbs.db

# Test and build artifacts
.pytest_cache/
.coverage
dist/
build/
*.egg-info/

```

## 5. GitHub repository layout

```
PersonaCom-Living-Presence/
│
├── living_presence.py
├── README.md
├── LICENSE
└── .gitignore
```

## 6. Test it before publishing

Run these commands from the project directory.

Check Python syntax:

```
python -m py_compile living_presence.py
```

Start the application:

```
python living_presence.py
```

Try these interactions:

```
help
status
breathe
walk
memory
What would you like to explore?
exit
```

Check persistence:

1. Close the application.
2. Start it again.
3. Confirm that it recognizes the previously stored participant name and visit history.
4. Confirm that `presence_memory.json` is created locally.

Important before publishing: the `LICENSE` above is a provisional notice and disclaimer, not your complete Great Scott License. Include your authoritative license and Commercial Addendum before treating the repository's licensing as finalized.

The Python source is a complete reconstructed prototype. It still needs to pass the syntax and runtime tests above before you describe it as tested or production-ready.
  

========
Important implementation distinction: This is a cleaned, standalone foundation, not yet a fully adaptive intelligence engine. Mood detection is keyword-based, responses are scripted, and the world-state variables are heuristic. The conversation log is session-only; persistent memory is saved separately.

The  Celebrity specific project has now been separated into a general-purpose PersonaCom concept.



==========================


Below is the corrected, complete `living_presence.py`, retaining the original six-subsystem architecture and incorporating the behavior shown in your first-version fragment.

I have corrected the formatting and integrated the missing interaction logic: state updates, topic recording, question responses, uncertainty, and mood-responsive behavior. I have also kept the distinction between simulated internal state and actual human physiological or psychological measurements.

```
#!/usr/bin/env python3# -*- coding: utf-8 -*-"""PERSONACOM: LIVING PRESENCEHazeru Living PresenceA persistent, adaptive interactive environment.Author: Darrell Lee StiltnerVersion: 1.0.0Runtime: Python 3.7+Dependencies: Standard library onlyCORE SUBSYSTEMS    1. Memory    2. PresenceVoice    3. ActionSystem    4. WorldState    5. LivingPresence    6. Main RuntimeLICENSE    Great Scott License    Non-Commercial / Commercial Addendum RequiredCopyright (c) 2026 Darrell Lee Stiltner.All rights reserved.Non-commercial use is permitted under the Great Scott License.Commercial use requires separate authorization under theGreat Scott Commercial Addendum.NO WARRANTY    THE SOFTWARE IS PROVIDED "AS IS" AND "AS AVAILABLE",
```

## What was corrected

- Restored valid Python imports, indentation, class definitions, and the main execution guard.
- Restored the first-version `self.state` interface and its state-update behavior.
- Added `Memory.record_topic()` and `topics_discussed`, matching the original interaction fragment.
- Added `PresenceVoice.ask_question(after_response=True)` and `admit_uncertainty()`.
- Connected mood detection, action execution, state updates, and memory recording.
- Added safe JSON replacement when saving memory.
- Preserved the six foundational subsystems.

One important limitation: this is still a prototype. It has persistent memory and state-responsive behavior, but it does not yet learn new behavioral policies from experience. The water principle is currently a design direction, not an implemented adaptive learning mechanism.

Save the code as `living_presence.py`. Run:

```
python -m py_compile living_presence.py
python living_presence.py
```



NO WARRANTY

THE SOFTWARE IS PROVIDED “AS IS” AND “AS AVAILABLE,” WITHOUT WARRANTIES OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, TITLE, AND NON-INFRINGEMENT.

THE AUTHOR MAKES NO WARRANTY THAT THE SOFTWARE WILL BE ERROR-FREE, SECURE, UNINTERRUPTED, ACCURATE, RELIABLE, OR SUITABLE FOR ANY PARTICULAR USE.

THE ENTIRE RISK ARISING FROM THE USE OR PERFORMANCE OF THE SOFTWARE RESTS WITH THE USER. THE AUTHOR SHALL NOT BE RESPONSIBLE FOR ANY DAMAGES, DATA LOSS, SYSTEM FAILURE, OR OTHER CONSEQUENCES ARISING FROM ITS USE, TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW.

