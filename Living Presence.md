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

#!/usr/bin/env python3
# -*- coding: utf-8 -*-

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

NO WARRANTY:
The software is provided "AS IS", without warranty of any kind.
See LICENSE for complete terms.

Python 3.7+
Standard library only.
"""

import json
import os
import random
import time

from dataclasses import dataclass, asdict
from datetime import datetime


# ============================================================
# MEMORY
# ============================================================

class Memory:

    def __init__(self, save_file="presence_memory.json"):
        self.save_file = save_file

        self.participant_name = None
        self.visits = 0
        self.first_visit = None
        self.last_visit = None

        self.shared_moments = []
        self.topics_discussed = []
        self.actions_taken = []

        self.player_mood = "neutral"
        self.silence_count = 0

        self.load()

    def load(self):
        if not os.path.exists(self.save_file):
            return

        try:
            with open(self.save_file, "r", encoding="utf-8") as file:
                data = json.load(file)

            self.participant_name = data.get("participant_name")
            self.visits = data.get("visits", 0)
            self.first_visit = data.get("first_visit")
            self.last_visit = data.get("last_visit")

            self.shared_moments = data.get("shared_moments", [])
            self.topics_discussed = data.get("topics_discussed", [])
            self.actions_taken = data.get("actions_taken", [])

            self.player_mood = data.get("player_mood", "neutral")
            self.silence_count = data.get("silence_count", 0)

        except (OSError, ValueError, TypeError):
            print("[Memory] Existing memory could not be loaded.")

    def save(self):
        data = {
            "participant_name": self.participant_name,
            "visits": self.visits,
            "first_visit": self.first_visit,
            "last_visit": self.last_visit,
            "shared_moments": self.shared_moments,
            "topics_discussed": self.topics_discussed,
            "actions_taken": self.actions_taken,
            "player_mood": self.player_mood,
            "silence_count": self.silence_count,
        }

        temporary_file = self.save_file + ".tmp"

        try:
            with open(temporary_file, "w", encoding="utf-8") as file:
                json.dump(data, file, indent=4, ensure_ascii=False)

            os.replace(temporary_file, self.save_file)

        except OSError as error:
            print("[Memory] Could not save memory:", error)

    def begin_visit(self):
        now = datetime.now().isoformat(timespec="seconds")

        self.visits += 1
        self.last_visit = now

        if self.first_visit is None:
            self.first_visit = now

        self.save()

    def remember_name(self, name):
        self.participant_name = name.strip()
        self.save()

    def record_moment(self, moment):
        self.shared_moments.append({
            "time": datetime.now().isoformat(timespec="seconds"),
            "moment": moment
        })

        self.shared_moments = self.shared_moments[-100:]
        self.save()

    def record_topic(self, topic):
        topic = topic.strip().lower()

        if topic and topic not in self.topics_discussed:
            self.topics_discussed.append(topic)
            self.topics_discussed = self.topics_discussed[-200:]
            self.save()

    def record_action(self, action):
        self.actions_taken.append({
            "time": datetime.now().isoformat(timespec="seconds"),
            "action": action
        })

        self.actions_taken = self.actions_taken[-100:]
        self.save()

    def remember_mood(self, mood):
        self.player_mood = mood
        self.save()


# ============================================================
# PRESENCE VOICE
# ============================================================

class PresenceVoice:

    def __init__(self):
        self.conversation_depth = 0

        self.responses = {
            "happy": [
                "There's a brightness in that.",
                "I'm glad there's something good in this moment.",
                "What do you think brought that feeling forward?"
            ],

            "sad": [
                "We don't have to rush past that feeling.",
                "I'm here to listen.",
                "Would you like to talk about what's weighing on you?"
            ],

            "angry": [
                "Something seems to have struck a nerve.",
                "Let's take a moment with that.",
                "What happened?"
            ],

            "curious": [
                "That's interesting. Let's explore it.",
                "There's more to investigate here.",
                "What makes you curious about it?"
            ],

            "quiet": [
                "We can let the moment be quiet.",
                "There's no need to fill every silence.",
                "I'm here."
            ],

            "neutral": [
                "Tell me more.",
                "I'm listening.",
                "What comes to mind next?",
                "Let's explore that together."
            ]
        }

    def respond_to_mood(self, mood, user_input):
        self.conversation_depth += 1

        choices = self.responses.get(
            mood,
            self.responses["neutral"]
        )

        return random.choice(choices)

    def ask_question(self, after_response=False):
        questions = [
            "What do you make of that?",
            "What feels most important about it?",
            "Where would you like to take this?",
            "What haven't we considered yet?",
            "How does that connect to what came before?"
        ]

        return " " + random.choice(questions)

    def admit_uncertainty(self, topic):
        return (
            "I'm not entirely certain about "
            + str(topic)
            + ". Perhaps we can examine it together."
        )


# ============================================================
# ACTION SYSTEM
# ============================================================

class ActionSystem:

    ACTIONS = {
        "stand": "The environment records a standing action.",
        "sit": "The environment records a seated action.",
        "lie down": "The environment records a resting action.",
        "breathe": "A moment of breathing is acknowledged.",
        "walk": "The environment records movement.",
        "run": "The environment records faster movement.",
        "stretch": "The environment records stretching.",
        "close eyes": "A moment of stillness is acknowledged.",
        "open eyes": "Attention returns to the environment.",
        "drink": "The environment records drinking.",
        "eat": "The environment records eating."
    }

    def perform(self, action):
        normalized = action.strip().lower()

        if normalized in self.ACTIONS:
            return self.ACTIONS[normalized]

        return None


# ============================================================
# WORLD STATE
# ============================================================

@dataclass
class WorldState:

    presence: float = 0.5
    clarity: float = 0.5
    integration: float = 0.5

    fatigue: float = 0.0
    hunger: float = 0.0
    thirst: float = 0.0

    def clamp(self):
        for key, value in asdict(self).items():
            setattr(
                self,
                key,
                max(0.0, min(1.0, value))
            )


# ============================================================
# LIVING PRESENCE
# ============================================================

class LivingPresence:

    def __init__(self):
        self.memory = Memory()
        self.voice = PresenceVoice()
        self.actions = ActionSystem()
        self.state = WorldState()

        self.running = True
        self.last_interaction = time.time()

        self.memory.begin_visit()

    # --------------------------------------------------------
    # MOOD DETECTION
    # --------------------------------------------------------

    def detect_mood(self, user_input):
        text = user_input.lower()

        mood_keywords = {
            "happy": [
                "happy", "good", "great", "wonderful",
                "excited", "love", "joy"
            ],

            "sad": [
                "sad", "depressed", "lonely", "upset",
                "hurt", "cry", "unhappy"
            ],

            "angry": [
                "angry", "mad", "furious", "frustrated",
                "annoyed", "hate"
            ],

            "curious": [
                "wonder", "curious", "interesting",
                "why", "how", "discover", "learn"
            ],

            "quiet": [
                "quiet", "silence", "peaceful",
                "still", "nothing", "calm"
            ]
        }

        for mood, keywords in mood_keywords.items():
            if any(word in text for word in keywords):
                return mood

        return "neutral"

    # --------------------------------------------------------
    # ACTION PROCESSING
    # --------------------------------------------------------

    def process_action(self, user_input):
        action = self.actions.perform(user_input)

        if action is None:
            return None

        self.memory.record_action(user_input)
        self.memory.record_moment(action)

        return action

    # --------------------------------------------------------
    # WORLD STATE UPDATE
    # --------------------------------------------------------

    def update_world(self, user_input, mood):
        text = user_input.lower()

        if any(word in text for word in ["tired", "exhausted"]):
            self.state.fatigue += 0.1

        if mood == "curious":
            self.state.clarity += 0.03

        if mood == "quiet":
            self.state.presence += 0.03

        if mood == "happy":
            self.state.integration += 0.02

        if mood == "sad":
            self.state.integration -= 0.01

        if "thirsty" in text:
            self.state.thirst += 0.1

        if "hungry" in text:
            self.state.hunger += 0.1

        self.state.clamp()

    # --------------------------------------------------------
    # INTERACTION
    # --------------------------------------------------------

    def interact(self, user_input):

        user_input = user_input.strip()

        if not user_input:
            self.memory.silence_count += 1
            self.memory.save()

            return self.voice.respond_to_mood(
                "quiet",
                user_input
            )

        if user_input.lower() in ["exit", "quit", "leave"]:
            self.running = False
            self.memory.save()
            return "Until next time."

        # PARTICIPANT IDENTITY

        if self.memory.participant_name is None:
            self.memory.remember_name(user_input)

            return (
                "It's good to meet you, "
                + self.memory.participant_name
                + "."
            )

        # ACTION PROCESSING

        action_response = self.process_action(user_input)

        if action_response:
            return action_response

        # MOOD DETECTION

        mood = self.detect_mood(user_input)

        self.memory.remember_mood(mood)

        # WORLD UPDATE

        self.update_world(user_input, mood)

        # TOPIC RECORDING

        words = user_input.lower().split()

        for word in words:
            cleaned = word.strip(".,!?;:\"'()[]{}")

            if len(cleaned) > 4:
                self.memory.record_topic(cleaned)

        # RESPONSE GENERATION

        if "?" in user_input:
            response = (
                "That's worth exploring. "
                "Let's examine the question rather than "
                "assume we already know the answer."
            )

            response += self.voice.ask_question(
                after_response=True
            )

        elif (
            self.voice.conversation_depth > 5
            and random.random() < 0.3
        ):
            topic = (
                random.choice(self.memory.topics_discussed)
                if self.memory.topics_discussed
                else "that subject"
            )

            response = self.voice.admit_uncertainty(topic)

        else:
            response = self.voice.respond_to_mood(
                mood,
                user_input
            )

            if (
                len(user_input) > 20
                and random.random() < 0.2
            ):
                response += self.voice.ask_question()

        self.memory.record_moment(user_input)
        self.memory.save()

        self.last_interaction = time.time()

        return response

    # --------------------------------------------------------
    # STATUS
    # --------------------------------------------------------

    def get_status(self):
        return {
            "participant": self.memory.participant_name,
            "visits": self.memory.visits,
            "mood": self.memory.player_mood,
            "presence": round(self.state.presence, 2),
            "clarity": round(self.state.clarity, 2),
            "integration": round(self.state.integration, 2),
            "fatigue": round(self.state.fatigue, 2),
            "hunger": round(self.state.hunger, 2),
            "thirst": round(self.state.thirst, 2)
        }


# ============================================================
# MAIN RUNTIME
# ============================================================

def main():

    presence = LivingPresence()

    print()
    print("=" * 52)
    print("          PERSONACOM: LIVING PRESENCE")
    print("=" * 52)
    print()
    print("A persistent interactive environment.")
    print()
    print("Commands:")
    print("  status  - View internal world state")
    print("  help    - Display commands")
    print("  exit    - Leave the environment")
    print()
    print("You may also interact naturally.")
    print()

    if presence.memory.participant_name:
        print(
            "Welcome back, "
            + presence.memory.participant_name
            + "."
        )
    else:
        print("What should I call you?")

    print()

    try:
        while presence.running:

            user_input = input("YOU: ").strip()

            if user_input.lower() == "help":
                print()
                print("Talk naturally or use an action:")
                print(", ".join(ActionSystem.ACTIONS.keys()))
                print("Use 'status' to inspect world state.")
                print("Use 'exit' to leave.")
                print()
                continue

            if user_input.lower() == "status":
                print()
                for key, value in presence.get_status().items():
                    print("{}: {}".format(key, value))
                print()
                continue

            response = presence.interact(user_input)

            print()
            print("PRESENCE: " + response)
            print()

    except (KeyboardInterrupt, EOFError):
        print()
        print("Session interrupted.")

    finally:
        presence.memory.save()
        print()
        print("Memory saved.")
        print("Living Presence closed.")
        print()


if __name__ == "__main__":
    main()


Deployment

Save as living_presence.py, then run:
python living_presence.py


It creates presence_memory.json in the working directory.

Correction notes: This version restores the missing program structure and completes the truncated method. It also adds a status command, safer JSON saving, and persistent participant history. It remains a scripted, keyword-driven prototype; the world-state values are illustrative rather than validated measurements.














Ad
Ad options



Learn more

Important implementation distinction: This is a cleaned, standalone foundation, not yet a fully adaptive intelligence engine. Mood detection is keyword-based, responses are scripted, and the world-state variables are heuristic. The conversation log is session-only; persistent memory is saved separately.

The  Celebrity specific project has now been separated into a general-purpose PersonaCom concept.

NO WARRANTY

THE SOFTWARE IS PROVIDED “AS IS” AND “AS AVAILABLE,” WITHOUT WARRANTIES OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, TITLE, AND NON-INFRINGEMENT.

THE AUTHOR MAKES NO WARRANTY THAT THE SOFTWARE WILL BE ERROR-FREE, SECURE, UNINTERRUPTED, ACCURATE, RELIABLE, OR SUITABLE FOR ANY PARTICULAR USE.

THE ENTIRE RISK ARISING FROM THE USE OR PERFORMANCE OF THE SOFTWARE RESTS WITH THE USER. THE AUTHOR SHALL NOT BE RESPONSIBLE FOR ANY DAMAGES, DATA LOSS, SYSTEM FAILURE, OR OTHER CONSEQUENCES ARISING FROM ITS USE, TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW.








