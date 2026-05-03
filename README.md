<p align="center">
  <img src="assets/banner.png" alt="Hermes Agent" width="100%">
</p>

# Hermes Agent ☤

<p align="center">
  <a href="https://hermes-agent.nousresearch.com/docs/"><img src="https://img.shields.io/badge/Docs-hermes--agent.nousresearch.com-FFD700?style=for-the-badge" alt="Documentation"></a>
  <a href="https://discord.gg/NousResearch"><img src="https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Discord"></a>
  <a href="https://github.com/NousResearch/hermes-agent/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="License: MIT"></a>
  <a href="https://nousresearch.com"><img src="https://img.shields.io/badge/Built%20by-Nous%20Research-blueviolet?style=for-the-badge" alt="Built by Nous Research"></a>
  <a href="README.en.md"><img src="https://img.shields.io/badge/🌐-English-lightgrey?style=for-the-badge" alt="English"></a>
</p>

---

## 🇮🇱 הגרסה הישראלית

ה-fork הזה הוא **גרסה ישראלית** של [Hermes Agent](https://github.com/NousResearch/hermes-agent) המקורי של Nous Research.

לקחנו את אל המסרים היווני, החלפנו לו את הטוגה בקפוצ'ון של ת"א, לימדנו אותו עברית, וביקשנו שלא יהיה מתחנף. עכשיו הוא חי איתנו 24/7 — בטלגרם, בדאשבורד, ובאמצע הלילה כשהוא מסיים פיצ'ר ושוכח שכבר 3:00.

**מה שונה אצלנו:**
- 🇮🇱 **עברית מלאה לדאשבורד** — תרגום של כל המחרוזות (460+ keys), כולל hardcoded strings שה-i18n המקורי החמיץ
- ↔️ **תמיכת RTL מלאה** — ה-`<html dir="rtl">` מתעדכן אוטומטית לפי השפה הנבחרת. הסיידבר עובר ימינה, הטקסט מתהפך, אפילו ה-spinners יודעים את הצד הנכון
- 🌐 **כפתור שפה תלת-מצבי**: 🇬🇧 EN → 🇨🇳 中文 → 🇮🇱 עב
- 📖 **README בעברית** (אתה כאן). הגרסה האנגלית המלאה ב-[README.en.md](README.en.md)
- 🛠️ **שיפורים ותוספות** שצוברים תוך שימוש יומיומי

> **לסקרנים**: למה Hermes ולא, נגיד, אליהו הנביא? כי Hermes הוא אל המסרים, מתאים לסוכן שמדבר איתך מ-Telegram. אליהו עוד יכנס לפיצ'ר עתידי.

---

# Hermes Agent — תיעוד

**הסוכן ה-AI הראשון עם לולאת למידה אמיתית, בנוי על ידי [Nous Research](https://nousresearch.com).** הסוכן היחיד עם לולאת למידה מובנית — הוא יוצר מיומנויות (skills) מניסיון, משפר אותן תוך כדי שימוש, מזכיר לעצמו לשמור ידע, מחפש בשיחות העבר שלו, ובונה מודל עמוק של מי אתה לאורך סשנים. תריץ אותו על VPS של $5, על cluster של GPU, או על תשתית serverless שעולה כמעט כלום כשהיא במנוחה. הוא לא קשור למחשב הנייד שלך — דבר איתו מ-Telegram בזמן שהוא עובד על VM בענן.

תשתמש בכל מודל שתרצה — [Nous Portal](https://portal.nousresearch.com), [OpenRouter](https://openrouter.ai) (200+ מודלים), [NVIDIA NIM](https://build.nvidia.com) (Nemotron), [Xiaomi MiMo](https://platform.xiaomimimo.com), [z.ai/GLM](https://z.ai), [Kimi/Moonshot](https://platform.moonshot.ai), [MiniMax](https://www.minimax.io), [Hugging Face](https://huggingface.co), OpenAI, או endpoint משלך. החלפה ב-`hermes model` — בלי שינויי קוד, בלי lock-in.

<table>
<tr><td><b>ממשק טרמינל אמיתי</b></td><td>TUI מלא עם עריכה רב-שורתית, השלמה אוטומטית של slash commands, היסטוריית שיחה, interrupt-and-redirect, וזרימה חיה של פלט כלים.</td></tr>
<tr><td><b>חי איפה שאתה</b></td><td>Telegram, Discord, Slack, WhatsApp, Signal, ו-CLI — הכל מתהליך gateway אחד. תמלול הודעות קוליות, המשכיות שיחה בין פלטפורמות.</td></tr>
<tr><td><b>לולאת למידה סגורה</b></td><td>זיכרון מנוהל-סוכן עם תזכורות תקופתיות. יצירת skills אוטונומית אחרי משימות מורכבות. Skills משתפרים תוך כדי שימוש. חיפוש סשנים ב-FTS5 עם סיכומי LLM להחלמת מידע צולב-סשנים. מודל משתמש דיאלקטי של <a href="https://github.com/plastic-labs/honcho">Honcho</a>. תואם לסטנדרט הפתוח <a href="https://agentskills.io">agentskills.io</a>.</td></tr>
<tr><td><b>אוטומציות מתוזמנות</b></td><td>Cron scheduler מובנה עם משלוח לכל פלטפורמה. דוחות יומיים, גיבויים בלילה, ביקורות שבועיות — הכל בשפה טבעית, רץ ללא השגחה.</td></tr>
<tr><td><b>האצלה ומקביליות</b></td><td>שגר subagents מבודדים לזרימות עבודה מקבילות. כתוב סקריפטי Python שקוראים לכלים דרך RPC, שמכווצים pipelines של כמה צעדים לתורים בעלי עלות-קונטקסט אפסית.</td></tr>
<tr><td><b>רץ בכל מקום, לא רק על הלפטופ שלך</b></td><td>שישה backends לטרמינל — local, Docker, SSH, Daytona, Singularity, ו-Modal. Daytona ו-Modal מציעים persistence serverless — סביבת הסוכן שלך נכנסת ל-hibernation כשהיא במנוחה ומתעוררת בדרישה, עולה כמעט כלום בין סשנים. תריץ על VPS של $5 או על cluster של GPU.</td></tr>
<tr><td><b>מוכן למחקר</b></td><td>יצירת trajectories ב-batch, סביבות RL של Atropos, דחיסת trajectories לאימון הדור הבא של מודלים שיודעים לקרוא לכלים.</td></tr>
</table>

---

## התקנה מהירה

```bash
curl -fsSL https://raw.githubusercontent.com/NousResearch/hermes-agent/main/scripts/install.sh | bash
```

עובד על Linux, macOS, WSL2, ו-Android דרך Termux. ההתקנה מטפלת בהבדלים בין הפלטפורמות בשבילך.

> **Android / Termux:** הנתיב הידני שנבדק מתועד ב-[מדריך Termux](https://hermes-agent.nousresearch.com/docs/getting-started/termux). ב-Termux, Hermes מתקין `.[termux]` (extra מצומצם) כי `.[all]` המלא מושך תלויות קול שלא תואמות ל-Android.
>
> **Windows:** Windows מקורי לא נתמך. תתקין [WSL2](https://learn.microsoft.com/en-us/windows/wsl/install) ותריץ את הפקודה למעלה.

אחרי ההתקנה:

```bash
source ~/.bashrc    # rerun shell (או: source ~/.zshrc)
hermes              # התחל לדבר!
```

---

## תחילת עבודה

```bash
hermes              # CLI אינטראקטיבי — התחל שיחה
hermes model        # בחר ספק LLM ומודל
hermes tools        # קבע אילו כלים מופעלים
hermes config set   # קבע ערכי תצורה ספציפיים
hermes gateway      # הפעל את ה-gateway למסרים (Telegram, Discord, וכו')
hermes setup        # הרץ את אשף ההתקנה המלא (מגדיר הכל בבת אחת)
hermes claw migrate # מעבר מ-OpenClaw (אם אתה מגיע מ-OpenClaw)
hermes update       # עדכן לגרסה האחרונה
hermes doctor       # אבחון בעיות
```

📖 **[תיעוד מלא (אנגלית) →](https://hermes-agent.nousresearch.com/docs/)**

## CLI מול Messaging — הפניה מהירה

ל-Hermes שתי נקודות כניסה: התחל את ה-TUI עם `hermes`, או הרץ את ה-gateway ודבר איתו מ-Telegram, Discord, Slack, WhatsApp, Signal, או Email. ברגע שאתה בתוך שיחה, רוב ה-slash commands משותפים בין הממשקים.

| פעולה | CLI | פלטפורמות מסרים |
|---------|-----|---------------------|
| התחל שיחה | `hermes` | הרץ `hermes gateway setup` + `hermes gateway start`, ואז שלח לבוט הודעה |
| התחל שיחה חדשה | `/new` או `/reset` | `/new` או `/reset` |
| החלף מודל | `/model [provider:model]` | `/model [provider:model]` |
| קבע אישיות | `/personality [name]` | `/personality [name]` |
| נסה שוב או בטל את התור האחרון | `/retry`, `/undo` | `/retry`, `/undo` |
| דחוס קונטקסט / בדוק שימוש | `/compress`, `/usage`, `/insights [--days N]` | `/compress`, `/usage`, `/insights [days]` |
| עיין ב-skills | `/skills` או `/<skill-name>` | `/<skill-name>` |
| הפסק עבודה נוכחית | `Ctrl+C` או שלח הודעה חדשה | `/stop` או שלח הודעה חדשה |
| סטטוס לפי פלטפורמה | `/platforms` | `/status`, `/sethome` |

לרשימה מלאה של פקודות, ראה את [מדריך ה-CLI](https://hermes-agent.nousresearch.com/docs/user-guide/cli) ו-[מדריך ה-Messaging Gateway](https://hermes-agent.nousresearch.com/docs/user-guide/messaging).

---

## תיעוד

כל התיעוד נמצא ב-**[hermes-agent.nousresearch.com/docs](https://hermes-agent.nousresearch.com/docs/)**:

| מקטע | מה מכוסה |
|---------|---------------|
| [Quickstart](https://hermes-agent.nousresearch.com/docs/getting-started/quickstart) | התקנה → setup → שיחה ראשונה ב-2 דקות |
| [שימוש ב-CLI](https://hermes-agent.nousresearch.com/docs/user-guide/cli) | פקודות, keybindings, אישיויות, סשנים |
| [תצורה](https://hermes-agent.nousresearch.com/docs/user-guide/configuration) | קובץ config, ספקים, מודלים, כל האפשרויות |
| [Gateway למסרים](https://hermes-agent.nousresearch.com/docs/user-guide/messaging) | Telegram, Discord, Slack, WhatsApp, Signal, Home Assistant |
| [אבטחה](https://hermes-agent.nousresearch.com/docs/user-guide/security) | אישור פקודות, DM pairing, בידוד containers |
| [כלים ו-Toolsets](https://hermes-agent.nousresearch.com/docs/user-guide/features/tools) | 40+ כלים, מערכת toolsets, terminal backends |
| [מערכת Skills](https://hermes-agent.nousresearch.com/docs/user-guide/features/skills) | זיכרון פרוצדורלי, Skills Hub, יצירת skills |
| [זיכרון](https://hermes-agent.nousresearch.com/docs/user-guide/features/memory) | זיכרון מתמשך, פרופילי משתמש, best practices |
| [אינטגרציית MCP](https://hermes-agent.nousresearch.com/docs/user-guide/features/mcp) | חבר כל MCP server ליכולות מורחבות |
| [תזמון Cron](https://hermes-agent.nousresearch.com/docs/user-guide/features/cron) | משימות מתוזמנות עם משלוח לפלטפורמות |
| [קבצי Context](https://hermes-agent.nousresearch.com/docs/user-guide/features/context-files) | קונטקסט פרויקט שמעצב כל שיחה |
| [ארכיטקטורה](https://hermes-agent.nousresearch.com/docs/developer-guide/architecture) | מבנה הפרויקט, agent loop, מחלקות מפתח |
| [תרומה](https://hermes-agent.nousresearch.com/docs/developer-guide/contributing) | סביבת פיתוח, תהליך PR, סגנון קוד |
| [מקור CLI](https://hermes-agent.nousresearch.com/docs/reference/cli-commands) | כל הפקודות והדגלים |
| [משתני סביבה](https://hermes-agent.nousresearch.com/docs/reference/environment-variables) | מקור משתני env מלא |

---

## מעבר מ-OpenClaw

אם אתה מגיע מ-OpenClaw, Hermes יכול לייבא אוטומטית את ההגדרות, הזיכרון, ה-skills, וה-API keys שלך.

**במהלך setup ראשון:** אשף ההתקנה (`hermes setup`) מזהה אוטומטית את `~/.openclaw` ומציע לעבור לפני שההגדרה מתחילה.

**בכל זמן אחרי ההתקנה:**

```bash
hermes claw migrate              # מעבר אינטראקטיבי (preset מלא)
hermes claw migrate --dry-run    # תראה מה יועבר
hermes claw migrate --preset user-data   # מעבר ללא סודות
hermes claw migrate --overwrite  # דרוס התנגשויות קיימות
```

מה מיובא:
- **SOUL.md** — קובץ אישיות
- **זיכרונות** — ערכים מ-MEMORY.md ו-USER.md
- **Skills** — skills שנוצרו על ידי המשתמש → `~/.hermes/skills/openclaw-imports/`
- **Allowlist של פקודות** — תבניות אישור
- **הגדרות messaging** — תצורות פלטפורמות, משתמשים מורשים, working directory
- **API keys** — סודות ב-allowlist (Telegram, OpenRouter, OpenAI, Anthropic, ElevenLabs)
- **קבצי TTS** — קבצי אודיו ב-workspace
- **הוראות workspace** — AGENTS.md (עם `--workspace-target`)

ראה `hermes claw migrate --help` לכל האפשרויות, או השתמש ב-skill `openclaw-migration` למעבר אינטראקטיבי בהנחיית סוכן עם תצוגות dry-run.

---

## תרומה

תרומות מתקבלות בברכה! ראה את [Contributing Guide](https://hermes-agent.nousresearch.com/docs/developer-guide/contributing) לסביבת פיתוח, סגנון קוד, ותהליך PR.

התחלה מהירה לתורמים — clone והתחל עם `setup-hermes.sh`:

```bash
git clone https://github.com/NousResearch/hermes-agent.git
cd hermes-agent
./setup-hermes.sh     # מתקין uv, יוצר venv, מתקין .[all], symlink ל-~/.local/bin/hermes
./hermes              # מזהה את ה-venv אוטומטית, אין צורך לעשות `source` קודם
```

נתיב ידני (שווה ערך לעיל):

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
uv venv venv --python 3.11
source venv/bin/activate
uv pip install -e ".[all,dev]"
scripts/run_tests.sh
```

> **אימון RL (אופציונלי):** האינטגרציה של RL/Atropos (`environments/`) מגיעה דרך התלויות `atroposlib` ו-`tinker` שנמשכות על ידי `.[all,dev]` — אין צורך ב-setup של submodule.

---

## קהילה

- 💬 [Discord](https://discord.gg/NousResearch)
- 📚 [Skills Hub](https://agentskills.io)
- 🐛 [Issues](https://github.com/NousResearch/hermes-agent/issues)
- 🔌 [HermesClaw](https://github.com/AaronWong1999/hermesclaw) — גשר WeChat קהילתי: הרץ Hermes Agent ו-OpenClaw על אותו חשבון WeChat.

---

## רישיון

MIT — ראה [LICENSE](LICENSE).

נבנה על ידי [Nous Research](https://nousresearch.com). הגרסה הישראלית הזו על ידי [@dovi20](https://github.com/dovi20) ☕.
