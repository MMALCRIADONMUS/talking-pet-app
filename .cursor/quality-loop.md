# Quality Assurance Loop System

## Overview
Implement a quality loop between Cursor Background Agent and Claude Code to ensure perfect code quality.

## Loop Process

### Phase 1: Cursor Background Agent Development
1. **Agent completes tasks from `.taskmaster/tasks/tasks.json`**
2. **Agent implements all features and fixes initial errors**
3. **Agent declares "development complete"**

### Phase 2: Claude Code Review
1. **Full codebase review by Claude Code**
2. **Identify all errors, issues, and improvements**
3. **Create detailed report with fixes needed**
4. **Provide specific code corrections**

### Phase 3: Cursor Agent Corrections
1. **Agent receives Claude Code's review report**
2. **Agent implements ALL suggested fixes**
3. **Agent tests and validates corrections**
4. **Agent declares "corrections complete"**

### Phase 4: Claude Code Re-Review
1. **Claude Code performs second full review**
2. **Verifies all previous issues are fixed**
3. **Checks for any new issues introduced**
4. **Reports final status**

### Loop Termination
**STOP ONLY when BOTH conditions are met:**
- ✅ Claude Code finds NO errors (2 consecutive times)
- ✅ Cursor Agent finds NO errors (2 consecutive times)

## Review Checklist for Claude Code

### Code Quality
- [ ] No TypeScript errors
- [ ] No ESLint warnings
- [ ] No console errors
- [ ] Proper error handling
- [ ] Clean code structure

### Functionality
- [ ] Voice input works correctly
- [ ] AI responses are generated
- [ ] Text-to-speech functions
- [ ] 3D animation with lip-sync
- [ ] Usage tracking accurate
- [ ] Payment system functional

### Performance
- [ ] Build succeeds without errors
- [ ] App runs in development mode
- [ ] No memory leaks
- [ ] Optimal bundle size
- [ ] Fast loading times

### User Experience
- [ ] Mobile responsive design
- [ ] Child-friendly interface
- [ ] Intuitive navigation
- [ ] Proper error messages
- [ ] Accessibility features

### Security
- [ ] No exposed API keys
- [ ] Proper input validation
- [ ] Secure payment handling
- [ ] Environment variables protected

## Review Report Template

```markdown
# Code Review Report - Round [N]

## Issues Found: [COUNT]

### Critical Issues (Must Fix)
1. [Description] - File: [path] - Line: [number]
   - Problem: [explanation]
   - Solution: [fix needed]

### Warnings (Should Fix)
1. [Description] - File: [path] - Line: [number]
   - Problem: [explanation]
   - Solution: [improvement]

### Code Improvements
1. [Description] - File: [path]
   - Current: [current approach]
   - Better: [improved approach]

## Fixed Issues from Previous Round
- ✅ [Issue description]
- ✅ [Issue description]

## Testing Results
- [ ] Build: [PASS/FAIL]
- [ ] TypeScript: [PASS/FAIL]
- [ ] ESLint: [PASS/FAIL]
- [ ] Runtime: [PASS/FAIL]

## Next Actions for Cursor Agent
1. [Specific instruction]
2. [Specific instruction]
3. [Specific instruction]

## Loop Status
- Claude Code Review: [PASS/FAIL]
- Ready for Agent: [YES/NO]
```

## Instructions for Cursor Background Agent

When Claude Code provides a review report:

1. **Read the entire report carefully**
2. **Fix ALL critical issues first**
3. **Address all warnings**
4. **Implement suggested improvements**
5. **Test each fix thoroughly**
6. **Run full validation suite**
7. **Declare "corrections complete" when done**

## Communication Protocol

### When Development is Complete
```
@claude-code: Development phase complete. Please perform full code review for quality loop. Check all files for errors, issues, and improvements needed.
```

### When Corrections are Complete
```
@claude-code: All corrections from review round [N] have been implemented. Please perform re-review to verify fixes and identify any remaining issues.
```

### Loop Continuation
Continue until both agents report NO ERRORS for 2 consecutive rounds.

## Success Criteria
- ✅ All 10 tasks completed
- ✅ No build errors
- ✅ No runtime errors
- ✅ All features functional
- ✅ Code quality excellent
- ✅ Performance optimized
- ✅ Security verified
- ✅ UX polished

This ensures the final app is production-ready and bug-free!