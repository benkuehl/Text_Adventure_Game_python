Indiana Jones and the Last Crusade — A Python Text Adventure

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

A choose-your-own-adventure game written in Python, inspired by Indiana Jones and the Last Crusade. The player takes on the role of Indiana Jones on a quest to find the Holy Grail and rescue his father, navigating five stages of decisions where the wrong choice spells death — and the right one moves the story forward.
Built as a class project in my Master of Science in Management at Hult International Business School. The objective was to design a complete text adventure using core Python — functions, loops, conditionals, lists, and exception handling — to demonstrate command of the fundamentals.

The Game
The story unfolds across five stages, each a different puzzle mechanic:

Venice Catacombs — Identify the right sarcophagus among three to recover Sir Richard's shield and the clues for the trials ahead
The Breath of God — The first trial. Survive the corridor of swinging blades
The Word of God — The second trial. Spell the name of the Lord, one letter tile at a time, with the right Latin spelling
The Path of God — The third trial. The leap of faith across the chasm
The Grail Chamber — The final test. Choose the true Grail from five chalices

A wrong choice at any stage triggers a narrative death scene and an option to restart. Survive all five and you win, with an ASCII chalice and a closing speech from Indy's father and the Grail Knight.
How to Play
The notebook is interactive — to actually play, you need to run it (the input() prompts don't work in GitHub's static notebook preview):

Locally: download Indiana Jones - Text Adventure Game - Ben Kuehl.ipynb, open it in Jupyter Notebook, JupyterLab, or VS Code, and run the cell. Type your answers — letters, words, or numbers all work, the input parser is tolerant.
In Google Colab: open the notebook URL through Colab to run it in the browser without installing anything.

GitHub displays the full code and the ASCII art inline if you just want to read through without playing.
Python Techniques Demonstrated
The assignment was an exercise in core Python fundamentals. The notebook applies:

Modular function design — one function per stage, with each stage calling the next on success and fail() on failure
Input validation with while loops — re-prompts the user on invalid input instead of ending the game prematurely
Tolerant input parsing — every answer accepts multiple forms (e.g., c, kneel, crawl, and 3 all work for the Breath of God puzzle), using lists of valid inputs and .lower().strip() normalization
Nested conditionals — outer checks input validity, inner evaluates the actual choice
for loops with enumerate — used in the Word of God stage to walk through the letter sequence one tile at a time, and in the Grail Chamber to render the menu of chalices with 1-indexed numbering
try/except error handling — protects against ValueError on numeric input conversion and acts as a safety net for unexpected errors
time.sleep() — short pauses between scenes for dramatic pacing
ASCII art via print formatting — the win scene displays a chalice, the fail scene a skull, both purely text-based

File Structure
A single notebook containing:

One markdown cell — title, setting, how-to-play, known bugs, source attribution
One code cell — the full game, organized as an intro() entry function, five stage functions (catacombs, breath_of_god, word_of_god, path_of_god, grail_chamber), and win() / fail() end-state functions
