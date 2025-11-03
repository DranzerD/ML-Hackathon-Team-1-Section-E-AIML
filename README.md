Contents

- `Team1.ipynb` — Main notebook with environment, HMM oracle, Q-learning agent, training, evaluation and demo playback.

Quick summary

- The environment (`HangmanEnvironment`) simulates Hangman games and exposes a simplified, hashable state used by a tabular `QLearningAgent`.
- An `HMMOracle` is trained from a corpus to provide probability distributions over next letters; the agent can combine Q-values with HMM suggestions for action selection.

Requirements

- Python 3.8+ (the notebook kernel in this workspace uses Python 3.13).
- Typical scientific stack: numpy, pandas, matplotlib, scikit-learn, hmmlearn. The notebook kernel in this workspace already contains many of these packages.

How to run (local)

1. Open the notebook `Team1.ipynb` in Jupyter / VS Code.
2. Confirm your DATA_ROOT and `corpus.txt` / `test.txt` paths in the notebook. By default the notebook looks for files inside a `Data` folder near the notebook; the code also contains fallbacks to use packaged sample words.
3. Run the notebook cells top-to-bottom. Training can be long depending on `num_episodes` (the notebook uses 3000 episodes in the provided run).

Important notes

- The notebook includes shims and defensive checks to handle missing data files; if the corpus or test files are missing, it will fall back to a small sample word set so the demo still runs.
- The main cell runs training and evaluation and may take significant CPU time; consider lowering `num_episodes` while you iterate.
- Saved artifacts (plots, model pickle) are written to the `outputs/` directory.

Suggested quick experiment

- Set `num_episodes=100` in the `train_agent` call to verify the pipeline and demo gameplay quickly.

Files you may want to edit

- `Team1.ipynb` — adjust hyperparameters, `DATA_ROOT`, and episode counts.

Contact / License

- This repository is created for the ML Hackathon Team 1 (Section E). Use, modify and share per your team rules.

Enjoy experimenting with RL + HMM hybrid strategies!
