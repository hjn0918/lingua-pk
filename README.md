# LinguaPK - Jiani & Leo Language Learning

A fun, interactive language learning web app where two partners learn each other's language through PK battles, flashcards, and phrase practice.

## Who is it for?

- **Jiani** - native Chinese speaker learning French
- **Léo** - native French speaker learning Chinese
- Interface language: English

## Features

### PK Battle (Pass & Play)
- Take turns answering vocabulary questions
- 10 questions per battle (5 each)
- Real-time scoring and combo streaks
- 3-2-1 countdown at battle start

### Flashcard Practice
- Browse words by category (Greetings, Numbers, Food, Colors, Family, Travel, Animals, Verbs)
- Rate your knowledge: Again / Hard / Good / Easy
- Spaced repetition tracking with mastery levels
- Tap any card to hear pronunciation

### Phrase Book
- 6 real-life scenarios (Meeting, Restaurant, Shopping, Directions, Emergency, Small Talk)
- 7 phrases per scenario per language
- Pronunciation practice with speech recognition scoring
- Tap to hear native pronunciation

### Progress Tracking
- Day counter for learning streak
- Daily progress bar
- Side-by-side progress comparison (Jiani vs Léo)
- 8 achievement badges to unlock

## Tech Stack

- **Single HTML file** - no build step, no dependencies
- **Vanilla JavaScript** - no framework overhead
- **Web Speech API** - text-to-speech + speech recognition
- **localStorage** - progress saved in browser, works offline after first load

## Play Online

Visit: **https://YOUR_USERNAME.github.io/lingua-pk/**

(Replace `YOUR_USERNAME` with the GitHub account name)

## Run Locally

Just open `index.html` in any modern browser. That's it!

## Collaborate

This project is designed for two-person collaboration. To contribute:

1. Clone the repo
2. Edit `index.html` (everything is in one file)
3. Push changes
4. GitHub Pages auto-deploys on push

### Adding New Content

All vocabulary and phrases are in the `DATA` object inside `index.html`:

```javascript
const DATA = {
  fr: {  // French content (for Jiani)
    categories: { ... },  // vocabulary
    phrases: { ... }      // phrase book
  },
  zh: {  // Chinese content (for Léo)
    categories: { ... },
    phrases: { ... }
  }
};
```

## Browser Support

- Chrome / Edge (recommended - best speech API support)
- Firefox (TTS works, speech recognition limited)
- Safari (iOS 14.5+)

## License

MIT - feel free to fork and customize for your own language learning duo!

---

Made with love for learning languages together.
