# Changelog - Recent Fixes

### 🐛 Bug Fixes
- **#50**: [BUG] Cross-project hook inheritance executes sibling project hooks inappropriately (bug, has repro, platform:macos, area:tools)
- **#48**: Claude Code executes wrong project hooks in multi-project workspace (bug, has repro, platform:macos, area:tools)
- **#37**: Invalid JSON Encoding in API Request Body (bug, duplicate, area:core, platform:macos, area:api)
- **#32**: Calling MCP tool create-spec-doc freezes in Cursor AI + GPT-5 (bug, area:mcp, area:ide, external)
- **#25**: Missing Tool Result Block for Tool Use ID toolu_01GUUUdR6TqtrqKTprMSuLqc (bug, duplicate, area:core, platform:macos, area:api)
- **#21**: Invalid JSON Encoding Error During API Request (bug, duplicate, area:core, platform:macos, area:api)
- **#15**: [BUG] Hard to trace changes in releases (bug)
- **#13**: Agent Command Autocomplete Regression in v72 (bug, has repro, platform:macos, area:tui)
- **#12**: [BUG] PowerLevel10k terminal theme causes Claude Code timeout and parsing failures due to ANSI escape sequence contamination (bug, has repro, area:core, platform:macos, area:tui)
- **#22**: [BUG] Search/Grep tool is BROKEN (bug, has repro, area:tools)

### 📚 Documentation
- **#39**: [DOCS] Slash command frontmatter table is misformatted (documentation)
- **#30**: [Docs] Undocumented `statusline` configuration feature (documentation, area:tui)
- **#23**: [Documentation] Claude Code release notes for v1.0.71 is not informative. Need more detailed notes. (documentation, enhancement)

### 🔄 Duplicates
- **#37**: Invalid JSON Encoding in API Request Body (duplicate of another issue)
- **#25**: Missing Tool Result Block for Tool Use ID toolu_01GUUUdR6TqtrqKTprMSuLqc (duplicate of another issue)
- **#21**: Invalid JSON Encoding Error During API Request (duplicate of another issue)

### 📊 Statistics
- **Total number of closed issues**: 14
- **Distribution by platform labels**:
  - `platform:macos`: 7 issues (#50, #48, #37, #25, #21, #13, #12)
- **Distribution by area labels**:
  - `area:tools`: 3 issues (#50, #48, #22)
  - `area:core`: 4 issues (#37, #25, #21, #12)
  - `area:api`: 3 issues (#37, #25, #21)
  - `area:mcp`: 1 issue (#32)
  - `area:ide`: 1 issue (#32)
  - `area:tui`: 4 issues (#30, #27, #13, #12)
  - `external`: 1 issue (#32)
  - `area:core` and `area:api` often co-occur (3 issues)
  - `area:tui` appears with both bug and documentation issues

*Note: Labels may overlap; an issue can have multiple area/platform labels.*