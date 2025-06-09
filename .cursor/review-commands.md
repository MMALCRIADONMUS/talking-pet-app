# Review Loop Commands

## For User to Trigger Quality Loop

### After Cursor Agent Finishes Development
```
@claude-code: The Cursor Background Agent has completed development. Please perform a comprehensive code review of the entire 3D Talking Pet App. Check ALL files for:

1. TypeScript/JavaScript errors
2. Build and runtime issues  
3. Code quality problems
4. Security vulnerabilities
5. Performance issues
6. UX/accessibility problems
7. Missing functionality
8. Testing gaps

Create a detailed review report with specific fixes needed. We'll loop this between you and the agent until both find no errors 2 times in a row.
```

### After Claude Code Review
```
Continue fixing the 3D Talking Pet App based on Claude Code's review report. Address ALL issues found:

CRITICAL ISSUES (must fix):
[List from Claude's report]

WARNINGS (should fix):  
[List from Claude's report]

IMPROVEMENTS:
[List from Claude's report]

After implementing ALL fixes, run full tests and declare "corrections complete" so Claude Code can re-review.

DO NOT STOP until Claude Code approves the code quality!
```

### For Subsequent Rounds
```
@claude-code: Cursor Agent has completed corrections from review round [N]. Please perform re-review to:

1. Verify all previous issues are fixed
2. Check for any new issues introduced
3. Validate overall code quality
4. Test all functionality works

If issues remain, provide another detailed report. If no issues found, this counts as 1 clean review (need 2 consecutive clean reviews to finish).
```

## Quality Gates

### Round 1
- Cursor Agent: Completes development
- Claude Code: First comprehensive review
- Cursor Agent: Fixes all issues
- Claude Code: Re-review (1st clean review if no issues)

### Round 2  
- Cursor Agent: Additional fixes if needed
- Claude Code: Final review (2nd clean review if no issues)

### Success Condition
**STOP when both agree there are NO ERRORS for 2 consecutive reviews**

## Final Validation Commands

### Build Tests
```bash
npm run build
npm run lint  
npm run type-check
npm test
```

### Runtime Tests
```bash
npm run dev
# Test all features manually
```

### Code Quality
- No TypeScript errors
- No ESLint warnings
- No console errors
- All features working
- Mobile responsive
- Payment system functional
- Voice/AI/TTS working
- 3D animation working

This ensures production-ready code quality!