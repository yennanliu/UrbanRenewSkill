# Changelog

All notable changes to the Taiwan Urban Renewal Expert Skill will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2024-02-24

### Added
- 🎉 Initial release of Taiwan Urban Renewal Expert Skill
- ✨ Complete Urban Renewal Act (都市更新條例) interpretation capabilities
- ✨ Rights Transformation (權利變換) vs Agreement-based Joint Development (協議合建) analysis
- ✨ Floor Area Ratio (FAR) bonus calculation features
  - Green Building bonus evaluation
  - Smart Building bonus evaluation
  - TOD (Mass Transit Oriented Development) bonus evaluation
- ✨ Dangerous & Old Building Reconstruction (危老重建) vs Urban Renewal comparison
- ✨ Professional document drafting capabilities
  - Urban Renewal Business Plans (都市更新事業計畫書)
  - Rights Transformation Plans (權利變換計畫書)
  - Notices to Owners (所有權人通知書)
  - Joint Development Agreements (合建契約書)
- ✨ Consent threshold calculation and strategy guidance
- ✨ Legal compliance review and risk analysis
- ✨ Taipei City and New Taipei City localized regulations
- 📚 Comprehensive documentation
  - Main skill file (taiwan-urban-renewal.md)
  - Detailed README with usage instructions
  - Extensive examples (EXAMPLES.md)
  - Metadata configuration (skill.json)
- 🇹🇼 Full Traditional Chinese (Taiwan) language support
- ⚖️ Specific legal article citations for all interpretations

### Features by Category

#### Legal Intelligence (法規諮詢)
- Precise Urban Renewal Act interpretation
- Rights Transformation Regulation explanation
- Distinction between rights transformation and agreement methods
- Compulsory execution procedures
- Minority owner rights protection

#### Project Evaluation (案件評估)
- Building/community condition analysis
- FAR bonus evaluation (up to 50%)
- Distribution ratio calculations
- Financial feasibility assessment
- Comparative analysis (危老 vs 都更)

#### Consultancy & Strategy (諮詢策略)
- Neutral consulting for residents, landowners, and developers
- Consent threshold achievement strategies
- Dispute navigation and resolution
- Negotiation guidance
- Risk mitigation recommendations

#### Legal Counsel (法律諮商)
- Compulsory execution concerns
- Trust mechanism guidance
- Land ownership dispute resolution
- Developer agreement review
- Government approval process guidance

#### Documentation (文書製作)
- Business plan drafting
- Rights transformation plan creation
- Owner notification letters
- Joint development agreement templates
- Meeting summaries and government submissions

### Technical Details
- Built for Claude Code compatibility
- Requires Claude 3.5 Sonnet or higher
- Markdown format with YAML frontmatter
- Structured response templates
- Emoji-enhanced section headers for clarity

### Documentation
- Complete skill definition with role specifications
- 30+ page comprehensive guide
- 4 detailed usage examples
- Installation instructions (3 methods)
- Legal disclaimer and scope limitations

### Localization
- Taiwan-specific terminology
- Taipei City autonomy regulations
- New Taipei City specific rules
- Regional difference considerations

---

## [Unreleased]

### Planned Features for v1.1.0
- 🔄 Add more municipal regulations (Taichung, Tainan, Kaohsiung)
- 📊 Interactive calculator for FAR bonus combinations
- 📝 More document templates (meeting minutes, consultation reports)
- 🎓 Tutorial mode for beginners
- 🔍 Case law database integration
- 🌐 English language support (optional)

### Under Consideration
- Integration with Taiwan government API (if available)
- Real-time regulation update notifications
- Community-contributed case studies
- Video tutorials and walkthroughs
- Mobile-friendly reference guide

---

## Version History

| Version | Release Date | Status | Key Features |
|---------|-------------|--------|--------------|
| 1.0.0 | 2024-02-24 | **Current** | Initial release with full capabilities |
| 0.9.0 | 2024-02-20 | Beta | Internal testing |
| 0.5.0 | 2024-02-15 | Alpha | Prototype development |

---

## Migration Guide

### From Prompt Files to Skill Package

If you were using the standalone prompt files (`prompt_gpt.txt` or `prompt_gemini.txt`), migration to the skill package is straightforward:

**Old Method:**
```
Copy-paste prompt into AI assistant
```

**New Method (Claude Code):**
```bash
cd UrbanRenewSkill
claude-code
# Skill automatically loaded
```

**Benefits:**
- ✅ Automatic context loading
- ✅ Structured response format
- ✅ Version control
- ✅ Easy updates
- ✅ Better documentation

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on how to contribute to this project.

---

## Support

For bug reports, feature requests, or questions:
- 🐛 [Issue Tracker](https://github.com/your-org/UrbanRenewSkill/issues)
- 💬 [Discussions](https://github.com/your-org/UrbanRenewSkill/discussions)
- 📧 Email: contact@example.com

---

**Maintained by Jerry Liu**
**© 2024 Taiwan Urban Renewal Expert Skill**
