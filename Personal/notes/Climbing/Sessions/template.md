---
date: <% tp.date.now("YYYY-MM-DD") %>
discipline: <% tp.system.suggester(["toprope", "bouldering"], ["toprope", "bouldering"], false, "Select Discipline") %>
overall_feeling: <% tp.system.suggester(["💪 Strong", "😅 Tired", "😬 Frustrated", "🫠 Zoned Out"], ["💪", "😅", "😬", "🫠"], false, "How'd it feel overall?") %>
---

# 🏔️ Climbing - <% tp.date.now("YYYY-MM-DD") %> - <% tp.file.frontmatter.discipline %>

## Climbs Log

### Climb 1 (e.g., "The Overhang Monster")
- **Grade:** // e.g., V4, 5.11a
- **Notes:**
- // Drag and drop pic for this climb here if you want! 📸

### Climb 2 (e.g., "Crimpy Corner")
- **Grade:**
- **Notes:**
- // Drag and drop pic for this climb here if you want! 📸

### Climb 3 (e.g., "Dynamic Duo")
- **Grade:**
- **Notes:**
- // Drag and drop pic for this climb here if you want! 📸

---
tags: [climbing, <% tp.file.frontmatter.discipline %>]