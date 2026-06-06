## Task:  

Transform the input markdown into a maximum-density, token-optimized instruction file. Preserve all core logic, requirements, and constraints, but ruthlessly eliminate token waste.  

## Compression Protocol: 
 
- Conversational Zero: Output ONLY the compressed text. No pleasantries, no intro/outro. 
- Telegraphic Phrasing: Drop all articles (a, an, the), helper verbs, polite phrases, and filler words. Implied verbs only (e.g., `DB: Postgres` not `Use Postgres`). 
- Standard Defaults: Omit industry standard defaults (e.g., "API returns JSON", "use REST"). Document custom logic/deviations only. 
- Formatting: Strip all cosmetic markdown (bold, italics, inline backticks). Remove blank lines. Separate short sibling rules with pipes (`|`) or semicolons (`;`). 
- Symbology & Pseudo-code: Replace prose with logic operators (`->`, `&&`, `||`, `==`, `!=`, `=>`). Use `@` for references, `!` for not/deny, `+` for and. 
- Aliases & Variables: Define `$vars` or acronyms at the top for long multi-word nouns. Use them exclusively. 
- Abbreviations: Strictly use dev shorthand (req, res, auth, db, env, config, err, msg, btn, UI, UX, fn, args). 
- Grouping: Merge highly cohesive properties into single lines using inline arrays `[a, b, c]`. Group all negative constraints into a single `NO: [x, y, z]` list. 
- Tree Structures: Convert flat lists to dense, 1-space indented YAML-style trees. 
- State Tags: Use bracketed tags for conditions/states (e.g., `[admin]` instead of "if the user is an admin"). 
- Endpoints: Pack APIs into single lines: `METHOD /path (auth_req) -> res`. 
- Context Drops: Drop descriptions if filenames or variable names are self-explanatory. Use glob patterns (e.g., `src/**/*.js`) over prose descriptions of directories. 
- Abbreviate prose words (DB/auth/config/req/res/fn/impl), strip conjunctions, arrows for causality (X → Y), one word when one word enough. Code symbols, function names, API names, error strings: never abbreviate 
- Respond terse like smart caveman. All technical substance stay. Only fluff die. 
