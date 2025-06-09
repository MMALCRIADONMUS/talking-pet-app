# Claude Code Review Template

## Comprehensive Review Checklist

### 1. Build & Compilation
- [ ] `npm run build` succeeds without errors
- [ ] `npm run type-check` passes all TypeScript checks
- [ ] `npm run lint` shows no warnings or errors
- [ ] All imports resolve correctly
- [ ] No unused dependencies in package.json

### 2. Code Quality & Structure
- [ ] TypeScript types are properly defined
- [ ] Functions have appropriate error handling
- [ ] Code follows consistent naming conventions
- [ ] No console.log statements in production code
- [ ] Proper async/await usage
- [ ] No memory leaks in React components
- [ ] Proper cleanup in useEffect hooks

### 3. Core Functionality Tests
- [ ] Voice capture works with react-speech-recognition
- [ ] OpenAI GPT-4o integration generates responses
- [ ] ElevenLabs TTS converts text to speech
- [ ] 3D avatar displays and animates
- [ ] Lip-sync synchronizes with audio
- [ ] Usage tracking counts time accurately
- [ ] Paywall triggers after 30 seconds
- [ ] Stripe payment integration functions

### 4. API Routes & Environment
- [ ] `/api/chat-with-pet` handles requests properly
- [ ] `/api/elevenlabs-tts` generates audio correctly
- [ ] Environment variables are validated
- [ ] API keys are properly secured
- [ ] Error responses are handled gracefully
- [ ] Rate limiting considerations

### 5. UI/UX & Responsiveness
- [ ] Child-friendly design implemented
- [ ] Large touch targets for children
- [ ] Mobile responsive on all screen sizes
- [ ] Visual feedback for recording states
- [ ] Loading states and animations
- [ ] Error messages are user-friendly
- [ ] Accessibility features (ARIA labels, etc.)

### 6. Performance & Optimization
- [ ] Bundle size is reasonable
- [ ] Images and assets are optimized
- [ ] Audio loading is efficient
- [ ] 3D rendering performance is smooth
- [ ] No unnecessary re-renders
- [ ] Lazy loading where appropriate

### 7. Security
- [ ] No API keys exposed in client code
- [ ] Input validation on all forms
- [ ] XSS protection implemented
- [ ] CSRF protection for payments
- [ ] Environment variables properly configured

### 8. Testing & Validation
- [ ] Core user flow works end-to-end
- [ ] Error scenarios are handled
- [ ] Edge cases considered
- [ ] Browser compatibility verified
- [ ] Mobile device testing

### 9. Task Completion Verification
- [ ] All 10 task-master tasks marked as complete
- [ ] Each subtask requirements fulfilled
- [ ] Test strategies from tasks executed
- [ ] Success criteria met for each task

### 10. Production Readiness
- [ ] Build artifacts are clean
- [ ] Environment setup documented
- [ ] Deployment configuration ready
- [ ] No development-only code in production
- [ ] Proper error boundaries implemented

## Review Report Format

```markdown
# Code Review Report - Round [N]
Date: [YYYY-MM-DD]
Reviewer: Claude Code

## Executive Summary
[Overall assessment of code quality and functionality]

## Issues Found: [TOTAL COUNT]

### 🚨 Critical Issues (Must Fix) - [COUNT]
1. **[Issue Title]** - `[file_path]:[line]`
   - **Problem:** [Detailed explanation]
   - **Impact:** [How this affects functionality]
   - **Solution:** [Specific fix required]
   ```javascript
   // Current (problematic) code
   
   // Fixed code should be:
   ```

### ⚠️ Warnings (Should Fix) - [COUNT]
1. **[Issue Title]** - `[file_path]:[line]`
   - **Problem:** [Explanation]
   - **Solution:** [Recommended fix]

### 💡 Improvements (Nice to Have) - [COUNT]
1. **[Improvement Title]** - `[file_path]`
   - **Current:** [Current approach]
   - **Better:** [Improved approach]
   - **Benefit:** [Why this is better]

## ✅ Fixed Issues from Previous Round
- [List items that were successfully fixed]

## 🧪 Testing Results
- **Build:** [PASS/FAIL] - [Details]
- **TypeScript:** [PASS/FAIL] - [Details]
- **ESLint:** [PASS/FAIL] - [Details]
- **Runtime:** [PASS/FAIL] - [Details]
- **Functionality:** [PASS/FAIL] - [Details]

## 📋 Task Completion Status
- **Voice Capture:** [COMPLETE/INCOMPLETE] - [Details]
- **AI Integration:** [COMPLETE/INCOMPLETE] - [Details]
- **Text-to-Speech:** [COMPLETE/INCOMPLETE] - [Details]
- **3D Animation:** [COMPLETE/INCOMPLETE] - [Details]
- **Usage Tracking:** [COMPLETE/INCOMPLETE] - [Details]
- **Payment System:** [COMPLETE/INCOMPLETE] - [Details]

## 🎯 Next Actions for Cursor Agent
1. [Specific instruction with file and line references]
2. [Specific instruction with expected outcome]
3. [Testing instruction to verify fixes]

## 🏁 Loop Status
- **Review Round:** [N]
- **Claude Code Status:** [PASS/FAIL]
- **Issues Remaining:** [COUNT]
- **Ready for Agent:** [YES/NO]
- **Quality Gate:** [NOT MET/1 CLEAN/2 CLEAN - DONE]

---
**Note:** Agent should address ALL critical issues and warnings before declaring "corrections complete"
```

This template ensures thorough, consistent reviews that catch all issues!