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

# Getting started (no experiment server set up)

- Make sure you have a functioning internet connection!
- Do this on a desktop PC or a laptop. Do _NOT_ use a mobile device, like a phone or tablet!

The easiest way to test a template _as is_:

1. Download this repository by clicking the green code button above and Download zip.
2. Unzip at a location of your choosing.
3. Inside the folder is a file called index.html, double click it in order to open it
   in a browser.

### Adapting stimuli
- Open the file `stimuli.js` in your plain text editor.
- There is a list, called LIST_1:

```javacript
const LIST_1 = [//...

```
-  This list can be adapted to your own needs, i.e, you can replace values, make the list longer (don't forget to increment the 'id' values for new items!).
- If you need to implement a more complex design, you should read the `stimuli.js` file (and its comment sections) a little better. 
- For an example of a Latin square design, please have a look [here](https://github.com/UiL-OTS-labs/jspsych-spr-mw) for some inspiration. 

In short: you can add additional lists if your experiment requires this, but then you also have to edit some other values in stimuli.js in order for your experiment to work as intended.

## Prepare for the data server setup (only for people affiliated to our lab!)

### Updating access key
In the file `globals.js` is a variable:
```javascript
const ACCESS_KEY = 'zeekretkey';
```
For uploading to the UiL-OTS data server you will need to change this to the access_key that you obtained when your experiment was approved. For elaborate info see `globals.js`.

Good luck!

