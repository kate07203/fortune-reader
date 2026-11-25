## My Initial Idea/Concept

A Little Fortune is an interactive reading inspired by tarot cards and the Magic 8 Ball. The visitor holds a question in mind, picks an intention, chooses their zodiac sign, and draws a celestial stamp. After a short pause, a card reveals a fortune and advice for their sign.

## Interface Sketch

[ Rest · Change · Clarity ]\
↓\
[ Zodiac cards ]\
↓\
[ Moon · Jupiter · Saturn ]\
↓\
[ Reveal my card ]\
↓\
✦ Fortune card + zodiac advice ✦

## Design Reflection

I wanted the reveal to feel like a small moment of mystery. Picking Rest, Change, or Clarity gives the visitor a chance to think about what they need that day. Their zodiac sign personalizes the advice, and choosing a stamp feels like pulling something from a deck. The hand-drawn borders and gently moving illustrations make the choices feel like cards. The gold glints mark the moment the fortune appears.

## Process Write-Up

I started with five Yes/No questions. I liked that they invited reflection, but the screen felt like a checklist. My classmate Robert suggested in our discussion post using the planets’ positions on the day someone visits. That got me thinking about the sky as an input, and I adapted his idea into a symbol the visitor could choose. I asked Codex where someone might feel that their choices didn’t matter. When the early symbol rule and The Star could both match, I decided the symbol should win because it was the visitor’s most deliberate choice. I asked Codex for a case I could predict before it explained the answer.

I tried two waiting messages in the design: “Reading your answers…” and “Turning over your Moon card…” I predicted the second would feel more personal because it acknowledged what the visitor had just chosen. I kept the delay at 900 milliseconds and edited the line to use the selected symbol’s name. The logic check confirmed that the name changed with the selection. How personal it feels is still a design judgment.

In the final version, JavaScript tracks *intention*, *zodiacSign*, *selectedSymbol*, and *revealStatus*. The reveal goes from ready to waiting to revealed. A change to any choice cancels a pending reveal. The intention and stamp determine the card. For example, Change with Jupiter gives Wheel of Fortune, and Change with Saturn gives The Hermit. Switching from Virgo to Sagittarius keeps the same card and changes the advice. Codex ran simulated checks for all 108 combinations and checked cancellation when a choice changed.

My biggest revision was replacing the five questions with one intention and giving each remaining choice a clear role. I also asked Codex to unify the illustrations after the different card styles made the page feel pieced together. I learned to ask for predictions, edge cases, and the exact line I could change. That helped me use AI to test my own decisions and see how the logic shaped what a visitor felt.
