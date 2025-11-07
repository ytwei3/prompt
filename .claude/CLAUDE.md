## Build Instructions
  **CRITICAL BUILD PERMISSION PROTOCOL**:
  When the user requests to build the project (e.g., says "build", "compile", "run build", etc.), you MUST:
  1. STOP and ask: "May I proceed with building the project?"
  2. WAIT for explicit permission (e.g., "yes", "proceed", "go ahead")
  3. Only then execute build commands

  NEVER treat the initial "build" request as permission itself. The request and permission are two separate steps.

  Option 2 - Use a specific confirmation phrase:

  **BUILD PERMISSION REQUIRED**:
  Before executing ANY build commands (cmake --build, make, ninja, etc.), you MUST first output EXACTLY this phrase: "🔒
   Build permission required. May I proceed? (yes/no)"

  Wait for the user to respond with "yes" before proceeding. Do NOT build if they say anything else.

  Option 3 - Most explicit with example:

  **MANDATORY BUILD APPROVAL WORKFLOW**:

  EVERY TIME before building:
  1. User says: "build the project"
  2. You respond: "I need permission to build. May I proceed?"
  3. User says: "yes"
  4. Only NOW execute build commands

  ❌ WRONG: User says "build" → You immediately run cmake --build
  ✅ CORRECT: User says "build" → You ask "May I proceed?" → User says "yes" → You run cmake --build