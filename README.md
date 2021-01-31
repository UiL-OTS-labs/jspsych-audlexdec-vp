# jspsych-audlexdec-vp
Auditory [Lexical Decision](https://en.wikipedia.org/wiki/Lexical_decision_task) Experiment with _Visual Prime_ (template)

# Generic documentation
Please read the [generic documentation](https://github.com/UiL-OTS-labs/jspsych-uil-template-docs) for some context and scope.

# Task Description
Combined visual and Auditory lexical decision task (todo).

## Short description
Visually primed auditory lexical decision task: the participant sees a fixation cross, visual prime and then hears a real word or a non existing word (non-word). The task is to respond as quickly as possible and indicate wether the heard word is a real word or not (or wether both the visual and the heard word are real words, it depends on the instructions.

# Crucial trial phases (sub trial phases)
- Fixation cross
- Visual Item (Prime)
- Auditory item (Decision phase)

# Output

The data of _all_ (sub) _trial phases_ are logged in the data, but the output data can be filtered after data collection in many ways.
Please read the [general primer on jsPsych's data](https://github.com/UiL-OTS-labs/jspsych-output) if you are new to jsPsych data output.

Essential output for the _'true experimental'_ purpose in this template are:

- Reaction Time (RT) of the keyboard response in the decision phase
- Correctness of the keyboard response in the decision phase

The crucial trial/sub-trial phase (decision phase) output may look similar to this:

```json
	{
		"rt": 1210,
		"stimulus": "./sounds/clem.wav",
		"key_press": 76,
		"condition": "NON_WORD",
		"word": "clem",
		"word_file": "./sounds/clem.wav",
		"prime": "flower",
		"id": 4,
		"trial_phase": "present_word",
		"useful_data_flag": true,
		"correct_response": 0,
		"trial_type": "audio-keyboard-response",
		"trial_index": 25,
		"time_elapsed": 56913,
		"internal_node_id": "0.0-12.0-2.0",
		"subject": "y82nwppg",
		"list": "my_one_and_only_list",
		"correct": true,
		"key_chosen_ascii": 76,
		"key_chosen_char": "L",
		"yes_key": "A",
		"no_key": "L"
	},
	//(...)
```

# Getting started (the easy way, working internet connection required)
For now, the easiest way to test these templates, is:

1. Download this repository by clicking the green code button above and Download zip.
2. Unzip at a location of your choosing.
3. Inside the folder is a file called index.html, double click it in order to open it
   in a browser.
