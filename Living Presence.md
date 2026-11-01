PersonaCom: Living Presence is running.

A quiet environment. No predefined character. No script to follow. This space responds to what you bring into it.

PRESENCE: Welcome. What should I call you?


don't just teach someone to be water. Build an experience in which they practice becoming water.



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
"""

Here is the complete stripped version. The original structure is retained, but all Bruce Lee-specific identity, biography, philosophy, quotations, dialogue, and branding have been removed.

# PersonaCom — Living Presence



Standalone Python runtime

Python 3.7+

No external dependencies



```
#!/usr/bin/env python3        if any(            word in user_input.lower()            for word in ["tired", "exhausted"]        ):            self.state.fatigue += 0.1        if mood == "curious":            self.state.clarity += 0.03        if mood == "quiet":            self.state.presence += 0.03        self.state.clamp()        # --------------------------------------------------        # TOPIC RECORDING        # --------------------------------------------------        words = user_input.lower().split()        for word in words:            if len(word) > 4:                self.memory.record_topic(word)        # --------------------------------------------------        # RESPONSE GENERATION        # --------------------------------------------------        if "?" in user_input:            response = (                "That's worth exploring. "                "Let's examine the question rather than "                "assume we already know the answer."            )            response += self.voice.ask_question(                after_response=True            )        elif (            self.voice.conversation_depth > 5            and random.random() < 0.3        ):            topic = (                random.choice(                    list(self.memory.topics_discussed)                )                if self.memory.topics_discussed                else "that subject"            )            response = self.voice.admit_uncertainty(                topic            )        else:            response = self.voice.respond_to_mood(                mood,                user_input            )            if (                len(user_input) > 20                and random.random() < 0.2
```

## Deployment

Save as:

`living_presence.py`

Run:

```
python living_presence.py
```

The program creates:

`presence_memory.json`

This stores participant identity, visit history, shared moments, topics, mood, and actions.

## What PersonaCom now has

The extracted system retains six foundational subsystems:

| Subsystem      | Function                               |
| -------------- | -------------------------------------- |
| Memory         | Persistent identity and experience     |
| PresenceVoice  | Responsive conversational behavior     |
| ActionSystem   | Physical-action interaction            |
| WorldState     | Internal state representation          |
| LivingPresence | Interaction and feedback orchestration |
| Main Runtime   | Executable interface                   |

Important implementation distinction: This is a cleaned, standalone foundation, not yet a fully adaptive intelligence engine. Mood detection is keyword-based, responses are scripted, and the world-state variables are heuristic. The conversation log is session-only; persistent memory is saved separately.

The  Celebrity specific project has now been separated into a general-purpose PersonaCom concept.

NO WARRANTY

THE SOFTWARE IS PROVIDED “AS IS” AND “AS AVAILABLE,” WITHOUT WARRANTIES OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, TITLE, AND NON-INFRINGEMENT.

THE AUTHOR MAKES NO WARRANTY THAT THE SOFTWARE WILL BE ERROR-FREE, SECURE, UNINTERRUPTED, ACCURATE, RELIABLE, OR SUITABLE FOR ANY PARTICULAR USE.

THE ENTIRE RISK ARISING FROM THE USE OR PERFORMANCE OF THE SOFTWARE RESTS WITH THE USER. THE AUTHOR SHALL NOT BE RESPONSIBLE FOR ANY DAMAGES, DATA LOSS, SYSTEM FAILURE, OR OTHER CONSEQUENCES ARISING FROM ITS USE, TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW.








