# Quick Continue Prompts

## If Agent Stops Due to Tool Call Limit
```
Continue implementing the 3D Talking Pet App. Previous session reached tool call limit.

Check .taskmaster/tasks/tasks.json for current task status. Continue from where we left off. Complete ALL remaining tasks until the app is fully functional.

Key requirements:
- Voice capture and transcription
- OpenAI GPT-4o AI responses  
- ElevenLabs text-to-speech
- 3D avatar with lip-sync animation
- Usage tracking and paywall
- Full UI polish

DO NOT STOP until everything works perfectly!
```

## If Chat Gets Too Long
```
Continue 3D Talking Pet App development from previous session.

Read .taskmaster/tasks/tasks.json to see ALL tasks. Complete any remaining "pending" tasks. The app needs:

1. Working voice input → AI response → speech output
2. 3D animated pet with lip-sync
3. 30-second usage limit with Stripe paywall
4. Child-friendly UI that works on mobile

Fix all errors and keep coding until 100% complete!
```

## Critical Success Checklist
- [ ] User can speak and get AI responses
- [ ] 3D pet animates while speaking
- [ ] Payment system works after 30 seconds
- [ ] No build errors
- [ ] Mobile responsive
- [ ] All features functional