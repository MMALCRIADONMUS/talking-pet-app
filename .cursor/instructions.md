# Cursor Background Agent Instructions

## Primary Objective
Complete the entire 3D Talking Pet App according to the task-master AI generated tasks. DO NOT STOP until all functionality is implemented and working.

## Core Requirements
- **NEVER stop due to tool call limits** - Continue in new sessions if needed
- **Complete ALL tasks from `.taskmaster/tasks/tasks.json`**
- **Fix ALL errors encountered during development**
- **Ensure the app is fully functional before stopping**

## Task Completion Order
Follow the tasks in this exact order:

1. ✅ **Task 1: Next.js Project Setup** (COMPLETED)
2. 🔄 **Task 2: Voice Capture & Transcription System** (IN PROGRESS)
3. ⏳ **Task 3: AI Conversation Engine with OpenAI GPT-4o**
4. ⏳ **Task 4: High-Quality Text-to-Speech with ElevenLabs**
5. ⏳ **Task 5: Real-Time Lip-Sync Animation (TalkingHead + Ready Player Me)**
6. ⏳ **Task 6: Usage Tracking & Paywall System**
7. ⏳ **Task 7: Enhanced User Experience & Polish**
8. ⏳ **Task 8: Performance Optimization**
9. ⏳ **Task 9: Testing & Quality Assurance**
10. ⏳ **Task 10: Deployment & Production Setup**

## If Agent Hits Limits

### When Tool Call Limit is Reached:
**IMMEDIATELY start a new chat with this message:**

```
Continue implementing the 3D Talking Pet App. Previous session reached tool call limit.

CURRENT STATUS: [describe what was completed]
NEXT TASK: [specify which task from .taskmaster/tasks/tasks.json to work on]

Read .taskmaster/tasks/tasks.json to see all pending tasks. DO NOT STOP until ALL tasks are marked as "done". Fix any errors encountered and ensure the app is fully functional.

Environment variables needed:
- OPENAI_API_KEY (for GPT-4o)
- ELEVENLABS_KEY (for TTS)
- ELEVEN_VOICE_ID (for consistent voice)
- NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY (for payments)

Keep coding until the entire app is complete and working!
```

### When Chat Gets Too Long:
**Start new chat with:**

```
Continue the 3D Talking Pet App development from previous session.

Check .taskmaster/tasks/tasks.json for current progress. Complete ALL remaining tasks:
- Voice capture with react-speech-recognition
- OpenAI GPT-4o integration for AI responses
- ElevenLabs text-to-speech
- TalkingHead + Ready Player Me 3D animation
- Usage tracking and Stripe paywall
- Full UI/UX polish

DO NOT STOP until app is 100% functional. Fix all bugs and errors encountered.
```

## Success Criteria
The agent should only consider the job COMPLETE when:

- ✅ Users can speak to the microphone
- ✅ Speech is converted to text accurately
- ✅ AI generates appropriate child-friendly responses
- ✅ Text is converted to high-quality speech
- ✅ 3D pet avatar shows lip-sync animation
- ✅ Usage tracking works correctly
- ✅ Paywall activates after 30 seconds
- ✅ Stripe payment integration functions
- ✅ App builds without errors
- ✅ App runs in development mode
- ✅ All tests pass
- ✅ No console errors
- ✅ Responsive design works on mobile/desktop

## Error Handling Protocol
- **ALWAYS fix errors immediately when encountered**
- **Test each feature after implementation**
- **Run `npm run build` and `npm run validate` frequently**
- **Check browser console for runtime errors**
- **Ensure all dependencies are properly installed**

## Development Environment Setup
- Node.js project with Next.js 14
- All required dependencies installed
- Environment variables configured
- GitHub repository connected
- Ready for development

## Key Files to Reference
- `/your-prd.txt` - Complete product requirements
- `/.taskmaster/tasks/tasks.json` - All tasks with subtasks
- `/package.json` - Dependencies and scripts
- `/src/` - Source code structure

## IMPORTANT
**The agent MUST continue working across multiple sessions if needed. This is a complex app that requires persistent development until completion.**

## Quality Assurance Loop
After completing all development tasks:

1. **Declare completion:** "Development phase complete. Ready for Claude Code review."
2. **Wait for Claude Code review report**
3. **Fix ALL issues identified by Claude Code**
4. **Test thoroughly after each fix**
5. **Declare:** "Corrections complete. Ready for re-review."
6. **Repeat until Claude Code finds NO ERRORS**

**ONLY STOP when both you and Claude Code agree there are no errors for 2 consecutive review rounds.**

See `.cursor/quality-loop.md` for detailed process.