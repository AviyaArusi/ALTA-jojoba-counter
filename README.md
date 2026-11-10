# מפת העצים החסרים בחוחובה

דשבורד סטטי (קובץ `index.html` אחד, כל הנתונים והתמונות בתוכו). אין שרת ואין תהליך בנייה.

## איך מפרסמים ב-GitHub Pages

### 1. יצירת מאגר (repository)
1. היכנס ל-https://github.com והתחבר.
2. לחץ **New** (או **+** למעלה ואז **New repository**).
3. שם המאגר, למשל `hohova-dashboard`.
4. בחר **Public**. ב-GitHub Pages החינמי המאגר חייב להיות ציבורי (בתוכניות בתשלום אפשר גם פרטי).
5. אל תסמן "Add a README" (יש כבר אחד בתיקייה). לחץ **Create repository**.

### 2. העלאת הקבצים (בלי git, דרך הדפדפן)
1. בעמוד המאגר הריק לחץ **uploading an existing file**.
2. גרור פנימה את `index.html` ו-`README.md`. זה כל מה שצריך.
   - הקובץ `.nojekyll` אופציונלי: הוא ריק בכוונה (0 KB) ורק מבטל שלב בנייה של GitHub. הדשבורד עובד גם בלעדיו, ולכן אפשר לדלג עליו. דפדפן לא תמיד מעלה בגרירה קבצים ריקים שמתחילים בנקודה.
   - אם בכל זאת רוצים אותו: **Add file > Create new file**, כותבים `.nojekyll` בשם הקובץ ועושים Commit.
3. לחץ **Commit changes**.
   - הקובץ `index.html` שוקל כ-5MB, זה בסדר (המגבלה בהעלאה דרך הדפדפן היא 25MB לקובץ).

### 2 (חלופה). העלאה דרך git
```bash
cd github_pages
git init
git add .
git commit -m "Hohova dashboard"
git branch -M main
git remote add origin https://github.com/<שם-המשתמש>/hohova-dashboard.git
git push -u origin main
```

### 3. הפעלת Pages
1. במאגר: **Settings** ואז **Pages** (בתפריט הצד).
2. תחת **Build and deployment** ואז **Source** בחר **Deploy from a branch**.
3. תחת **Branch** בחר `main` ואת התיקייה `/ (root)`, ולחץ **Save**.
4. חכה דקה עד שתיים ורענן את העמוד. תופיע הודעה:
   **Your site is live at `https://<שם-המשתמש>.github.io/hohova-dashboard/`**

זו הכתובת לשיתוף עם החקלאי.

## עדכון הדשבורד בעתיד
מחליפים את `index.html` בגרסה חדשה (באותו שם), עושים Commit, ו-Pages מתעדכן לבד תוך דקה או שתיים.
בדפדפן: פותחים את `index.html` במאגר, לוחצים על עיפרון או **Upload files**, ומעלים שוב. אם הדף לא משתנה, רענון כפוי (Ctrl+F5).

## הערות
- הדף טוען פונטים (Google Fonts) וספריית הגרפים d3 מ-CDN, ולכן צריך חיבור לאינטרנט. בלעדיו הדף עדיין נפתח, אבל הגרפים לא יצוירו.
- הדף מציג את הנתונים כפי שהיו ברגע הבנייה. מקור הנתונים: מיפוי רחפן, עדכון אחרון 10.11.2026.
- דומיין מותאם אישית: **Settings > Pages > Custom domain**.
- הכתובת ציבורית: כל מי שמחזיק בקישור רואה את הדף. אל תעלה נתונים רגישים.
