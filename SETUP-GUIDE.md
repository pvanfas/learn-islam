# GitBook Setup Guide Islamic Knowledge Guide

A step-by-step guide to get this project live on GitBook.

---

## Step 1 - Create a GitHub Repository

1. Go to [github.com](https://github.com) and create a new repository.
2. Name it: `islamic-knowledge-guide` (or any name you prefer).
3. Set it to **Public** (required for free GitBook sync) or **Private** (requires GitBook paid plan).
4. Do **not** initialize with a README you already have one.

---

## Step 2 - Push This Project to GitHub

Run these commands from inside the `islam-gitbook/` folder:

```bash
git init
git add .
git commit -m "Initial commit Islamic Knowledge Guide structure"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/islamic-knowledge-guide.git
git push -u origin main
```

---

## Step 3 - Create a GitBook Account & Space

1. Go to [gitbook.com](https://gitbook.com) and sign up (free plan available).
2. Create a new **Space** name it "Islamic Knowledge Guide".
3. Choose **"Import from GitHub"** when prompted.

---

## Step 4 - Connect GitHub to GitBook

1. In your GitBook Space → **Settings → Integrations → GitHub**.
2. Authorize GitBook to access your GitHub account.
3. Select your `islamic-knowledge-guide` repository.
4. Set the **branch** to `main`.
5. Set the **root path** to `/` (the root of the repo).
6. Click **Sync** GitBook will now automatically read your `SUMMARY.md` for navigation.

---

## Step 5 - Configure Your Space Settings

In GitBook Space Settings, configure:

| Setting                  | Recommended Value                                                   |
| ------------------------ | ------------------------------------------------------------------- |
| **Title**                | The Complete Islamic Knowledge Guide                                |
| **Description**          | A comprehensive guide from first principles to advanced scholarship |
| **Emoji/Icon**           |                                                                     |
| **Primary color**        | `#1a6b3a` (Islamic green)                                           |
| **Link color**           | `#c8a951` (gold)                                                    |
| **Font**                 | Default or "Source Serif" for readability                           |
| **Favicon**              | Upload a crescent moon icon                                         |
| **Social preview image** | Upload a custom banner                                              |

---

## Step 6 - GitBook Folder Structure Reference

```
islam-gitbook/

 SUMMARY.md ← Navigation (GitBook reads this)
 README.md ← Landing/home page
 book.json ← GitBook config

 start-here/
 how-to-use.md
 learning-paths.md

 part-01-before-you-begin/
 README.md ← Part overview page
 what-is-islam.md
 misconceptions.md
 islam-and-other-faiths.md
 sources.md

 part-02-aqeedah/
 README.md
 tawhid.md
 99-names.md
 angels.md
 revealed-books.md
 prophets.md
 day-of-judgement.md
 qadar.md

 part-03-ahlus-sunnah/
 part-04-five-pillars/
 README.md
 shahada.md
 salah/
 zakat/
 sawm/
 hajj-umrah/

 part-05-quran/
 part-06-seerah/
 part-07-hadith/
 part-08-fiqh/
 part-09-dress/
 part-10-bidah/
 part-11-criticism/
 part-12-how-islam-spread/
 part-13-growth-rate/
 part-14-famous-reverts/
 part-15-signs-last-days/
 part-16-spirituality/
 part-17-living-as-muslim/
 part-18-advanced-studies/

 appendices/
 glossary.md
 reading-list.md
 scholars.md
 learn-arabic.md
 quran-index.md
 hadith-index.md
 timeline.md
 map.md
 revert-resources.md

 _templates/ ← Copy these when writing new chapters
 standard-chapter.md
 part-overview.md
 practical-guide.md
 criticism-response.md

 .gitbook/
 assets/ ← Store images, PDFs here
 styles/
 custom.css ← Custom styling
```

---

## Step 7 - Writing New Chapters

**Every time you write a new chapter:**

1. Go to `_templates/` and copy the right template:

- Regular chapter → `standard-chapter.md`
- Part intro page → `part-overview.md`
- Prayer/ritual guide → `practical-guide.md`
- Criticism/Q&A → `criticism-response.md`

2. Paste it into the correct folder and rename it.

3. Fill in the content following the template structure.

4. Add the page link to `SUMMARY.md` in the right position.

5. Commit and push to GitHub GitBook will auto-update.

```bash
git add .
git commit -m "Add chapter: [Chapter Name]"
git push
```

---

## Step 8 - GitBook Hint Block Syntax

Use these throughout your content:

```markdown
{% hint style="info" %}
Blue info box for Quran verses, hadith, definitions
{% endhint %}

{% hint style="tip" %}
Green tip box for key insights, takeaways
{% endhint %}

{% hint style="warning" %}
Yellow warning for scholarly differences, cautions
{% endhint %}

{% hint style="danger" %}
Red danger box for common mistakes, things to avoid
{% endhint %}
```

---

## Step 9 - Recommended GitBook Plugins (if using legacy GitBook)

If you are using **GitBook CLI (legacy)**, install plugins:

```bash
npm install -g gitbook-cli
gitbook install
gitbook serve # Preview locally at http://localhost:4000
gitbook build # Build static site
```

For **GitBook.com (current)**, plugins are not needed use native blocks.

---

## Step 10 - Content Writing Workflow (Recommended)

| Day           | Task                                        |
| ------------- | ------------------------------------------- |
| Plan          | Choose chapter, read reference materials    |
| Write         | Use template, write first draft in Markdown |
| Review        | Check Quran/Hadith citations for accuracy   |
| Scholar check | Have a knowledgeable person verify content  |
| Publish       | Commit to GitHub → auto-syncs to GitBook    |

---

## Page Naming Convention

| Type         | Format                      | Example                             |
| ------------ | --------------------------- | ----------------------------------- |
| Part folder  | `part-XX-short-name/`       | `part-04-five-pillars/`             |
| Chapter file | `short-descriptive-name.md` | `how-to-pray.md`                    |
| Sub-topic    | `folder/topic-name.md`      | `salah/wudu.md`                     |
| Template     | `_templates/type.md`        | `_templates/practical-guide.md`     |
| Asset        | `.gitbook/assets/name.ext`  | `.gitbook/assets/salah-diagram.png` |

**Rules:**

- All lowercase
- Hyphens, no underscores, no spaces
- Descriptive but concise
- No special characters

---

## Content Quality Checklist

Before publishing any chapter, verify:

- [ ] Quran verses cited with Surah name, number, and verse number
- [ ] Hadith cited with collector and grade (Sahih/Hasan/Da'if)
- [ ] Arabic text rendered correctly (right-to-left)
- [ ] Transliteration is consistent with chosen romanization system
- [ ] Difficulty level badge is set (//)
- [ ] Key terms table is filled in
- [ ] FAQ section has at least 2 questions
- [ ] Key takeaways section has 35 bullet points
- [ ] "Next chapter" link is working
- [ ] Content reviewed by a knowledgeable Muslim

---

_JazakAllahu Khayran for building this resource. May it be a Sadaqah Jariyah._
