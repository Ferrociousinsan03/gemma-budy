# 📚 Gemma Study Buddy

Turn your notes into **summaries, quizzes and flashcards** using Google's open
[Gemma](https://ai.google.dev/gemma) model, running **locally** via Ollama.
No API keys, no data leaves your machine.

Built for the *Road to Devfest: Opensource Edition* build sprint.

## Features
- 3 modes: `summary`, `quiz`, `flashcards`
- Works with any Ollama model (default `gemma3:1b`)
- Unit-tested, with GitHub Actions CI

## Quick start
```bash
# 1. Install Ollama (https://ollama.com) and pull Gemma
ollama pull gemma3:1b

# 2. Set up the project
git clone https://github.com/YOUR_USERNAME/gemma-study-buddy.git
cd gemma-study-buddy
pip install -r requirements.txt

# 3. Run it
python -m study_buddy.cli sample_notes.txt --mode quiz
```

## Project structure
```
study_buddy/
  prompts.py   # prompt templates per mode
  client.py    # calls the local Gemma model
  cli.py       # command-line interface
tests/         # pytest unit tests
.github/workflows/ci.yml
```

## Roadmap
- [ ] Flutter front-end
- [ ] Save flashcards to Firebase
- [ ] PDF input

## License
MIT
