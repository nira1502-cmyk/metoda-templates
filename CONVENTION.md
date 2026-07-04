# מוסכמת מבנה פרויקטים — מתודה AI

## עיקרון
כל פרויקט עצמאי לחלוטין — קוד + תיעוד באותה תיקייה.
`_metoda-templates` = תבניות ריקות בלבד.

## מבנה תיקייה לכל פרויקט חדש

```
<project-name>/
├── _docs/
│   ├── spec/
│   │   ├── index.html          ← אפיון המערכת
│   │   └── [תמונות/נכסים]
│   └── guide/
│       ├── index.html          ← מדריך למשתמש
│       └── [תמונות/נכסים]
├── CLAUDE.md                   ← הנחיות לקלוד (העתק מ-template-CLAUDE.md)
└── [קבצי הפרויקט]
```

## Vercel — פריסה מתיקיית `_docs`

בכל פרויקט ב-Vercel, מגדירים 2 פרויקטים מאותו ריפו:
- **פרויקט ראשי** (`<name>.vercel.app`) → root dir: `/`
- **מדריך** (`<name>-guide.vercel.app`) → root dir: `/_docs/guide`
- **אפיון** (ב-`metoda-templates.vercel.app/<name>`) → root dir: `/_docs/spec` ← עדיין דרך _metoda-templates

## קבצי תבנית זמינים
- `template-CLAUDE.md` ← להעתיק לכל פרויקט חדש כ-CLAUDE.md
- `template-spec.html` ← בסיס לאפיון חדש
- `template-guide.html` ← בסיס למדריך חדש
- `shared-styles.css` ← עיצוב משותף לכל המסמכים
